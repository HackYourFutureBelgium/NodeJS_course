0. Clean code
1. Deployment
2. How to save a password, login and tokens
3. Other small stuff
---
How to deploy a website?
---
1. Set up a branch pipeline
2. Make your project production ready
3. Deploy your master app to Heroku
4. Deploy your dev app to Heroku
5. (Add process env variables)
---
## Initiate branch pipeline
1. replace port inside index.js with `const PORT = process.env.PORT || 8000;`
2. Create a dev branch
3. You do new development on the dev branch
4. The master branch will be the live version
5. For now switch to the *master* branch
---
## Make your project production ready
1. Compress the HTTP response with [Compression middleware](https://www.npmjs.com/package/compression)
2. Protect against well known vulnerabilities with [Helmet middleware](https://www.npmjs.com/package/helmet)
3. Set the environment to production by adding `NODE_ENV=production` to the start command inside package.json
4. Replace at the same place `nodemon` with `node`
---
## Deploy your **master** branch to Heroku
1. Initiate your project as a GitHub repository
2. [Sign up for Heroku](https://signup.heroku.com/?c=70130000001x9jFAAQ)
3. Setup a new app
4. Deploy with your Github repository with master branch
5. Enable automatic deploys
---
## Deploy your **dev** branch to Heroku
1. **Don't** do any production setup
2. Deploy with your Github repository with dev branch
3. Enable automatic deploys
4. Make changes on the dev branch, test them on the domain
5. Test okay? Merge with master
---
## Making use of process env variables
1. Go to heroku app settings
2. Reveal config vars
3. Add `databasePassword` as key and `siuhUBG93p` as value
4. Add `databaseUser` as key and `sql7253327` as value
5. Use `process.env.<varName>` in the Database config
---
How to save a password, login and tokens?
---













What we didn’t cover => Making an app for the terminal, email sending, GraphQL, testing (continuous integration), scraping…
Service providers to make life easier => AWS S3, Postmark…
What does it mean to be a backend developer?
