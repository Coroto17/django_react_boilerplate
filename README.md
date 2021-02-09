# Frontend and Backend core for a Django-React app.

## Frontend create-react-app

I'm gonna leave the original create-react-app README for future references.

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

## Backend Django.

Steps to prepare the backend:

* Clone this repo: `git clone https://github.com/Coroto17/django_react_boilerplate.git`
* Change directory to the repo folder.
* Make a virtual env: `python3 -m pip venv venv`
* Activate the venv `. venv/bin/activate`
* **Important:** Always check and upgrade pip inside your venv before installing anything there `pip install --upgrade pip`
* Install packages `pip install -r requirements.py`
* Make migrations: `python manage.py makemigrations`
* Migrate: `python manage.py migrate`

At this point you can start creating your custom models, serializers, and so on.

### Useful links.

If you want to understand what's going on, particulary with the web API, [check out the DRF documentation](https://www.django-rest-framework.org/). You can find here how to set token authentication, setting up serializers, manage permissions and authentication, and so on.

Check [dj-rest-auth](https://dj-rest-auth.readthedocs.io/en/latest/index.html) to know how to transform users registration and authentication into API endpoints.

Serving static files in development and production with whitenoise [Check docs](http://whitenoise.evans.io/en/stable/index.html)

## CREATE YOU .ENV FILE.

For the project to work, you should make a .env file in the root folder, containing your needed env variables. In my case, i needed to change react app port and browser, and set the SECRET_KEY for the backend. So i ended up creating a .env file with content like this:
```
PORT=3033
BROWSER="/mnt/c/Program Files (x86)/Google/Chrome Dev/Application/chrome.exe"
SECRET_KEY="bdi@8sjhg&tvo!4e%yz!b_7@%x_-uyyiq4*cq_l1t8c"
```
The SECRET_KEY is some random string inside quotes...

Then, you include these env vars in you current environment by running the command (linux) `source .env`.  
You can check if these env vars are included in your current environment by calling them, e.g if you want to see the PORT: `echo $PORT`

