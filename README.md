[![CodeQL](https://github.com/imagineai/create-node-app/actions/workflows/codeql-analysis.yml/badge.svg)](https://github.com/imagineai/create-node-app/actions/workflows/codeql-analysis.yml)

<h1> Create Node App 💛 </h1>

Easy **one-line command** to create a Node app with all the **dependencies auto-installed**, and **built-in support (alpha release) for**:
  - connecting to different databases (**MySQL, PostgreSQL, SQLite3**)
  - data model creation
  - CRUD API creation (**REST, GraphQL**)
  - unit tests and test coverage reporting
  - autogenerated test factories
  - linting and code formatting (**eslint, prettier**)
  - autogenerated API documentation (**Swagger, ReDoc**)

<br/>

<h2> Overview </h2>

- **Run the following command** to create your new Node app:
```
npm install -g imagine && imagine create -f node -n myapp 
```
If you don't have `npm` installed, you'll need to [install this first](https://docs.npmjs.com/cli/v7/commands/npm-install).

<br/>

- You should see this:

```
$ npm install -g imagine && imagine create -f node -n myapp 

changed 214 packages, and audited 215 packages in 5s
....
found 0 vulnerabilities
32 files written
You have successfully created a new project!
Now you can run "cd myapp && imagine run" to install the dependencies and open a web server running at
http://127.0.0.1:8000/
```
<br/>

- Run `cd myapp && imagine run` to run your new Node app, and open http://127.0.0.1:8000/ to see that the install worked successfully.

- **Congrats! Your Node app is up and running!**

- Now that you've created your new app, **check out the `myapp.im` in your app directory** - using this you can: 
  - easily change your app settings such as Node server, package manager, API format, database etc.
  - generate code for data models, CRUD APIs etc using our simple config spec. 

- Continue reading to learn more, or check out www.imagine.ai.

</br>
<h2> Learn more </h2>

<h3> Easy to create </h3>

- Our one-line command allows your to get started with your Node app immediately, without worrying about installing dependencies - we take care of those, so you can focusing on writing business logic. 


- Our default settings when we create your Node app are as follows: 
  - API format:             REST
  - Database:               sqlite3
  - Database name:          myapp-db

- These aren't the exact settings you want? No sweat, you can always change the settings as per your preferences - read on to see how to do this.

<br/>

<h3> Easy to customize </h3>

- If you want to change any of the above defaults for your app, its a piece of cake.

- Go to the myapp.im file in your directory, your should see the basic default settings here:

</br>

```
settings

app:
    # your application name
    name: myapp
    # choose one: [django, node]
    framework: node

api:
    # choose one: [rest, graphql]
    format: rest

end settings

# database <database-name> <database type: [sqlite, mysql, posgresql]>
database myapp-db sqlite3

```
  
- You can replace the default settings with your preferences (based on the options allowed), and then run `imagine compile myapp.im` in your terminal. Your app will be updated with the new settings.


<br/>

<h3> Easy to add app functionality </h3>

- Not only can you change your app settings easily, you can also generated production-ready code using the `myapp.im` file. 


- Use Imagine's simple syntax to generate code for [data models](https://www.imagine.ai/docs/model) and [CRUD APIs](https://www.imagine.ai/docs/api) to your Node app. 


- Run `imagine compile myapp.im` to see the generated code.

- PS - all our generated code has:
  - unit tests and test coverage reporting
  - autogenerated test factories (using FactoryBoy)
  - linting and code formatting (you can select autopep8 or isort)
  - autogenerated API documentation (using Swagger and ReDoc)

- PPS - in this repository, we have included an example to-do app that we created and generated using the `todoapp.im` file. You can check out the `todoapp.im` file that we used to create the Node app and express the specifications for the data models and APIs, as well as all the Node code files that are generated when you run `imagine compile todoapp.im`.

- Have fun! 💛
