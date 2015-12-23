# Golang / React template

This is a super slim starter kit for an app with a Golang backend (in the `backend` directory) and a React-based frontend (in the `frontend`) directory.  In a nutshell:

* Your frontend is a React app that is bundled into a single file (`bundle.js`).  
* You edit the frontend code in the `frontend` directory
* The `npm run start` command will use watchify + browserify + reactify to create a single `bundle.js` file, which is stored in `backend/public`
* The Golang backend is in the `backend` directory.  `gin` is used to do live recompile.
* The Golang server uses `net/http` to serve the contents of `backend\public` as a static site.  The `index` file in this directory loads the `bundle.js` app generated by your frontend.  

To use it, you'll need:

* `npm` for package management
* A Golang dev environment
* [gin](https://github.com/codegangsta/negroni)

First, clone it down to your machine (duh!) and `cd` into your new directory.  Then:

```
npm install
npm run start
```

This will start a dev server with live reload so that you can edit your go code in the `backend` and your React code in `frontend`.  `gin` handles reload for Golang and `watchify` handles it for React.

View the app at `http://localhost:3000`.


You should then put your new components in `frontend\components` and your golang stuff in `backend`.
