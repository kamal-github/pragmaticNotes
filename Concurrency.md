#### General Guide
- Share state is an incorrect state
- Use concurrent primitives to handle shared state properly.
- It is always the reponsibility of an API to take care of concurrency and exclusive access of shared resources handling, NEVER of the callers.
- Shared resources not only includes memory refs, but also Files/Network resources/DB etc, access them in concurrent-safe manner too.

#### Actor model
- Actor model for concurrency, [Learn more about it](https://www.google.com/search?q=actor%20model%20concurrency).
It is similar to go routines that pass the messages through channels and do not share the memory, Actor model is widely used in Erlang/Elixir and there are other language implementations.

#### Blackboards
