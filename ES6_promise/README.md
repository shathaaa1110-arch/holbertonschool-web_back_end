# ES6 Promises

**Author:** Shatha Alanzi

This project is about working with asynchronous code in JavaScript (ES6) using Promises.
It covers creating promises, handling results with `then` and `catch`, running many promises together, and handling errors with `try` / `catch`.

## What I learned

- What a Promise is and how to create one
- How to use `then`, `catch` and `finally`
- How to run many promises together with `Promise.all`, `Promise.allSettled` and `Promise.race`
- How to throw errors and catch them with `try` / `catch`

## Tasks

| # | File | What it does |
|---|------|--------------|
| 0 | `0-promise.js` | Returns a simple Promise. |
| 1 | `1-promise.js` | Returns a Promise. If `success` is `true`, it resolves with `{ status: 200, body: 'Success' }`. If not, it rejects with the error `The fake API is not working currently`. |
| 2 | `2-then.js` | Takes a promise. When it resolves, it logs `Got a response from the API` and returns `{ status: 200, body: 'success' }`. When it rejects, it returns an empty `Error`. |
| 3 | `3-all.js` | Calls `uploadPhoto` and `createUser` from `utils.js` together using `Promise.all`, then logs the photo body with the first and last name. If something fails, it logs `Signup system offline`. |
| 4 | `4-user-promise.js` | Returns a resolved Promise with `{ firstName, lastName }`. |
| 5 | `5-photo-reject.js` | Returns a rejected Promise with the error `<filename> cannot be processed`. |
| 6 | `6-final-user.js` | Calls the functions from task 4 and task 5 together using `Promise.allSettled`, and returns an array with the `status` and `value` of each one. |
| 7 | `7-load_balancer.js` | Takes two download promises and returns the result of the one that finishes first, using `Promise.race`. |
| 8 | `8-try.js` | Divides two numbers. If the denominator is `0`, it throws `cannot divide by 0`. |
| 9 | `9-try.js` | Runs a math function inside `try` / `catch` and returns an array with the result (or the error message), followed by `Guardrail was processed`. |

## How to run

```bash
npm install
npm run dev 0-main.js
```
