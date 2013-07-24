# Sentiment API Example

This is a very basic API that returns the sentiment value of a word or a sentence. You can define the sentiment value of any additional word that is not in the dictionary.

The API is meant to serve an example of how you can easily create an API, and how you can use the free 3scale platform to control, manage and monitor the operations of the API so that you only have to do the fun part.

The original sentiment values are taken from the dataset AFINN-111.txt from [Technical University of Denmark](http://www2.imm.dtu.dk/pubdb/views/publication_details.php?id=6010) 

## Versions 

See the full version list of this API [here](https://github.com/3scale/sentiment-api-example/blob/master/README.md).

## Usage

Start the API...

	ruby ./sentiment-api.rb 8080

Call one method of the API with curl (or with your browser if you want)

	curl -X GET -g "http://localhost:8080/words/fantastic.json

The above call returns 

	{"word":"fantastic","sentiment":4}

## Deploying the API to Heroku

Before deploying your application, you must have installed the Heroku
toolbelt and be already logged in to Heroku. For more help on this
process, check the guide [here](https://toolbelt.heroku.com). 

Clone this repository

  git clone https://github.com/vdel26/sentiment-api-heroku.git

From inside the repository folder that was just created, create an Heroku app

  heroku create

Check the output of that command, as it will have the URL of your
application. It will look like this: 
  
  http://random-heroku-name.herokuapp.com 

Now push the code to Heroku

  git push heroku master

That's it! Now you can call the API like you did before but using the
URL that Heroku just gave you:

	curl -X GET -g "http://random-heroku-name.herokuapp.com/words/fantastic.json
