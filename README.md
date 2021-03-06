# Get Pre-trained Sentence Embeddings from TensorFlow Hub
An easy script to get sentence embeddings from Google's pre-trained models on TensorFlow Hub. This script includes 6 such models of varying embedding dimensions (20-512) and/or architectures.

## Example Usage

Returns an embedding vector per sentence of the input.
```python
EMBEDDING_SIZE = n

Input = ["Colorless green ideas sleep furiously.", \
	"Noam Chomsky offered this as an example of a grammatically valid, \
	semantically nonsensical sentence."]
				
Output = array of shape (m,n) #m=number of sentences(=2), n=EMBEDDING_SIZE
``` 


## Installation and Use
Run `pip3 install -r requirements.txt`

Run `python3 get_embeddings.py`

## Can't find the embedding dimension/model you need?
Add the required model's URL [available here](https://tfhub.dev/s?module-type=text-embedding&subtype=module,placeholder) to **[dictionary here.](https://github.com/saranya132/pretrained_sent_embeddings/blob/832e609920d58e614a5342221d0406bd6995dc0e/get_embeddings.py#L13-L21)**

### Note 
1. Create a **key** for new dictionary **values (URLs)** with the format "embed_**_size/modelName_**_model_url".
2. Pass **_size/modelName_** as EMBEDDING_SIZE.

### Credits
All the models used (and more) are available [here on TensorFlow Hub.](https://tfhub.dev/s?module-type=text-embedding&subtype=module,placeholder)
