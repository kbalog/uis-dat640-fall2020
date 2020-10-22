# A5 errata

## Query-document feature extraction

Regarding the function `extract_query_doc_features`, a correction and a clarification need to be made:

### Correction: Unique Terms in Field

The `unique_query_terms_in_{field}` feature yields the number of unique terms in the query that occur in the given document field.
There was a code error in `unique_query_terms_in_{field}` that has been fixed, which necessitates updated test cells. 

These are the test cells that will replace the ones in your notebook during grading. You may insert these to test your code solutions. Do not remove the incorrect test cells. 

These updated test cells are all downstream from the `extract_query_doc_features` function. 

Tests of query-document feature extraction:
```
# Tests of query-document feature extraction.

q0d2_features = extract_query_doc_features(analyze_query(es, QUERY[0], 'body'), 'd2', es, index='toy_index')
assert q0d2_features['unique_query_terms_in_title'] == 1
assert q0d2_features['sum_TF_body'] == 1

q0d3_features = extract_query_doc_features(analyze_query(es, QUERY[0], 'body'), 'd3', es, index='toy_index')
assert q0d3_features['avg_TF_title'] == 0.5
assert q0d3_features['max_TF_body'] == 1

q2d5_features = extract_query_doc_features(analyze_query(es, QUERY[2], 'body'), 'd5', es, index='toy_index')
assert q2d5_features['unique_query_terms_in_body'] == 2
assert q2d5_features['avg_TF_body'] == 1.0
```

Tests of the combined feature extraction:
```
# Tests of the combined feature extraction.

feature_vect_q0_d1 = extract_features(analyze_query(es, QUERY[0], 'body'), 'd1', es, index='toy_index')
assert feature_vect_q0_d1 == pytest.approx([2, 1.8325814637483102, 0.9162907318741551, 0.9162907318741551, 2, 
                                            5, 0, 0, 0, 0.0, 0, 0, 0, 0.0], abs=1e-5)

feature_vect_q1_d2 = extract_features(analyze_query(es, QUERY[1], 'body'), 'd2', es, index='toy_index')
assert feature_vect_q1_d2 == pytest.approx([1, 0.9162907318741551, 0.9162907318741551, 0.9162907318741551, 2, 
                                            5, 0, 0, 0, 0.0, 1, 1, 1, 1.0], abs=1e-5)

feature_vect_q3_d3 = extract_features(analyze_query(es, QUERY[3], 'body'), 'd3', es, index='toy_index')
assert feature_vect_q3_d3 == pytest.approx([2, 1.0216512475319814, 0.5108256237659907, 0.5108256237659907, 2, 
                                            4, 0, 0, 0, 0.0, 0, 0, 0, 0.0], abs=1e-5)
```

Test of preparation of training data:
```
# Test of preparation of training data.
assert len(X_train) == 63763
assert X_train[0] == pytest.approx([2, 9.04183708889101, 5.404451972764346, 4.520918544445505, 10, 
                                    251, 0, 0, 0, 0.0, 2, 2, 1, 1.0], abs=1e-5)
assert y_train[0] == 1
```

Test of learning-to-rank rankings:
```
# Test of learning-to-rank rankings
rankings_ltr = get_rankings(ltr, test_query_ids, es, index='trec9_index', rerank=True)
assert len(rankings_ltr['MSH2691']) == 16
assert rankings_ltr['MSH2691'].index('87254618') < rankings_ltr['MSH2691'].index('87216812')
```


### Clarification: Aggregate TF query-document features

The `'{sum/max/avg}_TF_{field}'` features should each be aggregated over a list of field-specific term frequencies in a document for each occurrence of a term in the list of analyzed query terms. That is, these features are to be computed over all query terms, not only unique ones.
