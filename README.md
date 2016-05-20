## How to use this template?

- clone this app and name it as whatever your want:
`$ git clone https://github.com/mz026/universal-redux-template.git my-killer-app`

- remove the `.git` folder since you won't need the history of this boilerplate:
`$ cd my-killer-app; rm -rf .git`

- start out a new git history:
`$ git init`

- Install dependencies:
`$ npm install`

- Host dev environment and start to build something chaning the world!
`$ npm start`

- To run the test with Mocha, Sinon and Chai:
`$ npm test`

- To generate a container/component/action and its tests:
`$ ./bin/generate <type> <path>`

- To update [npm-shrinkwrap](https://docs.npmjs.com/cli/shrinkwrap):
`$ npm shrinkwrap --dev`

eg: `$ ./bin/generate component myNamespace/MyComponent`

## Features:
- Universal rendering, with async data support
- Server side redirect
- Separate vendor and app js files

## Stack:
- React 15.0.2
- React-Router 1.0.2
- Express as isomorphic server
- Babel
- Webpack

## Testing:
- Use Mocha, Chai as testing framework; Rewire, Sinon to mock

## Routes Draft:
- Intro page: `{base_url}`
- Question Page: `{base_url}/questions`

## Deployment:

To deploy this app to production environment:

- Prepare a server with NodeJS environment

- Use whatever tool to upload this app to server. ([Capistrano](http://capistranorb.com/) is a good choice.)

- Run `$ NODE_ENV=production npm install` on server
  - After the installation above, `postinstall` script will run automatically, building front-end related assets under `dist/` folder.

- Kick off the server with:

`$ NODE_ENV=production NODE_PATH=./app node app/server`

### Deploy to Heroku

To deploy this app to heroku,

- Set up heroku git remote url
- Set `API_BASE_URL` to heroku config var. (without trailing slash)

Here's a [sample](https://redux-template-test.herokuapp.com/) deployed to heroku: https://redux-template-test.herokuapp.com/
For this case, the `API_BASE_URL` mention above would be `https://redux-template-test.herokuapp.com`


## Resources:
- [Blogpost on Codementor](https://www.codementor.io/reactjs/tutorial/redux-server-rendering-react-router-universal-web-app)
- [Chinese version of the above](http://mz026.logdown.com/posts/308147-hello-redux-2-3-server-rendering)


