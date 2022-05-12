# poc-newsy-editor-viewer
Simple frontend SPA application in vue.js 2.6 using the bootstrap-vue for UI. Used for viewing and adding articles, this application is a frontend for web API at https://github.com/igolovic/poc-newsy   
   
**Functionality implemented in web API**
   
**Prerequisites**  
vue.js 2.6   
bootstrap-vue 2.22.0   
poc-newsy web API on https://localhost:5001/swagger/index.html (CORS in web API was set up to allow this hostname and port), PostgreSQL database (part of newsy-poc installation)   
   
**Development tools**   
Visual Studio Code   
      
**Operation**   
Run the application using the "run npm serve", add articles by entering plain text or HTML and selecting users/authors (one article can have multiple authors).   
   
**Authentication and authorization**   
They are provided for the Vue.js frontend client application by the npm package oidc-client which implements IdentityServer4/OpenID-Connect. User cannot use SPA application before successful login in a form provided by the IdentityServer4 custom server application on https://host.docker.internal:44343. API itself is protected by the same IdentityServer4 custom server application and cannot be accessed before login.
   
**Architecture**   
Applicaiton is a SPA multi-component application followingn organization layed out by the Vue.js CLI.

**Installation**   
- In VS Code get required modules and run using the npm serve on URL http://localhost:8080/

**TODO**   
- HTML editor for editing article instead of textarea    
- full CRUD controls for articles   
- full CRUD controls for users   
