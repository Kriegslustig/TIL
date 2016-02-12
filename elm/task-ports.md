# Task Ports

In Elm outgoing Ports can be used to run things in concurrently to `main`. An outgoing port has the signature `Signal x`. You can use that to regularly perform some unsafe, asyncronous action and pass the result back into the main data-flow. Unsafe, asynchronous actions are `Task`s in Elm. To pass something from a port to `main`, you can use a `Mailbox`.

