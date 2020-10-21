# A5 erratum

## Query-document feature extraction

Regarding the function `extract_query_doc_features`, there are two clarifications to be made:
    - The ‘unique_query_terms_in_{field}’ feature should count every occurrence of a term in the list of analyzed query terms. In other words, although the wording "unique query terms" may imply only the set of query terms, this feature should count all the query terms in the query. 
    - The {sum/max/avg}_TF_{field} features should each be aggregated over a list of field-specific term frequencies in a document for each occurrence of a term in the list of analyzed query terms. That is, these features are to be computed over all query terms, not only unique ones.

The test for this function will need to be passed as it is in the A5 assignment notebook. 
