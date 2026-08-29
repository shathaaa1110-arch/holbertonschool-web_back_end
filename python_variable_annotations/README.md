# Python - Variable Annotations

Type annotations in Python 3: how to declare the types of variables, function
parameters and return values, and how to check those declarations with `mypy`.

Python is dynamically typed, so annotations are never enforced at runtime — a
function annotated `-> float` will still happily return a string. They exist for
two reasons: the people reading the code, and the static analysis tools that read
it before it ever runs.

## Requirements

- Ubuntu 20.04 LTS, Python 3.9
- All files end with a new line and start with `#!/usr/bin/env python3`
- Code follows `pycodestyle` (version 2.5)
- All files are executable
- Every module, class and function has a docstring explaining its purpose

Checking style and types:

```
pycodestyle *.py
mypy 102-type_checking.py
```

## Files

| File | Task | Concepts |
|------|------|----------|
| `0-add.py` | `add(a, b)` returns the sum of two floats | Basic parameter and return annotations |
| `1-concat.py` | `concat(str1, str2)` joins two strings | `str` annotation |
| `2-floor.py` | `floor(n)` returns the floor of a float | Return type different from parameter type |
| `3-to_str.py` | `to_str(n)` returns the string form of a float | Explicit type conversion |
| `4-define_variables.py` | Four annotated module-level variables | Annotating variables, not just functions |
| `5-sum_list.py` | `sum_list(input_list)` sums a list of floats | `List[float]` from `typing` |
| `6-sum_mixed_list.py` | `sum_mixed_list(mxd_lst)` sums ints and floats | `Union` for values of several types |
| `7-to_kv.py` | `to_kv(k, v)` returns a key and the square of a value | `Tuple` with a fixed shape |
| `8-make_multiplier.py` | `make_multiplier(multiplier)` returns a function | `Callable`, closures |
| `9-element_length.py` | `element_length(lst)` pairs each item with its length | `Iterable`, `Sequence`, duck typing |
| `100-safe_first_element.py` | First element of a sequence, or `None` | `Any`, `Optional` |
| `101-safely_get_value.py` | Dictionary lookup with a fallback value | `TypeVar`, `Mapping`, generics |
| `102-type_checking.py` | Fix the code until `mypy` reports no errors | Static type checking in practice |

## Usage

File names start with a digit, so they cannot be imported with a normal `import`
statement. Use `__import__` instead:

```python
#!/usr/bin/env python3
add = __import__('0-add').add

print(add(1.11, 2.22))        # 3.33
print(add.__annotations__)    # {'a': <class 'float'>, 'b': <class 'float'>, 'return': <class 'float'>}
```

Annotations are stored on the function itself, which is what tools like `mypy`
and editors read.

## Notes

`7-to_kv.py` is a good illustration of what annotations do and don't do:

```python
to_kv("eggs", 9)   # ('eggs', 81)
```

The return is annotated `Tuple[str, float]`, but `81` is an `int`. Nothing
complains, because nothing checks. Running `mypy` on the file is what turns the
annotation into something with consequences — that is the point of the last task.

## Resources

- [PEP 484 — Type Hints](https://peps.python.org/pep-0484/)
- [`typing` — Support for type hints](https://docs.python.org/3/library/typing.html)
- [mypy documentation](https://mypy.readthedocs.io/en/stable/)

## Author

[Shatha Alanazi](https://github.com/shathaaa1110-arch) — Holberton School
