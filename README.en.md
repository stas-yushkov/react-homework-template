**Read in other languages: [Українська](README.md), [Polska](README.pl.md), [English](README.en.md), [Española](README.es.md), [Русский](README.ru.md).**

# React homework template

This project was created with
[Create React App](https://github.com/facebook/create-react-app). 
To get acquainted and configure additional features
[refer to documentation](https://facebook.github.io/create-react-app/docs/getting-started).

## Preparing a new project

1. Make sure you have an LTS version of Node.js installed on your computer.
   [Download and install](https://nodejs.org/en/) if needed.
2. Clone this repository.
3. Change the folder name from `react-homework-template` to the name of your project.
4. Create a new empty GitHub repository.
5. Open the project in VSCode, launch the terminal and link the project to the GitHub repository 
  [according to the instructions] (https://docs.github.com/en/get-started/getting-started-with-git/managing-remote-repositories #changing-a-remote-repositorys-url).
6. Install the project's base dependencies with the `npm install` command.
7. Start development mode by running the `npm start` command.
8. Go to [http://localhost:3000](http://localhost:3000) in your browser.
 This page will automatically reload after saving changes to the project files.

## Deploy

The production version of the project will automatically be linted, built, 
and deployed to GitHub Pages, in the `gh-pages` branch, every time the `main` 
branch is updated. For example, after a direct push or an accepted pull request. 
To do this, you need to edit the `homepage` field in the `package.json` file, 
replacing `your_username` and `your_repo_name` with your own, and submit the 
changes to GitHub.

```json
"homepage": "https://your_username.github.io/your_repo_name/"
```

Next, you need to go to the settings of the GitHub repository (`Settings` > `Pages`) 
and set the distribution of the production version of files from the `/root` 
folder of the `gh-pages` branch, if this was not done automatically.

![GitHub Pages settings](./assets/repo-settings.png)

### Deployment status

The deployment status of the latest commit is displayed with an icon next to its ID.

- **Yellow color** - the project is being built and deployed.
- **Green color** - deployment completed successfully.
- **Red color** - an error occurred during linting, build or deployment.

More detailed information about the status can be viewed by clicking on the icon, 
and in the drop-down window, follow the link `Details`.

![Deployment status](./assets/status.png)

### Live page
After some time, usually a couple of minutes, the live page can be viewed at the address 
specified in the edited `homepage` property. For example, here is a link to a live version for this repository
[https://goitacademy.github.io/react-homework-template](https://goitacademy.github.io/react-homework-template).

If a blank page opens, make sure there are no errors in the `Console` tab related 
to incorrect paths to the CSS and JS files of the project (**404**). You most likely 
have the wrong value for the `homepage` property in the `package.json` file.

### Routing
If your application uses the `react-router-dom` library for routing, you must 
additionally configure the `<BrowserRouter>` component by passing the exact name 
of your repository in the `basename` prop. Slashes at the beginning and end of 
the line are required.

```jsx
<BrowserRouter basename="/your_repo_name/">
  <App />
</BrowserRouter>
```

## How it works

![How it works](./assets/how-it-works.png)

1. After each push to the `main` branch of the GitHub repository, a special script 
  (GitHub Action) is launched from the `.github/workflows/deploy.yml` file.
2. All repository files are copied to the server, where the project is initialized 
  and linted and built before deployment.
3. If all steps are successful, the built production version of the project files is 
  sent to the `gh-pages` branch. Otherwise, the script execution log will indicate 
  what the problem is.
