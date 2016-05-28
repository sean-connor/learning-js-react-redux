# Redux Introduction

## Core Concepts

* Single Immutable State Tree
  * State in Redux exists as a single object. This makes it much easier to manage state, hydrate the client with state, and perform actions regarding state's history.
* Reducers
  * Pure functions that take the current state and return the next state.  Key concept is that the state is immutable, so we return an entirely new object, not just a mutated previous object.
* Stores
  * The state is read-only from the store, nothing can change the state, actions can be emitted, which call reducers.

## Videos
* Must watch intro by Dan Abramov: [Live React](https://www.youtube.com/watch?v=xsSnOQynTHs)
* Series on egghead.io by the creator of Redux, Dan Abramov: [Introduction to Redux](https://egghead.io/series/getting-started-with-redux)



## To-Dos:
* [Awesome Redux](https://github.com/xgrommx/awesome-redux), really great central point for finding redux information.
* Try to recreate the counter example from Dan's videos.
