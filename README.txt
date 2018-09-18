The simple project demonstrates how Async Hooks can help find automatically the original HTTP request which trigerred an error.

It was generated with:
  express --view=ejs myapp
The only files which we modified after are:
  app.js: the modified section is explicitely delimited by comments
  asyncHooksDoctrineSimplified.js: this is core of the async hooks implementation

To run it (you need at least Node.js):
  cd myapp
  npm install
  npm start

Then to test the concept:
  Go to http://localhost:3000/ to check the app is running (you should see "Welcome to Express")
  Go to http://localhost:3000/crash1 -> The application should crash, but you should be able to see in the console that it was /crash1 that triggered the crash.
