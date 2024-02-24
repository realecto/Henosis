NOTE: THIS PROJECT WAS CREATED WITH A LOCAL VERSION CONTROL AND PUSHED TO THIS ACCOUNT AT ONCE.

# Getting Started

First, run the development server:

```bash
npm run dev
# or
yarn dev
# or
pnpm dev
```

# Structure Overview

- Henosis is created using Next.js + Tailwindcss as frontend, and Firebase as back end.

- Todo component take in a uid that represents a todo list, if no uid is found then render
  TodoDates component, else render TodoList component

- TodoDates component renders all the different lists which are represented with dates as
  titles, each TodoDates document has a uid, and a items collection.
  On the top, the component renders a form. Which requires the users to enter a title, date, time woken up, and on submittion the component generates a uid for this task and writes all this information to "collection(firestore, "todos")". And updates the context to have a uid, and render the TodoList component. 

- TodoList component takes in a uid, and reads the todolist with that uid. And renders all 
  the items that particular list has.

*I am not sure if I should have the date objects to be a link and takes the user to a unique webpage, or I want the components to render all in the little box in real time. Since the website is basically a dashboard, it would be nice to not have to take the user to a whole new page. But this may be a possible challenge.

# Features

Henosis starts on a daily basis.

![henosis_1](https://github.com/realecto/Henosis/assets/126880408/dd6c6d50-3b2e-42f9-af00-60fe5100952e)

Then you have all your tasks, which you can drag them around to order them.

![henosis_2](https://github.com/realecto/Henosis/assets/126880408/ed5ce5f4-6b41-40e3-be4b-fa0c1f6c29ef)

You can also edit them

![henosis_3](https://github.com/realecto/Henosis/assets/126880408/63aa3755-4733-4d73-baa4-b9219f7e125a)

All real time!
