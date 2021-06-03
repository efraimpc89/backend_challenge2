# Postman + Newman - Backend - Challenge 2
The subject under test will be the Square API, more specifically the payments and refunds endpoints 
https://developer.squareup.com/reference/square/payments-api

Square APIs enable you to accept payments securely and integrate your app with Square’s first party product ecosystem.

The purpose of this repository is to test the scenarios described on the following challenge:
https://docs.google.com/document/d/19qR-7Gv8g7iae1Njo2Y3mRYgZociXqrjHjvGNgx402Y/edit?usp=sharing


## Project Structure

An NPM project that has a very simple structure:

**Collection**: this folder should contain exported postman collections.
**envVariables**: contains the environment variables in json format.
**package.json**: contains NPM's project main information such as descripction, version, scripts that can be executed and more.
```
backend_challenge2
└ API
  ├ collection
  |  └ Challenge2_EfraimPC.postman_collection.json
  | 
  ├ envVariables
  |  └ Prod.postman_environment.json
  | 
  ├ package.json
  └ README.md
```

## Pre-requisites

1. Install Node.js + npm [https://nodejs.org/en/](https://nodejs.org/en/)  
[You can follow this guide: [https://wsvincent.com/install-node-js-npm-windows/](https://wsvincent.com/install-node-js-npm-windows/)]  

2. [Installing Artillery](https://artillery.io/docs/guides/getting-started/installing-artillery.html)
3. [Install Git](https://git-scm.com/downloads)
4. [OPTIONAL] Javascript IDE:  
	   (Only if you wish to explore the code more confortable)
	- Visual Studio Code: [https://code.visualstudio.com/](https://code.visualstudio.com/)  
	- Atom: [https://ide.atom.io/](https://ide.atom.io/) 
5. [OPTIONAL] [Postman](https://www.postman.com/downloads/) 

## How to run 

1. Generate an authentication token by [signing up](https://squareup.com/login?app=developer&return_to=https://developer.squareup.com/reference/square/payments-api) on Square API's webpage and once you login go to [Obtain Token](https://developer.squareup.com/explorer/square/oauth-api/obtain-token) section and be sure to select *"Production"* from the upper middle button and then press the *"Get Token"* button and it should generate an *auth token*. 
(example: EXAMPLEpRZcFuvC2DD-ecl1t-DJXSJDI4IASTcClwRFGQ69L7YL5Of9OJrTG5oZ6r)

3. Open windows command line
4. Clone github repository: 

		 git clone https://github.com/efraimpc89/backend_challenge2.git

5. Navigate to *backend_challenge2* folder and execute one of following commands:
	
	**-To run all tests with no report generated:**

		 npm run test-all-no-report <AUTH_TOKEN>

	The results of the tests will be displayed on console.
	
	**-To run all tests and generate an html report**:

		 npm run test-all-report <AUTH_TOKEN>

	 in order to see the html report, navigate to *backend_challenge2/newman* folder and you should see all the generated reports so far, open them with any browser to view them.


*IMPORTANT NOTE: Another way to run the tests its to import the collection and environment variables directly to postman but the point of this repository is to run them directly from console.*

## Contact

If you have any questions, feel free to send me an email:
efraimpc89@gmail.com

```