### MEVN Template

#### Server: [MEVN-CLI](https://github.com/danialhasan/mevn-cli)

#### Client: [Vite](https://github.com/web2033/vite-vue3-tailwind-starter)

[This article](https://dev.to/stlnick/how-to-deploy-a-full-stack-mern-app-with-heroku-netlify-ncb) is a guide to deploying apps like this. 
However, in order to start builds/deploys on **both** netlify _and_ heroku with just one `commit`, you have to `enable automatic deploys` in Heroku's deploy settings and set up [this buildpack](https://github.com/timanovsky/subdir-heroku-buildpack) (before the _heroku/nodejs_ buildpack) alongside the setup that comes with it, detailed [here.](https://medium.com/@timanovsky/heroku-buildpack-to-support-deployment-from-subdirectory-e743c2c838dd) For Netlify, you must specify your base directory (client) and your _npm run build_ command. 
