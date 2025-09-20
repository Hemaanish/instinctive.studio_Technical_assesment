# instinctive.studio_Technical_assesment

install below softwares 

a) we need to install langchain

b) we need to install supporting softwares

practical step : pip install pypdf---load pdf
                
                 pip install langchain-community----split pdf

all-mpnet-base-v2 cotains rules and regulations to build the model(llm-large language model)

sentence-transformers software will use that instructions to build the model


steps:-

step 1: load pdf into documents using pypdf.
              documents=loader.load()

step 2: split documents in text splitters
             chunks=textsplitter.split_documents()

step 3: create embedding model
             model=sentenceTransformer(".../all-mpnet-base-v2")

step 4: create vectior bd(faiss db)
              vector_store=faiss("model name,vector size,where to store hard disk or ram,for indexing)

step 5: add [or] store documnets to vector database
               vector_store.add_documents(chunks)

step 6: ask question to vector db and get relevant chunks
               context=vector_store.similarity_search("ceo?",k=1)

step 7: go to open ai ,register,get your secret_key
step 8: make a prompt with [context+question]
step 9: pass prompt+secret_key ----to ----> open AI,get answer.


we can run by keeping cursor on current cell then click on run button
