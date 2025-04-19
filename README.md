# RAG-Chatbot

At Outlier.ai, we have an existing chatbot system where users can upload Pdf documents and then write their query. Here LLM will take all the information provided and will generate a response. 

LLM has a limited context window so it is not scalable to give too many Pdf documents/large documents to it.

So, we are experimenting with the RAG approach. RAG retrieves only the most contextually relevant information from pdf documents and gives it to LLM with the user query so it can  generate a response. We are evaluating whether using RAG we can reach at par performance compared to existing chatbot


What is a RAG?

RAG is Retrieval Augmented Generation.                                                                              
It consists of two main components: Retrieval and Augmented Generation.
Retrieval:
When a user submits a query, the retrieval system searches a knowledge base for the most relevant text chunks.
The knowledge base is typically structured as a vector database, where text chunks are stored as embeddings (numerical representations).
The retrieval system uses semantic search( using similarity search algorithms) to fetch the most relevant information.
Augmented Generation:
The retrieved text chunks are combined with the user query and passed to the LLM.
Then LLM generates a response.



Knowledge Base Structure:
The knowledge base consists of text chunks, which are smaller pieces of structured or unstructured data.
These chunks are indexed and retrieved efficiently based on semantic similarity.
The retrieval method could involve vector search



Project Highlights:
I developed an end-to-end text chunking and indexing pipeline using pdfminer, which allowed the chatbot to analyze both text and image-based content within PDFs.
Implemented a hybrid search strategy with Elasticsearch, combining BM25 and KNN techniques to improve the relevance of retrieved context.
Evaluated the chatbot's performance using factual correctness metrics, including G-Eval Correctness, Precision, and Recall, achieving an average correctness of 79%, which marked a 3% improvement over the previous model.
Technologies Used:
Programming & Frameworks: Python, GPT-4o-mini, Elasticsearch
Data Processing: pdfminer, Pandas
Evaluation: Custom metrics for factual correctness and answer relevancy
Impact:
This project not only enhanced the chatbot's accuracy and reliability but also strengthened my expertise in natural language processing, data preprocessing, and model evaluation. It was a rewarding experience that demonstrated my ability to apply AI techniques to solve real-world challenges effectively.
