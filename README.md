# BookStore

This is a startup project based on the ABP framework. For more information, visit <a href="https://abp.io/" target="_blank">abp.io</a>

## Build

Run `yarn` to get packages

Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory. Use the `--prod` flag for a production build.

## Development server
 - install  mongodb: get a new Atlas account and create a cloud based DB
 - Update the ConnectionStrings.Default value in :
 - change .\BookStore-Angular-MongoDb\aspnet-core\src\Acme.BookStore.HttpApi.Host\appsettings.json
 
 and
 - change .\BookStore-Angular-MongoDb\aspnet-core\src\Acme.BookStore.DbMigrator\appsettings.json
 -   update the connection string value to as indicated on https://cloud.mongodb.com/ Cluster | Connect | Application. Similar to:
 -   "mongodb+srv://{username}:{password}@{hostcluster}.mongodb.net/BookStore?ssl=true&replicaSet={replicaset}&authSource=admin&retryWrites=true&w=majority"
 -   and note never to check in the code to github with your password
 
  OR
 -   install mongodb locally
 -   and connect using local certs or local username/password
 -   install easy-rsa etc. as per: https://www.percona.com/blog/2019/10/28/setting-up-mongodb-with-member-x509-auth-and-ssl-easy-rsa/
 - Open ..\..\global.json
 - Open console
 - Run 'dotnet --list-sdks'
 - Pick highest and update global.json or install the version mentioned in global.json
 - Open ..\aspnet-core\Acme.BookStore.sln in VS
 - Set Acme.BookStore.HttpApi.Host as the Startup Project
 - To initialise your database:
  - cd .\BookStore-Angular-MongoDb\aspnet-core\src\Acme.BookStore.DbMigrator\
  - dotnet run Acme.BookStore.DbMigrator.csproj
  - open .\BookStore-Angular-MongoDb\aspnet-core\src\Acme.BookStore.Domain\Data\BookStoreDbMigrationService.cs
  - Comment out line 40 //await MigrateDatabaseSchemaAsync();, as there is a mongo error "pending collection catalog changes" 
 - To seed the data run:
 -  dotnet run Acme.BookStore.DbMigrator.csproj

 - From Visual studio
 -  Open Developer Command prompt
 -  Run:
 -  Yarn
 -  Gulp
 -  Close the developer command prompt
 -  Debug (press f5)
 -  VS will open `http://localhost:44308`. 


  From commandline, open:
 - $\abp-samples\BookStore-Angular-MongoDb\angular
 
 run 
 - `yarn build`
 - `yarn start`
 - Open a browser to: `http://localhost:4200/`
 - Login with admin/1q2w3E*

## Code scaffolding

Run `ng generate component component-name` to generate a new component. You can also use `ng generate directive|pipe|service|class|guard|interface|enum|module`.

## Running unit tests

Run `ng test` to execute the unit tests via [Karma](https://karma-runner.github.io).

## Running end-to-end tests

Run `ng e2e` to execute the end-to-end tests via [Protractor](http://www.protractortest.org/).

## Further help

To get more help on the Angular CLI use `ng help` or go check out the [Angular CLI README](https://github.com/angular/angular-cli/blob/master/README.md).
