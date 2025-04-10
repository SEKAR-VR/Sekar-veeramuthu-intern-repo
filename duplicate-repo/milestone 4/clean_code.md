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
