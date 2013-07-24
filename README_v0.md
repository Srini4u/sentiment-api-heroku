## Sentiment API Example

This is a very basic API that returns the sentiment value of a word or a sentence. You can define the sentiment value of any additional word that is not in the dictionary.

The original sentiment values are taken from the dataset AFINN-111.txt from [Technical University of Denmark](http://www2.imm.dtu.dk/pubdb/views/publication_details.php?id=6010) 

## Version 0 

This is version 0. See the full version lists [here](https://github.com/3scale/sentiment-api-example/blob/master/README.md).

## Usage

Start the API...

	ruby ./sentiment-api.rb 8080

Call one method of the API with curl (or with your browser if you want)

	curl -X GET -g "http://localhost:8080/v1/words/fantastic.json

The above call returns 

	{"word":"fantastic","sentiment":4}






