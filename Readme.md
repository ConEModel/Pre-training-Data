## Leaf Goal Identification from Event Log Using LogFiBER Model
## Prerequisite
 - LogFiBER Model (BERT based Transformer Model trained on [MIMIC clinical dataset])(https://www.kaggle.com/drscarlat/mimic2-original-icu) 
 - How to use LogFiBER model to measure semantic textual similarity.
## LogFiBER Model
 - [ ] Download LogFiBER Model from [Here](https://www.dropbox.com/s/mzkhns1e7qkh7mf/LogFiBER.zip?dl=1)
 - [ ] Extract the zip file
 - [ ] Create a python file in the same directory
 - [ ] Execute the sample code for measuring semantic similarity

       !pip install -U sentence-transformers
       from sentence_transformers import SentenceTransformer, util
       model = SentenceTransformer('./LogFiBER/') #LogFiBER is the directory.
       sentence1 = ['This framework generates embeddings for sentences']
       sentence2 = ['The model encodes sentences']
       embeddings1 = model.encode(sentence1)
       embeddings2 = model.encode(sentence2)
       cosine_scores = util.pytorch_cos_sim(embeddings1, embeddings2)
       print(cosine_scores)
   
    
