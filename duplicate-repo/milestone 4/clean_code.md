# Clean Code Reflection

## How do unit tests help keep code clean?

Unit tests help make sure each function works the way it’s supposed to. It makes the code cleaner because I have to think about how to break it down into smaller parts that are easier to test. If I change something later, the tests will tell me if I broke anything. That way I can fix it quickly.

Also, writing tests forces me to write better code — not messy or complicated. It’s easier to read, reuse, and understand. So it keeps the code clean and not confusing.

---

## What issues did you find while testing?

While testing my function, I saw that I didn’t think about all edge cases — like what happens if I multiply by 0 or use a negative number. The tests helped me notice that.

Also, I had to move my logic into a separate function to make it easier to test. That actually made my code better and more organized. So writing tests helped me find small mistakes and improve the way I wrote the function.

# handling error and edge code

## What was the issue with the original code?

The original function didn’t check for errors. For example, if someone tried to divide a number by 0, the code would break and throw an error. It didn’t handle that case at all. There was no check for invalid input, so the function wasn’t safe to use.

---

## How does handling errors improve reliability?

Handling errors makes the code more reliable because it doesn’t crash when something goes wrong. It gives a proper message or fallback result, so the user or system knows what happened. Adding guard clauses helps catch problems early and stop the function from running bad logic. It also makes debugging easier and keeps the app working even with bad inputs.
# Clean Code Reflection – Comments and Documentation

## When should you add comments?

You should add comments when the code is doing something that’s not easy to understand just by reading it. Like if there’s a trick or special logic, or something that needs a reason explained. A small comment helps someone know why the code is written that way.

---

## When should you avoid comments and instead improve the code?

If the code is clear, you don’t need comments. Instead of writing comments for simple things, just use better function and variable names. Like if you write a function called `a()` that adds numbers, it’s better to call it `add_numbers()` so it explains itself. If the code is confusing and needs a lot of comments, it’s a sign to clean it up first.
# Clean Code Reflection – Refactoring

## What made the original code complex?

The original code was doing too many things in one place. The function had nested ifs, hard-to-read logic, and no clear names. It was hard to follow what the code was doing step by step. Also, some parts were repeated and could’ve been reused instead of written again.

---

## How did refactoring improve it?

Refactoring made the code easier to read and understand. I broke the big function into smaller ones with clear names. I removed nested ifs and used early returns (guard clauses) to clean up the logic. I also reused code instead of repeating it. Now the code looks cleaner, and I can find and fix problems faster. It’s also easier to test and update later.

# Clean Code Reflection – DRY Principle

## What were the issues with duplicated code?

There were parts in the code where I was repeating the same logic in more than one place. For example, the same calculation or print statement was written twice. This made the code longer and harder to maintain. If I had to change the logic later, I would have to update it in multiple places, and it’s easy to miss one.

---

## How did refactoring improve maintainability?

I moved the repeated logic into a separate function and just called that function wherever needed. This made the code shorter, cleaner, and easier to understand. Now if I need to make a change, I only have to update it once. It also reduces the chance of bugs and makes the code easier to test and reuse.

# Clean Code Reflection – Small Functions

## Why is breaking down functions beneficial?

Breaking big functions into smaller ones makes the code easier to read and understand. Each small function has one job, so it's clear what it’s supposed to do. It’s also easier to test and debug when something goes wrong. If the logic is inside one big function, it's harder to figure out what part is causing the issue. Small functions are also reusable, so I can use them in other places if needed.

---

## How did refactoring improve the structure of the code?

I had a long function that was doing too many things — like printing data, calculating values, and sending messages all in one place. I split it into smaller functions like `print_user_info()`, `calculate_total()`, and `send_message()`. This made the code more organized and easier to follow. Now each function has a clear name and purpose, and the main function just calls them in order. It looks cleaner and makes more sense.

# Clean Code Reflection – Code Formatting

## Why is code formatting important?

Formatting is important because it makes the code easier to read and work with. If everyone follows the same style, the code looks clean and consistent across the project. It also helps avoid mistakes like missing semicolons, extra spaces, or messy indentation. Good formatting saves time during reviews and makes it easier for others to understand the code.

---

## What issues did the linter detect?

The linter showed small issues like:
- Missing semicolons
- Unused variables
- Wrong spacing in functions and objects
- `==` used instead of `===`

These issues didn’t break the code, but fixing them made it cleaner and more standard.

---

## Did formatting the code make it easier to read?

Yes, after running Prettier and fixing the ESLint issues, the code looked much better. The structure was clearer, everything was aligned properly, and it was easier to scroll through and understand each part. It also helped me spot other small things to clean up while reading the code.

# Clean Code Reflection – Naming

## What makes a good variable or function name?

A good name should clearly say what the variable or function is doing or storing. It should be easy to understand without needing a comment. For example, `total_price` is better than `tp`, and `calculate_discount()` is better than `cd()`.

---

## What issues can arise from poorly named variables?

Bad names make the code hard to read and confusing. If someone else looks at the code (or even me later), they won’t know what `x`, `data1`, or `calc()` is supposed to mean. It also increases the chance of making mistakes because you don’t fully understand what the code is doing.

---

## How did refactoring improve code readability?

I changed short or unclear names to more meaningful ones. For example, I renamed `t` to `total_amount`, and `fn` to `format_name()`. After that, the code was much easier to follow. I could understand the logic just by reading the names, without adding comments. It also made it easier to find what I needed while scrolling through the file.

# Clean Code Reflection – Core Principles

## Simplicity

Code should be simple and not do more than it needs to. The goal is to solve the problem in the easiest way possible, without adding extra steps or overthinking it. Simple code is easier to write, read, and test.

## Readability

Anyone reading the code (including me later) should be able to understand what it does without guessing. Good names, clear structure, and less clutter help with this. If I have to think too hard about what a line means, it’s not readable.

## Maintainability

Good code is easy to change or update in the future. If I or someone else needs to fix a bug or add a new feature, the code should be easy to work with. Messy code takes more time to understand and can break things when changed.

## Consistency

Following the same style across the whole project makes everything look cleaner. Using the same naming patterns, spacing, and structure helps everyone on the team understand the code faster.

## Efficiency

The code should run well and not be slow or use too many resources. But I shouldn’t overcomplicate the logic just to make it “fast” — it’s better to keep it clean first, and then optimize if needed.

---

## Messy Code Example (Before)

```python
def p(n):
    if n>0:
        for i in range(0,n):
            if i%2==0:
                print(i)
