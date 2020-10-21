# A5 erratum

## Query-document feature extraction

Regarding the function `extract_query_doc_features`, there are two clarifications to be made:
    - The ‘unique_query_terms_in_{field}’ feature should count every occurrence of a term in the list of analyzed query terms. 
    - The {sum/max/avg}_TF_{field} features should each be aggregated over a list of field-specific term frequencies in a document for each occurrence of a term in the list of analyzed query terms.
