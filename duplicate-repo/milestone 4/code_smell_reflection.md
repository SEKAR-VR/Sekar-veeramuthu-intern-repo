# Code Smell Reflection

## What code smells did you find in your code?

In my earlier code, I identified several common code smells:

- **Magic Numbers**: Hardcoded values like `3.14`, `0.9`, and `100` were used without context.
- **Long Functions**: Some functions were trying to handle multiple responsibilities.
- **Duplicate Code**: Logic such as calculations appeared in multiple places.
- **Inconsistent Naming**: Short or unclear variable/function names (e.g., `f`, `x`) made the code harder to understand.
- **Commented-Out Code**: Unused code was left in the file, adding visual clutter.
- **Large Classes (God Objects)**: Some classes were doing too much instead of being split by responsibility.
- **Deeply Nested Conditionals**: Complex `if` statements made logic harder to follow.

---

## How did refactoring improve the readability and maintainability of the code?

Refactoring the code brought several improvements:

- **Improved clarity** by using named constants and descriptive function/variable names.
- **Better structure** by breaking long functions into smaller, single-purpose functions.
- **Increased reusability** by removing duplicate logic and creating reusable functions.
- **Cleaner codebase** by removing commented-out lines and reducing clutter.
- **Modularity** by splitting large classes into smaller, focused components.

These changes made the code easier to read, easier to test, and simpler to maintain over time.

---

## How can avoiding code smells make future debugging easier?

Avoiding code smells helps in:

- **Locating issues quickly** due to well-organized and clear code.
- **Understanding logic faster** through meaningful names and consistent patterns.
- **Reducing bugs** by removing repetition and simplifying complex logic.
- **Making safer changes** since each function or class has a clear and isolated role.
- **Writing better tests** for smaller, focused components.

Clean code not only prevents bugs — it also makes fixing them faster and less error-prone.

