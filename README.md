# FAIRHealth

This repository contains two simulated datesets and one Python code (jupyter notebook) which converts CSV file to R2RML file. They are applied to test our privacy-preserving infrastructure (based on personal health train architecture) in a simulated scenario. More information you can find about:
1. Personal health train(PHT) concept: https://www.dtls.nl/fair-data/personal-health-train/
2. PHT Proof-of-Concept paper: https://www.ncbi.nlm.nih.gov/pubmed/29678027 
3. PHT Open-source code: https://bitbucket.org/jvsoest/pytaskmanager
2. FAIR stations: http://github.com/maastroclinic/DataFAIRifier 

## Simulated dataset
This simulated dataset is from a publicly available simulated dataset which contains variables that could be interpreted as sex, BMI, number of children, smoking status, region, and reimbursement information of patients [https://edu.kpfu.ru/pluginfile.php/278552/mod_resource/content/1/MachineLearningR__Brett_Lantz.pdf]. Additionally, we generated artificial personal identifiers including date of birth, zipcode, house number, and sex for record linkage by using a Python tool called Faker [https://faker.readthedocs.io/en/master/]. 

First, this dataset is vertically split over two providers: 
Provider A has personal identifiers, BMI, number of children, and smoking status; 
Provider B has the same personal identifiable information and living region, and reimbursement information. 

Second, we simulated that Provider A only hosts a small number of patients, i.e., 1338 patients, while Provider B hosts about 400,000 patients (which includes Provider A’s patients too). 

## Convert CSV to RDF file:
Prerequisites: 
1. Python 3+ 
2. Jupyter Notebook 
3. PostgresQL: https://www.postgresql.org/
4. R2RML (Mapping tool): https://github.com/nkons/r2rml-parser 
5. Knowledge on RDF: https://www.w3.org/TR/2004/REC-rdf-primer-20040210/#rdfxml 
