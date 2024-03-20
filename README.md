# recipe-rag
Find recipe that suits your needs. Built on top of Gemma-2B with RAG hosted on MongoDB. Made using the first 1k recipe from the [recipe-nlg](https://huggingface.co/datasets/recipe_nlg) dataset.

## How to replicate
- The notebook was developed on Google Colab, but can be adapted for use in other environments.
- Create `MONGO_URI` and `HF_TOKEN` environment values / secrets for your MongoDB database and Hugging Face account respectively.
- Create a MongoDB collection for hosting the embeddings and assign a vector search index using the [guide](https://www.mongodb.com/docs/atlas/atlas-vector-search/tutorials/reciprocal-rank-fusion/#define-the-atlas-vector-search-index.-1), while setting `path` as "embedding", `similarity` as "cosine" and `numDimensions` as 1024 to match the embedding model.
- In a GPU environment, run the notebook and follow instructions.

## TODO
- Enrich response with the matched recipe.
- Create a simple chat interface.

## Reference
- Inspired by a Hugging Face [cookbook](https://github.com/huggingface/cookbook/blob/main/notebooks/en/rag_with_hugging_face_gemma_mongodb.ipynb).
