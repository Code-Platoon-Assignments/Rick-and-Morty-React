# Rick and Morty React

Create a project for the Rick and Morty show. By the end of this assignment your project should meet the following requirements:
  
  - Vite + React Development Environment
  - HomePage.jsx, App.jsx, router.jsx
  - React Router's browser router (`createBrowserRouter`) connected to App.jsx
  - HomePage.jsx should render a quick "Attention Getter" to get people to watch the show at [http://localhost:5173/](http://localhost:5173/)

## Setup

```sh
npm create vite@latest rick-and-morty -- --template react
cd rick-and-morty
npm install
npm install react-router
npm run dev
```

React Router 8 needs Node 22.22+ (the devcontainer uses Node 24). It is one package, `react-router`: `react-router-dom` stopped at version 7, so skip tutorials that install it or use `<BrowserRouter>`, `<Switch>`, `useHistory` or `history.push`.

- `RouterProvider` comes from `'react-router/dom'`; everything else (`createBrowserRouter`, `Outlet`, `Link`, the hooks) comes from `'react-router'`.
- In `router.jsx`, create the router with `createBrowserRouter`: `App` is the route for `/`, and `HomePage` is one of its `children`.
- `App.jsx` renders an `<Outlet />` where the current page should appear.
- In `main.jsx`, render `<RouterProvider router={router} />` instead of `<App />`.
