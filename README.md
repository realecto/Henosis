# Getting Started

First, run the development server:

```bash
npm run dev
# or
yarn dev
# or
pnpm dev
```
NOTE: THIS PROJECT WAS CREATED WITH A LOCAL VERSION CONTROL AND PUSHED TO THIS ACCOUNT AT ONCE.

# Structure Overview
- Todo component take in a uid that represents a todo list, if no uid is found then render
  TodoDates component, else render TodoList component

- TodoDates component renders all the different lists which are represented with dates as
  titles, each TodoDates document has a uid, and a items collection.
  On the top, the component renders a form. Which requires the users to enter a title, date, time woken up, and on submittion the component generates a uid for this task and writes all this information to "collection(firestore, "todos")". And updates the context to have a uid, and render the TodoList component. 

- TodoList component takes in a uid, and reads the todolist with that uid. And renders all 
  the items that particular list has.

*I am not sure if I should have the date objects to be a link and takes the user to a unique webpage, or I want the components to render all in the little box in real time. Since the website is basically a dashboard, it would be nice to not have to take the user to a whole new page. But this may be a possible challenge.

