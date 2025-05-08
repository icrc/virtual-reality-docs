# VideoPath Documentation Site

A simple, searchable documentation site for the VideoPath app - built with [Docsify](https://docsify.js.org).


## Developing Locally

* Install `docsify-cli` to make viewing and developing the site locally easy:
  * `npm i docsify-cli -g`
* Run docsify locally (change the port from 5258 if you need to):
  * `docsify serve -p 5258`
* View the development site at `http://localhost:5258/`

## Building and Deployment

* No build process is required - the site can be simply copied as is. Just make sure that:
  * `baseURL` in `vp.production.js` is set to the URL of the production VideoPath site  
  * Your deployment script should copy `vp.production.js` over `vp.js` 

The site was originally deployed to GitLab. The CI config can be found in `.gitlab-ci.yml`
