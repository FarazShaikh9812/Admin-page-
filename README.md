# Getting Started with Create React App

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## Available Scripts

In the project directory, you can run:

### `yarn start`

Runs the app in the development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in the browser.

The page will reload if you make edits.\
You will also see any lint errors in the console.

### `yarn test`

Launches the test runner in the interactive watch mode.\
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

### `yarn build`

Builds the app for production to the `build` folder.\
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.\
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.

### `yarn eject`

**Note: this is a one-way operation. Once you `eject`, you can’t go back!**

If you aren’t satisfied with the build tool and configuration choices, you can `eject` at any time. This command will remove the single build dependency from your project.

Instead, it will copy all the configuration files and the transitive dependencies (webpack, Babel, ESLint, etc) right into your project so you have full control over them. All of the commands except `eject` will still work, but they will point to the copied scripts so you can tweak them. At this point you’re on your own.

You don’t have to ever use `eject`. The curated feature set is suitable for small and middle deployments, and you shouldn’t feel obligated to use this feature. However we understand that this tool wouldn’t be useful if you couldn’t customize it when you are ready for it.

## Learn More

You can learn more in the [Create React App documentation](https://facebook.github.io/create-react-app/docs/getting-started).

To learn React, check out the [React documentation](https://reactjs.org/).

### Code Splitting

This section has moved here: [https://facebook.github.io/create-react-app/docs/code-splitting](https://facebook.github.io/create-react-app/docs/code-splitting)

### Analyzing the Bundle Size

This section has moved here: [https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size](https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size)

### Making a Progressive Web App

This section has moved here: [https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app](https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app)

### Advanced Configuration

This section has moved here: [https://facebook.github.io/create-react-app/docs/advanced-configuration](https://facebook.github.io/create-react-app/docs/advanced-configuration)

### Deployment

This section has moved here: [https://facebook.github.io/create-react-app/docs/deployment](https://facebook.github.io/create-react-app/docs/deployment)

### `yarn build` fails to minify

This section has moved here: [https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify](https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify)




code resolve:

1)  npx yarn-audit-fix

2)  "start": "react-scripts start"
to

"start": "react-scripts --openssl-legacy-provider start"

3) The error you're encountering is related to the use of JSX in your Home.jsx file. JSX (JavaScript XML) is a syntax extension for JavaScript that looks similar to XML or HTML but works with React to describe what the UI should look like.

The specific error messages indicate that the React variable is not in scope when using JSX. To resolve this issue, you need to make sure that you have React imported at the top of your Home.jsx file.

Here's an example of how you can import React in your Home.jsx file:

jsx
Copy code
import React from 'react';

// Your component code here

// For example:
const Home = () => {
  return (
    <div>
      <h1>Hello, World!</h1>
    </div>
  );
};

export default Home;
Make sure that you have the import statement at the top of your file, and it should resolve the "React must be in scope when using JSX" error.

If you have already imported React and the issue persists, please check for typos in the import statement or provide additional information about the structure of your Home.jsx file for further assistance.

4)rmdir /s /q node_modules    # On Windows
rm -rf node_modules         # On Unix-based systems
del yarn.lock               # On Windows
rm yarn.lock                # On Unix-based systems
yarn install
yarn cache clean
del yarn.lock               # On Windows
rm yarn.lock                # On Unix-based systems
rmdir /s /q node_modules    # On Windows
rm -rf node_modules         # On Unix-based systems