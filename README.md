# poc-newsy-editor-viewer
Frontend SPA application in vue.js 2.6 using the bootstrap-vue for UI. This application is a frontend for web API at https://github.com/igolovic/poc-newsy.   
   
## Functionality
Used for viewing and adding articles.   
      
## Architecture
Application is a SPA multi-component application implemented and structured according to Vue.js CLI using the Vue.js framework.   
   
## Prerequisites
Vue.js 2.6 CLI   
Bootstrap-vue 2.22.0   
poc-newsy web API running on https://localhost:5001 (Docker)    
poc-newsy IdentityServer4 running on https://host.docker.internal:44343 (Docker)    
pg4admin PostgreSQL UI running on http://localhost:5050/browser/ (Docker)    
PostgreSQL RDBMS running and containing the expected database (Docker)    
    
## Components
poc-newsy-editor-viewer frontend web application running on https://localhost:8080/    

## Development tools
Visual Studio Code   
      
## Operation
Run the application using the "run npm serve" in VS Code to connect to the web applications in Docker container (https://github.com/igolovic/poc-newsy/blob/master/README.md).   
Add articles by selecting users/authors (one article can have multiple authors) and by entering plain text or HTML as article content.   
   
## Authentication and authorization
These services are provided for the frontend client application by the npm package oidc-client which implements IdentityServer4/OpenID-Connect.    
User cannot use poc-newsy-editor-viewer before successful login which is provided by the IdentityServer4 custom server application on https://host.docker.internal:44343.    
Web API is protected by the same IdentityServer4 custom server application and cannot be accessed before login.    
   
## Installation
In VS Code get required npm modules and run the frontend application using the npm serve on URL http://localhost:8080/    
    
## ToDo
- HTML editor for editing article instead of textarea    
- full CRUD controls for articles   
- full CRUD controls for users   
