Routing:
  1) Either of 2 libraries, React Router or Reach Router.
  2) The navigation bar should always be there while the contents are the one that are re-rendering.

Updating/Upgrading Libraries:
  1) 

Setting Up Our Homepage:
  1) BrowserRouter is the generic router.
  2) BrowserRouter is a component.
  3) Route level components should only be used for routing.
  4) Import { Routes, Route }.
    - These 2 components required to assemble routing.
    - Routes to wrap everything within.
    - Route for each individual route.
  5) Route 
    - Path is the relative path.
    - element renders the page.

React Router Outlet:
  1) Nested routes to keep the navigation bar from re-rendering.
  2) Make Route components where we can embed children between them.
  3) The path which is nested inside is relative to the path of the parent.
  4) Parental component at parent level route is going to render unless we tell it otherwise.
  5) You need to use {Outlet} in the parent component to render the child component.
    - Put the <Outlet /> in return ().
  6) Outlet allows pattern matching and nesting structure.

Navigation Bar Component:
  1) Create a navigation bar and nest the contents inside of it.
  2) Instead of path, use index to default the content showed on first start up.
  3) Routing nesting can go however deep you want.

React Router Link:
  1) We can use a {Fragment} instead of {div} in a component.
  2) Fragment is rendered to nothing when gets mounted on the DOM.
    - It renders whatever is inside but it itself is not rendered.
  3) Link behaves like an anchor tag.
    - Link is utilized for proper routing.
    - Whatever you wrap within the link it gives it the routing functionality.

Setting Up Firebase:
  1) By Google.
  2) Help to build out sign-in page using authentication.
  3) Firebase is a Google platform that allows you to spin up a database.
    - Helps to leverage some kind of database.
  4) 

Authentication Flow:
  1) CRUD
    - Create
    - Read
    - Update
    - Delete
  2) The majority of the data will not live on our front-end.
  3) Each user has specific data on their own page.
  4) You send a request you get back a response.
  5) Firebase allows us to leverage email and password authentication.
    - Also allows us to use Google sign in.
  6) Authentication - Makes sure that you are who you say you are to an application.
  7) Starts with making a request with Google sign in.
    - Sign in with password and email.
  8) Google creates an auth_token
    - A unique hash string that's really hard to break apart.
  8) Responds back with the auth_token.
  9) Sends the auth_token to the Firebase.
  10) Firebase will verify the auth_token with Google.
  11) Google will send back a verification_token.
  12) Firebase will send back to user an access_token.
    - The access_token is user specific. Defines what the user should be able to access.
  12) User sends the CRUD request alongside the access_token.
  13) Firebase return responses.
  14) The access_token is important to skip having to verify every single step.

Authenticating With Firebase:
  1) 

Async Await:
  1) A way to write asynchronous code that looks more synchronous.
  2) fetch call, will use .then, for error handling use .catch.
  3) We can replace with using async await.
    - const functionName = async () => {}
  4) Await pauses the function's execution until what is being awaited is completed and comes back with a value.
  5) Async await error handling:
    - try {} catch (err) {}.

Introducing Firestore Data Models:
  1) You can add multiple different authentication provider services.
  2) Authentication is separate service from Firestore Database.
  3) Firestore comprises data, document, collection.
    - Documents are JSON objects.
  4) You are trying to get the data from the document.

Sign Up Form Pt.1:
  1) Set button type = submit, and you can set a change of onSubmit.
  2) 
