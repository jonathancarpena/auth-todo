# Simple Todo with Login Page

> This project features a simple login page and a todo list that persists through localStorage. 
> The project is built using React.js, TypeScript, and plain CSS.

## Buidling Process

### Login Page
The state is managed using the React Hooks where the user authentication state is recorded in App.tsx. If the user is authenticated, then the MyTodos component will render otherwise, the Login component will still be rendered. For the Login component, I created separate validating functions to verify if the email field was valid and the password was valid as well. Since I was having issues with sending a post request to the link given, I created a mockFetchLogin function that mocks the login process using Promises and async/await. I also incorporated different error messages based on the mocked status codes. 

