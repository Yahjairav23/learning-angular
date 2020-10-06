# My First Angular App

In this project we will be learning how to build projects using angular.

## Notes
- Imports are placed in the app.module.ts file
- The index.html file is the file that our application loads.
- in app.component.ts we have a selector and this allows us to set a name to our app.component
    - the app component is broken down to a css file, html file, spec file, and a typescript file.
    - the html file gets rendered
- The first code that will get executed when we run our app will be the main.ts file and that will direct the app to the app.module.ts file where bootstrap is made aware of all the components(bootstrap: [])
- app.component will be our root component that we ap our other components to.

- conventions when creating a new component
    - create a folder within your app folder with the name of your component
    - inside component folder you will place all of your different component files
    - your component files should be name: filename.component.filetype
    - must import Component decorator in your filename.component.ts file
        import { Component } from '@angular/core'
        @Component({
            selector: 'given-name',
            templateUrl: 'htmlfile-location',
            styleUrls: ['an array pointing to the style sheet/s']
        })
        - a component must at least have a template

Decorators - TypeScript feature that allows your to enhance your classes and elements

- modules bundle different components from your app into packages

- angular will not scan all files, hence why we must make it aware of any files that may need to be read in @ngModule
    - we can do this by adding the component selector name to the declarations in the @ngModule decorator in the app.module.ts file
    - we will also need to import the file (we don't need to include file type when writing the location of the component import)

you can use your component selector name as an html tag to call the component within a different component 

- you can create a new component in the cli like so:
    ng generate component componentName
    - this creates a new folder with your component files
    - this will also automatically import your component to the declarations and import the file to app.module.ts file.
