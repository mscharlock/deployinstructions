# Deploy Instructions
How to deploy on heroku 

# Git Hub setup
- On GH, create repo from front end
- On GH, create repo for back end
**Don't be like Scott and push up your .envs or node_modules**

# Front End
- Add script in package.json
  -"heroku-postbuild": "webpack -p --progress"
- In package.json, change "main" to point to "server.js"
- Add server.js file to your front end folder
  - Look at Scott's repo for what you need to type into that file
- NPM i express
- Change API_URI in your settings to 

