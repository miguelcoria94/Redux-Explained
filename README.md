<h1 align="center">
Redux Explained
</h1>

Redux is a JavaScript Framework for managing the frontend state of a web application.

Redux allows you to store information in an organized manner in a web app.

Redux also allows you to quickly retrieve that information from anywhere in the app

Advantages of using Redux

    * Redux simplifies some of the more complicated aspects of flux
    * Redux is very lightweight; the library only takes up 2kbs
    * Redux is very fast(the time to insert and retrieve data)
    * Redux is very predictable

<h1 align="center">
Where did Redux come from?
</h1>

Redux was created in 2015 by Dan Abramov.

Redux was created to simplify Flux.

Flux had a bunch of boilerplate code that was unnecessary. (things to create a flux app)

Dan also wanted to elimanate some of the problems he was facing when it came to debugging.

Dan envisioned dev tools that would allow him to undo or replay a series of actions at the click of a button.

Dans vision became the React DevTools.

Redux updates state using pure functions called Reducers.

One can simply replay a series of actions and be guaranteed to arrive at the same final state.

Redux also becomes more convenient to use a single object to use a single object  to store the state,
as opposed to traditional Flux which uses multiple store.

Philosophy of Redux

    * **A Single Source of Truth** The state for an entire Redux app is stored in a single plain JS object.
    * **State is Read Only** The state object cannot be directly modified. Instead it is modified by dispatching actions.
    * **Changes Are Made with Pure Functions** The reducers that receive the actions and return updated state are pure functions of the old state and the actions.

<h1 align="center">
When is it appropriate to use Redux?
</h1>

Redux has over 3mil downloads.

The Redux repo has over 50,000 stars.

Redux is used by big companies (Exana, Patreon, ClassPass)

Context, like Redux gives you a way to store and manage global state in your React apps.

Projects with simpler global state requirments favor Context over React.

Context is built into React so there's no need for additional installs.

Context is simpler and requires less work to get up and running.

Redux is still better for more complex global state.

Redux offers more flexibility with support for middlewares and better devtools.

<h1 align="center">
Vocabulary
</h1>

Learning how to use Redux requires you to understand a fair amount of terminology.

    * **State** "Redux is a state manager" - The state of a program means all the information stored by that program at a particular point in time. It's the data stored by a program at a particular instance in time, as opposed to the logic of the program, which doesnt change over time. The job of Redux is to store the state of your app and make it available to the entire app.

    










