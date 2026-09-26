# ES6 Data Manipulation

**Author:** Shatha Alanzi

This project is about working with data in JavaScript (ES6).
It covers arrays and their methods (`map`, `filter`, `reduce`), typed arrays, `Set`, and `Map`.

## What I learned

- How to use `map`, `filter` and `reduce` on arrays
- What typed arrays are and how to use them with `ArrayBuffer` and `DataView`
- How to use `Set` to store unique values
- How to use `Map` to store key/value pairs

## Tasks

| # | File | What it does |
|---|------|--------------|
| 0 | `0-get_list_students.js` | Returns a list of 3 student objects. Each student has an `id`, a `firstName` and a `location`. |
| 1 | `1-get_list_student_ids.js` | Takes a list of students and returns only their ids. If the input is not an array, it returns an empty array. Uses `map`. |
| 2 | `2-get_students_by_loc.js` | Takes a list of students and a city, and returns only the students who live in that city. Uses `filter`. |
| 3 | `3-get_ids_sum.js` | Returns the sum of all student ids. Uses `reduce`. |
| 4 | `4-update_grade_by_city.js` | Returns the students of a given city with their new grade added. If a student has no grade, the grade is `'N/A'`. Uses `filter` and `map`. |
| 5 | `5-typed_arrays.js` | Creates an `ArrayBuffer` of a given length, puts an `Int8` value at a given position, and returns a `DataView`. If the position is out of range, it throws `Position outside range`. |
| 6 | `6-set.js` | Takes an array and returns a `Set` made from it. |
| 7 | `7-has_array_values.js` | Checks if every item of an array exists in a set. Returns `true` or `false`. |
| 8 | `8-clean_set.js` | Takes a set and a start string. For each value that starts with that string, it keeps the rest of the value, then joins them with `-`. |
| 9 | `9-groceries_list.js` | Returns a `Map` of grocery items and their quantities. |
| 10 | `10-update_uniq_items.js` | Takes a grocery `Map` and changes every quantity of `1` to `100`. If the input is not a `Map`, it throws `Cannot process`. |

## How to run

```bash
npm install
npm run dev 0-main.js
```
