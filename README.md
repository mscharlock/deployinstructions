# Deploy Instructions
How to deploy on heroku 

![Deploy](https://media.giphy.com/media/l0HlK4xG1fTszmFS8/giphy.gif)

# Git Hub setup
**Don't be like Scott and push up your .envs or node_modules**
- On GH, create repo from front end
- On GH, create repo for back end

# Back End
**In heroku:**
- Hook up mLabs (find this in Resources tab, choose the Sandbox option) 
- Navigate to config vars (in Settings tab) 
- Copy the MONGODB_URI url that is created by mLabs and paste this into another config var, which you will call MONGO_URI
- Add all your other config vars from your env file on the backend, including SECRET, AWS_BUCKET, AWS other keys, CORS_ORIGINS. You don't need PORT.
- Set API_URL var and CORS_ORIGINS to the url of the front end (do not include the trailing slash) 
- Deploy master branch

# Front End
- Add script in package.json
  -"heroku-postbuild": "webpack -p --progress"
- In package.json, change "main" to point to "server.js"
- Add server.js file to your front end folder
  - Look at Scott's repo for what you need to type into that file
- NPM i express
- ACP
- **In heroku:** In frontend config vars (in Settings tab), add API_URI and set it to the url of the backend (do not include a final / on the url) 
- Deploy master branch

