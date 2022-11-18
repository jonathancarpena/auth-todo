# Simple Todo with Login Page

> This project features a simple login page and a todo list that persists through localStorage. 
> The project is built using React.js, TypeScript, and plain CSS.

## Buidling Process

### Login Page
The state is managed using the React Hooks where the user authentication state is recorded in App.tsx. If the user is authenticated, then the MyTodos component will render otherwise, the Login component will still be rendered. Inside the Login component, although, there was support in validating email and requiring min and max lengths, I still created separate validating functions to verify if the email field was valid and the password was valid as well. Since I was having issues with sending a post request with the link given, I created a mockFetchLogin function that mocks the login process using Promises and async/await. I also incorporated different error messages based on the mocked status codes. The whole process of coding the logic as well as the design took about 1-2 hours

### My Todos Page
The MyTodos components keep track of todoList, filteredTodoList, newTodo, and search. The user-generated todos are stored in localStorage. On initial mount, using useEffect, the program fetches the “todo-list” key and if there isn’t a key, then it sets an empty array to the key “todo-list” in localStorage. However, if the key is present, the data is then parsed and set as the todoList state. After setting up the initial state, I began building the search bar and the add new todo function. If there is data in the todoList state, then the search feature will render a filtered list of todos that include the characters that are imputed (case insensitive). The new todo button triggers the newTodo state and places a form under the search bar where the user can record their new todo. After clicking save, I update the state and the array in localStorage. This same function pattern of updating the state and the array in localStorage is applied when editing todos and deleting todos. The whole process of coding the logic and design took about 2-3 hours.

