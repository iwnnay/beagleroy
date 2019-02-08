# beagleroy
Dynamic State Interface for React

# Description
Beagleroy creates an interface for maintaining and adjusting the state of an
application. This is still in the early state of development.

# Current Spec

    const state = createStore('inventory');

    state.createAction('addItem', (name, price) => {
        ... return a pure version of the state
    })
    .meanwhile(*(state, action) => {
        ... asynchronous calls
    });

# Why beagleroy
This is a baseline attempt to make a state storage interactive through actions
that have side effects in as compact a space as possible.

# Goals
* Testability
* Compact action writing
* State maintaince and healing
* ease of use and understanding
