# Assignment 4 Errata

## Smoothing

Under ‘Advanced entity retrieval: PRMS’, under ‘Retrieval method’, the Dirichlet smoothing specifies that ’$\mu_i$ is the field-specific smoothing parameter (set to 1000)’. However, the corresponding global variable is set in the code cell below as MU = 100. In the context of A4, the coded value of 100 is correct, and the description’s mention of ‘set to 1000’ can be ignored.


## Indexing

Regarding the number of entities to be indexed, it appears the updating/editing of the subpages of 
`'Lists_of_musicians'` has been happening more frequently than anticipated when creating the assignment,
and thus the tests will need to be updated. For grading, we will update these tests at the time of grading. 

After running through the code in the reference solution this afternoon (13:30), there were 2748 unique entities indexed. 

The affected test cells are updated and provided below. You can insert and run these as 
code cells in your notebook, but do remove them before submission. Tests will be used during grading based on updates that will be current at that time. 

This is the current, updated test cell following `bulk_index`:

```
# Test index
tv_1 = es.termvectors(index=INDEX_NAME, id='Al Green', fields='catch_all')
assert tv_1['term_vectors']['catch_all']['terms']['1946']['term_freq'] == 23

tv_2 = es.termvectors(index=INDEX_NAME, id='Runhild Gammelsæter', fields='attributes')
assert tv_2['term_vectors']['attributes']['terms']['khlyst']['term_freq'] == 1

tv_3 = es.termvectors(index=INDEX_NAME, id='Music of Belarus', fields='description')
assert tv_3['term_vectors']['description']['terms']['kazakhstan']['term_freq'] == 1

tv_4 = es.termvectors(index=INDEX_NAME, id='MC HotDog', fields=['types', 'description'])
assert tv_4['term_vectors']['description']['terms']['microphon']['term_freq'] == 1

tv_5 = es.termvectors(index=INDEX_NAME, id='Deadmau5', fields=['types', 'description', 'related_entities'])
assert tv_5['term_vectors']['description']['terms']['italiano']['term_freq'] == 1
```

The updated test cell for `prms_retrieval` is 

```
# Tests for PRMS retrieval

prms_query_1 = 'winter snow'
prms_retrieval_1 = prms_retrieval(es, prms_query_1)
assert prms_retrieval_1[:5] == ['Snow (musician)', 'Kurt Winter', 'Hank Snow', 'Derek Miller', 'Richard Manuel']

prms_query_2 = 'summer sun'
prms_retrieval_2 = prms_retrieval(es, prms_query_2)
assert prms_retrieval_2[:5] == ['Joseph Summers (musician)', 'Sun Nan', 'Stefanie Sun', 'Virgil Sturgill', 'Robert Turner (composer)']

prms_query_3 = 'freedom jazz'
prms_retrieval_3 = prms_retrieval(es, prms_query_3)
assert prms_retrieval_3[:5] == ['Paul Bley', 'Stéphane Galland', 'Saifo', 'Christy Sutherland', 'K.d. lang']
```

and the final test cell comparing the above with baseline retrieval needs no update.  

Getting less than 2500 items indexed will not be penalized. The tests will be adjusted if necessary. 

## Field mapping probabilities

There was a small notational inconsistency in the description and variable 
names of the code for `get_term_mapping_probabilities`.

The correct description should be 
"
Implement the function `get_term_mapping_probs` to return $P(f|t)$ of all fields $f$ 
for a given term $t$ according to the description above of how PRMS extends the MLM retrieval model. 
"
and the Dictionary of mapping probabilities to be returned by `get_term_mapping_probabilities` 
should properly be named `Pf_t` rather than `Pt_f`, reflecting that mapping probability is the probability 
(normalized over the probabilities of all fields) that a given field $f$  should be the 
field to which a term $t$ would be mapped. 

You may consider this your starting point for implementing that solution, if you find it helpful:
```
def get_term_mapping_probs(es, clm, term):
    """PRMS: For a single term, find their mapping probabilities for all fields.
    
    Arguments:
        es: An active Elasticsearch instance.
        clm: Collection language model instance.
        term: A single-term string. 
        
    Returns:
        Dictionary of mapping probabilities for the fields.
    """
    Pf_t = {}
    # YOUR CODE HERE
    raise NotImplementedError()
    return Pf_t
```

Use the longer mathematical description under the heading "Retrieval method" in the 
A4 notebook and note that the mapping probability is $P(f|t)$. 

### Alternative test

Since the field probability mapping depends on the index, and there are many discrepancies between what students are finding and the tests which are based on the updated index resulting from the reference solution, we have created an alternative test on a toy `TestCollectionLM` for use in testing `get_term_mapping_probs`. This new test cell should indicate whether your solution for `get_term_mapping_probs` is equivalent to the reference solution:

```
class TestCollectionLM(object):
    def __init__(self):
        self._probs = {
            'names': {
                't1': 1/3,
                't2': 0,
                't3': 1/9,
                't4': 1/9,
                't5': 1/3,
                'gospel': 1/9,
                'soul': 2/9
            },
            'types': {
                't1': 5/18,
                't2': 1/18,
                't3': 1/3,
                't4': 1/6,
                't5': 1/6,
                'gospel': 0,
                'soul': 0                
            },
            'description': {
                't1': 1/20,
                't2': 1/20,
                't3': 1/10,
                't4': 1/10,
                't5': 2/10,
                'gospel': 4/10,
                'soul': 1/5                 
            },
            'attributes': {                
            },
            'related_entities': {
                't1': 1/8,
                't2': 0,
                't3': 0,
                't4': 1/4,
                't5': 0,
                'gospel': 1/2,
                'soul': 1/8                
            },
            'catch_all': {
                't1': 2/14,
                't2': 2/14,
                't3': 1/14,
                't4': 0,
                't5': 2/14,
                'gospel': 3/14,
                'soul': 4/14                
            }            
        }
    def prob(self, field, term):
        return self._probs.get(field, {}).get(term, 0)
        
# Tests for field mapping probabilities
clm_3 = TestCollectionLM()
Pf_t_3_1 = get_term_mapping_probs(None, clm_3, 'gospel')
assert Pf_t_3_1['description'] == pytest.approx(0.32642, abs=1e-5)
assert Pf_t_3_1['attributes'] == pytest.approx(0, abs=1e-5)
assert Pf_t_3_1['related_entities'] == pytest.approx(0.40803, abs=1e-5)
Pf_t_3_2 = get_term_mapping_probs(None, clm_3, 'soul')
assert Pf_t_3_2['names'] == pytest.approx(0.26679, abs=1e-5)
assert Pf_t_3_2['types'] == pytest.approx(0, abs=1e-5)
assert Pf_t_3_2['catch_all'] == pytest.approx(0.34302, abs=1e-5)
```

This alternative test will replace the original test for the purposes of grading the assignment.  


