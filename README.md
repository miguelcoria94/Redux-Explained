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

    * **Store** "The Redux store is updated by dispatching actions" - The Redux store is a single JS object with a few methods, including (getState, dispatch(action), and subscribe(listener)). Any state you want Redux to handle is held in the store.

    * **Actions** "The Redux store is updated by dispatching actions" - An action is a POJO with a type property. Actions contain info that can be used to update the store. They can be sent to the store, in response to user actions or AJAX requests. Typically Redux apps use functions called action creators that return actions. Action creators can take arguements which allow them to customize the data contained in the actions they generate.

    * **Pure functions** "Redux reducers are pure functions" - A function is pure if its behavior depends only on its arguements and it has no side effects. A pure function cannot depend on the value of any variables that are not passed in as arguements. Pure functions can not alter the state of the program or any variable existing outside itself. A pure function simply takes in arguements and returns a value.

    * **Reducer** "Redux handles actions using reducers." - A reducer is a function that is called each time an action is dispatched. The reducer recieves an action and the current state as arguements and returns an updated state. Redux reducers are required to be pure functions of the dispatched action and the current state. This maked their behaviour very predictable and allows their effects to potentially be reversed.

    * **Middleware** "You can customize your response to dispatched actions using middleware" - Middleware is an optional component of Redux that allows custom responses to dispatched actions. When an action is dispatched, it passes through each middleware that has been added to the state. The middleware can take some action in response and choose whether or not to pass the action on down the chain. Behind the scenes, the middleware actually replaces the dispatch method of the store with a customized version. There is a large ecosystem of existing middleware ready to be plugged into any Redux projects. Perhaps the most common use for middleware is to dispatch async requests to a server.

    * **Time traveling dev tools** "Redux has time traveling dev tools." - Redux reducers are pure functions of the dispatched action and the current state. This means that if one were to store a list of the previous states over time and the action sthat had been dispatched, one could retroactively cancel an action and recalculate the state as if that action had never dispatched. This is precisely the functionality that the Redux DevTools provide. The dev tools can be added as middlewate to any Redux project. They allow you to look back through the history of the state and toggle past actions in and off to see a live recalculaton of the state. This ability to revert toa previous state us what is meant by time travel.

    * **Thunks** "Thunks are a convienent format for taking async actions in Redux" - A thunk is a general concept in computer science referring to a function whose primary purpose is simply to call another function. In Redux a thunk action creator returns a function rather than an object. When they are dispatched thunks are intercepted by a piece of middleware that simply checks if each action is a function. If it is, that function is called with the state and dispatched as arguements, otherwise it is passed on down the chain. Thunks are most commonly used to make asynce API requests.








