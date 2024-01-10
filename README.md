# ReactDeploymentTest
 
Not much to see here, I just wanted to learn how to deploy React apps to github pages :D 

1. Create a new repository on GitHub and name it after your project.
2. Install `create-react-app` package by running `npx create-react-app <project-name>` in the terminal.
3. Navigate to the root directory of your project and run `npm run build` to create a production build of your app.
4. Install the `gh-pages` package by running `npm install gh-pages --save-dev`.
5. In the `package.json` file, add the following lines of code to the top-level object:

```
"homepage": "https://<username>.github.io/<project-name>",
"scripts": {
  "predeploy": "npm run build",
  "deploy": "gh-pages -d build"
}
```

6. Replace `<username>` with your GitHub username and `<project-name>` with the name of your project.
7. Run `npm run deploy` in the terminal to deploy your app to GitHub Pages.
8. Wait for a few minutes and then visit `https://<username>.github.io/<project-name>` to see your app live.

I also needed to add to .gitconfig:
```
[credential]
    helper = wincred
```
