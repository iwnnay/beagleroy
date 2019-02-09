# beagleroy
Dynamic State Interface for React

# Description
Beagleroy creates an interface for maintaining and adjusting the state of an
application. This is still in the early state of development.

# Why beagleroy
This is a baseline attempt to make a state storage interactive through actions
that have side effects in as compact a space as possible.


# Current Spec
## primary usage

    const state = createStore('inventory');

    state.createAction('addItem', (name, price) => {
        ... return a pure version of the state
    })
    .meanwhile(*(state, action) => {
        ... asynchronous calls
    });

## config

    const state = createStore('inventory', configObject);

The `configObject` in the line above is how you pass in additional options into
the system. Some of the options will require that additional libraries be installed.
If those libraries are not installed and the environment is development you'll
get a warning in the console.

* *Logging:* `off` (default), `all`, `actions`, `sideEffects`. Requires library `beagleroy-logging`
    Logging only works in development modes.

# Goals
* Testability
* Compact action writing
* State maintaince and healing
* ease of use and understanding
