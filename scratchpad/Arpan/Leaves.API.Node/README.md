# Leaves.API.Node

This is a demo project used for connecting a REST API to a DataStax Astra Database

## Set up

Complete the following steps to start a new project (NEW-PROJECT-NAME):

1. Clone this repository to your local machine `git clone LEAVES.API.NODE-URL NEW-PROJECTS-NAME`
2. `cd` into the cloned repository
3. (**IGNORE IF TEAM MEMBER**) Make a fresh start of the git history for this project with `rm -rf .git && git init`
4. Install the node dependencies `npm install`
5. Move the example Environment file to `.env` that will be ignored by git and read by the express server `mv example.env .env`
6. Edit the contents of the `package.json` to use NEW-PROJECT-NAME instead of `"name": "Leaves.API.Node",`

## Scripts

**Before starting application**

* Set BUNDLE in .env equal to Astra Secure Connect Bundle .zip file name 

* Set USER and PASS equal to Astra Credentials

```
NODE_ENV=development
PORT=8000
EXAMPLE="example-environmental-variable"
BUNDLE=secure-connect-example.zip
USER="Example"
PASS="Example"
```

Start the application `npm start`

Start nodemon for the application `npm run dev`

(**WORK IN PROGRESS**) Run the tests `npm test`

~~## Deploying~~

~~When your new project is ready for deployment, add a new Heroku application with `heroku create`. This will make a new git remote called "heroku" and you can then `npm run deploy` which will push to this remote's master branch.~~

## Endpoints (thus far / subject to change)

* `/api/leaves`
    * `GET` -> (**WORKING + TESTED**) Returns items from the KEYSPACE.leaves table
    * `POST` -> (**TBD AND UNTESTED TO LEAVES DB**) Creates a new item in the KEYSPACE.leaves table

* `/api/leaves/:id`
    * `GET` -> (**WORKING + TESTED**) Returns single item based on id parameter from KEYSPACE.leaves table
    * `PATCH` -> (**TBD AND UNTESTED TO LEAVES DB**) Updates an item in KEYSPACE.leaves table based on id parameter and request body
    * `Delete` -> (**UNTESTED TO LEAVES DB**) Deletes an item in KEYSPACE.leaves table based on id parameter