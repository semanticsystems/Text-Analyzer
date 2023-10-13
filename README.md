# News Text Analyzer with Ontology Matching

This Jupyter Notebook processes a text document containing news content and uses spaCy to identify entities. The identified entities are then compared with an existing ontology to determine matching classes and instances.

## Dependencies:

- **spaCy** 
    - A library for advanced Natural Language Processing in Python.
    - Install in a Jupyter cell: `!pip install spacy`
  
- **rdflib**
    - A library for working with RDF, a simple yet powerful language for representing information.
    - Install in a Jupyter cell: `!pip install rdflib`

## How to Run:

1. Ensure you have Jupyter Notebook installed. If not, install it using: `!pip install jupyter`
2. Launch Jupyter Notebook: `jupyter notebook`
3. Navigate to the directory containing this notebook and open it.
4. Ensure `spaCy` and `rdflib` are installed.
5. Download the required `en_core_web_lg` spaCy model in a Jupyter cell: `!python -m spacy download en_core_web_lg`
6. Modify the `file_path` variable to point to your text file. By default, it's set to 'news.txt'.
7. Modify the `existing_ontology.parse()` function to point to your ontology file. By default, it's set to 'test.ttl'.
8. Execute each cell sequentially in the notebook.

## Outputs:

The script will output:

- Number of matching classes in the existing ontology vs. total identified classes from the news text.
- Number of matching instances in the existing ontology vs. total identified instances from the news text.
- Lists of classes and instances identified in the news text but not found in the existing ontology.

## Notes:

- The script assumes the ontology is in Turtle format. Adjust the `format` parameter in `existing_ontology.parse()` if your ontology is in another format.
- Entities identified are encoded to create valid URIs. Spaces are replaced with underscores and double quotes are removed.

## License:

This code is under the MIT License.
