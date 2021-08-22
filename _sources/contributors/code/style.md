# Code style

## Code formatting 
We use the [`black` code formatter](https://black.readthedocs.io/en/stable/) with 79 character line limits.
We also adopt the [PEP8](https://www.python.org/dev/peps/pep-0008/) style guide whenever possible (`black` does not enforce all PEP8 style recommendations, so please consult PEP8 if you're unsure about something).

### Comments
`black` does not modify comments. Please do the following:
* Keep comments to 79 characters when possible
* Add a space after the `#`
* Capitalize the first letter of the first word in a comment, unless it refers to a lowercase object

**DO NOT:**
```python
#this line is really long this line is really long this line is really long this line is really long this line is really long
```

**DO:**
```python
# This line is really long this line is really long this line is really long
# this line is really long this line is really long
```

## Functions

Do not create a variable which is only returned.

**DO NOT:**
```python
def square(x):
    res = x * x
    return res
```
**DO:**
```python
def square(x):
    return x * x
```

## Data analysis

### `pandas`

Use `.` notation to access columns.

**DO NOT:**
```python
df["in_poverty"] = df["income"] < df["poverty_threshold"]
```

```python
df["in_poverty"] = df.income < df.poverty_threshold
```
