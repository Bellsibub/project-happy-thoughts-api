# Happy Thinking API

**Mission:** 

*Create a an API for the Front End project Happy Thinking*

**Requirements:**
- 🔵 COMPLETE (all)
- 🔴 COMPLETE (all)
- ⚫ NONE


***

## Installation

Navigate to the project folder and run the following command

```
$ npm install
```

**To test the local database on a public environment (i.e. get public error messages)**

```
$ npm run testENV
```
**To start development environment**

```
$ npm run dev
```
<br>

## ✅ Features ✅
***


> 💡 SEE OFFICIAL DOCS FOR MORE INFO: https://documenter.getpostman.com/view/8159541/TzRa7PkV


*The following are the main features of this application:*
  * The API has the following endpoints:
    * `/thoughts`
      * Method: GET
        * Returns a list of the latest 20 thoughts posted
      * Method: POST
        * Body => `message`(required),`name`,`category`
        * returns the created thought object 
    * `/thoughts/:id/like`
      * Method: POST
        * Increments the heart rating on the requested thought

<br>

## 💭 Reflections 💭
***
I enjoyed this project a lot! It was fun switching between FrontEnd and BackEnd. Eventually I came up with a system of work that streamlined everything. I decided to have two VSCode sessions open (one for each environment) and then I first made changes to the API, then switched to the FrontEnd to implement some features that dispaly the new API changes. So overall this project was smooth and simple.

<br>

Issues that came up:
- I did struggle just a bit with getting my dev environment setup like I wanted. MongoDB Compass was struggling a bit to relay the correct error messages I needed to solve my issues. But thankfully Google is a dear friend 😻. I found out that since I setup using dotenv and made a dynamic switch of MONGO_URL depending on NODE_ENV, I had forgotten to setup switching NODE_ENV on npm scripts.
  
  So therefore I fixed it by chaning the npm scripts:
  ```json
  "dev": "set NODE_ENV=development&&nodemon server.js --exec babel-node"
  ```
  
  So whenever running the dev script I will always use the development environment. I honestly thought that running the dev script would automatically set it to `NODE_ENV=development`, but apperently not... 🤔

If I were to continue on this project / start over I would:
- Add sorting and pagination options

<br>

***

## Try it live
Link to published API: https://happy-thinking.herokuapp.com

Link to API docs: https://documenter.getpostman.com/view/8159541/TzRa7PkV

Link to Front End: https://happythinking.netlify.app/