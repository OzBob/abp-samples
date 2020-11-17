# BookStore

This is a startup project based on the ABP framework. For more information, visit <a href="https://abp.io/" target="_blank">abp.io</a>

## Run the app:
Install  mongodb
Change .\BookStore-Angular-MongoDb\aspnet-core\src\Acme.BookStore.HttpApi.Host\appsettings.json "ConnectionStrings.Default to have the correct value: e.g. mongodb://localhost:27017/BookStore
install easy-rsa etc. as per: https://www.percona.com/blog/2019/10/28/setting-up-mongodb-with-member-x509-auth-and-ssl-easy-rsa/
.. TODO provide instructions on connecting to mongodb using cert ".\aspnet-core\src\Acme.BookStore.HttpApi.Host\tempkey.rsa" and provide values for "aspnet-core\src\Acme.BookStore.DbMigrator\tempkey.rsa"
Open console
Run 'dotnet --list-sdks'
Pick highest and update global.json or install the version mentioned in global.json
Save global.json
Open .\aspnet-core\Acme.BookStore.sln in VS
Set Acme.BookStore.HttpApi.Host as the Startup Project
From command prompt, run `yarn start` for a dev server.
From Visual studio Debug/f5 app
VS will open `http://localhost:4200/`. 

## Development server

Run `ng serve` for a dev server. Navigate to `http://localhost:4200/`. The app will automatically reload if you change any of the source files.

## Code scaffolding

Run `ng generate component component-name` to generate a new component. You can also use `ng generate directive|pipe|service|class|guard|interface|enum|module`.

## Build

Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory. Use the `--prod` flag for a production build.

## Running unit tests

Run `ng test` to execute the unit tests via [Karma](https://karma-runner.github.io).

## Running end-to-end tests

Run `ng e2e` to execute the end-to-end tests via [Protractor](http://www.protractortest.org/).

## Further help

To get more help on the Angular CLI use `ng help` or go check out the [Angular CLI README](https://github.com/angular/angular-cli/blob/master/README.md).
