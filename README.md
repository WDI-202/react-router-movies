## Work one piece at a time, please commit as you go. Will be looking at the commits and will be accounted for!

1. Set up a new React project: Create a new React project using Create React App.

2. Create app with create-react-app: and install needed dependencies

   ```
   npx create-react-app .
   npm i react-router-dom uuid
   ```

3. Create a movie data source:

   - Define a movie data structure, including properties like title, genre, director, actors, movieLength and etc.
   - Create a local mock dataset of movies. You can put it in another file or keep it at the top of the component that holds all the state.

4. Set up the routes: Set up the routes using React Router in index.js. Define routes for the following pages:

   - Home page: Displays a list of movies.
   - Movie details page: Displays detailed information about a specific movie.
   - Create movie page: Allows users to add a new movie.
   - Edit movie page: Allows users to edit an existing movie.

5. Create components: Create the necessary React components for each page defined in the routes.

   - Home component: Fetches the list of movies from your list of fake movies and displays them in a list format.
   - MovieCard: Holds information of each movie that will be displayed in the Home component.
   - MovieDetails component: Fetches the details of a specific movie from the data set and displays them in its own page.
   - CreateMovie component: Provides a form for users to enter details of a new movie and submit it to the mock dataset.
   - EditMovie component: Similar to CreateMovie but prepopulates the form with existing movie details.

6. Implement CRUD functionality:

   - Home component: READ, display the list of movies.
   - MovieDetails component: READ, display the details of a specific movie.
   - CreateMovie component: CREATE, add a new movie when the form is submitted.
   - EditMovie component: UPDATE, update an existing movie when the form is submitted.
   - Delete functionality: DELETE button on the MovieDetails page to remove a movie from the list.

7. Link components using React Router: Use the appropriate links and route configurations to navigate between pages and pass necessary data (such as movie IDs) as URL parameters.

8. Test and refine: Test your application to ensure that all CRUD operations are working correctly. Make any necessary refinements or improvements to the user interface or functionality.

9. Style your application: Apply CSS styles or use a UI library like Bootstrap to enhance the visual appeal of your application.

**Reminder**

1. In index.js:

- Import createBrowserRouter and RouterProvider from react-router-dom.

  ```
  import { createBrowserRouter, RouterProvider } from 'react-router-dom'
  ```

- create router by using createBrowserRouter.
- Create routes in array form:
  ```
  createBrowserRouter([
     {
        path: "",
        element: <Component/>,
        children:[
           {
              index: true,
              element: <Component>
           },
           {
              path: "",
              element: <Component>
           }
        ]
     },
     ...Other routes
  ])
  ```
- replace `<App/>` with `<RouterProvider router={router}/>`.
- If you're want to use params remember to use `:<param variable name>` inside path.
- If you want a children element to render first use `index: true` inside the children routes.

2. In App.js:
   -If you're using children inside the createBrowserRouter, remember to put `<Outlet/>` from react-router-dom inside the return.

   ```
   import {Outlet} from 'react-router-dom'
   ```

   -If App.js holds states that will be passed down as props to the children(from createBrowserRouter) remember to put `context ={{}}` and the props inside `<Outlet/>`.

3. In App.js' children(from createBrowserRouter):
   -If you're using the props passed in from `context={{}}`, remember to use `useOutletContext()` hooks from react-router-dom to get the props.

   ```
   import {useOutletContext} from 'react-router-dom'
   const { props } = useOutletContext()
   ```

   -If you're using params use `useParams()` hooks from react-router-dom.

   ```
   import {useParams} from 'react-router-dom'
   const { paramName } = useParams()
   ```

   -If you want to redirect use `useNavigate()` hooks from react-router-dom.

   ```
   import {useNavigate} from 'react-router-dom'
   const navigate = useNavigate()
   navigate('/routes)
   ```

4. If you're creating a NavBar:

- use `<Link to="/routes"></Link>` component from react-router-dom.
