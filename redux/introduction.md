# Redux Introduction

## Core Concepts

* Single Immutable State Tree
  * State in Redux exists as a single object. This makes it much easier to manage state, hydrate the client with state, and perform actions regarding state's history.
* Reducers
  * Pure functions that take the current state and return the next state.  Key concept is that the state is immutable, so we return an entirely new object, not just a mutated previous object.
* Stores
  * The state is read-only from the store, nothing can change the state, actions can be emitted, which call reducers.

## Videos
* Series on egghead.io by the creator of Redux, Dan Abramov: [Introduction to Redux](https://egghead.io/series/getting-started-with-redux)



## To-Dos:
* Try to recreate the counter example from Dan's videos.
