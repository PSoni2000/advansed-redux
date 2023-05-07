# Notes

- Reducers must be **pure, side-effect free, synchronous** functions.

that means http request must not go on our reducers

- where should side-effects and async tasks be executed?

  1. Inside the components (e.g. useEffect())
  2. Inside the action creators

**Fat Reducers vs Fat Components vs Fat Actions**

- where should our logic (code) go?

1. Synchronous, side-effect free code (i.e, data transformations)
   - Prefer Reducers
   - Avoid Action Creators or Components
2. Async Code or Code with side-effect
   - Prefer Action Creation or Components
   - Never use Reducers

**Thunk**

- What is a "Thunk"?
  A function that delays an action until later.
  An action creator function that does NOT return the action itself but another function which eventually returns the action.
