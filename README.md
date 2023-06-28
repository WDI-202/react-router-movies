## Work one piece at a time, please commit as you go. Will be looking at the commits and will be accounted for!

1. Set up a new React project: Create a new React project using Create React App.

2. Install React Router: In your project directory, install React Router by running the following command:

   ```
   npx create-react-app .
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
