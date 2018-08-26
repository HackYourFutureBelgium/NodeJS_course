0. Clean code
1. Deployment
2. How to save a password and login?
3. Other small stuff
---
## Clean code tips
- Indentation!
- Be consistent in naming things and use conventions
- Use small, one purpose functions (max 20/25 lines)
- Name functions to what they do
- Keep your classes small (max 300/400 lines)
- Write code in a way that it's explains itself
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
2. Deploy to new Heroku app with your Github repository using the dev branch
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
How to save a password and login?
---
## How can you save a password?
password is "password123"
1. SHA256 encrypt "password123"
2. Generate a random string to use as salt
3. Salt the hash with the random string
4. Save the representation of the password and the random string
---
## How do you login with a given username/password?
Requirements:
1. You should send "login succesfull" when an existing username/password is given
2. You should send "login failed" when a wrong username/password is given
Try to figure it out yourself. First one wins a price :D
---
Service providers to make life easier
---
- AWS S3 => File storage
- Postmark => Email sending
- Onesignal => Sending push notifications
- ...
---
What we didn’t cover
---
Making an app for the terminal
---
GraphQL
---
Testing (continuous integration)
---
Web scraping and so much more
---
## What does is it take to be a web developer in 2018?
Watch this [video](https://www.youtube.com/watch?v=gVXcqO9A1vo)
