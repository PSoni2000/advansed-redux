# Notes

- Reducers must be **pure, side-effect free, synchronous** functions.

that means http request must not go on our reducers

- where should side-effects and async tasks be executed?

1. Inside the components (e.g. useEffect())
2. Inside the action creators
