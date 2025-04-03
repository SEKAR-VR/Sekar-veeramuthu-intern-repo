# Git Understanding

## Why are PRs important in a team workflow?
PRs are important in a team because they allow everyone to check each other's work before it’s added to the main project. This helps prevent mistakes, improves code quality, and keeps things organized. It also allows the team to have discussions and suggest changes in a structured way. PRs make sure that everyone is aware of what’s changing and why.

## What makes a well-structured PR?
A good PR has a clear title, a short but clear explanation of what was changed and why, and it should be easy to understand. It also helps to link any related issues and break the changes into smaller commits. If the code is clean and follows the project’s style, it’s easier for others to review. Having tests pass is also important so the team knows the changes didn’t break anything.

## What did I learn from reviewing an open-source PR?
I learned that open-source projects have a very respectful and helpful review process. Reviewers give feedback politely and suggest ways to improve the code. I saw that changes often go through a few rounds of suggestions and updates before they’reaccepted. It was interesting to see how everyone works together to improve the project. I also noticed how important automated tests are before merging any changes.
## Debugging with Git Bisect

### What does `git bisect` do?
`git bisect` helps you find out which specific commit introduced a bug. Instead of checking each commit manually, it uses a method called binary search. It checks out different commits and asks you to say whether each one is "good" or "bad", and keeps narrowing down the search until it finds the exact commit that caused the problem.

### When would you use it in a real-world debugging situation?
You would use `git bisect` when a bug appears in your project, but you're not sure when it started. For example, if your code was working last week and now it's broken, you can use `git bisect` to figure out which commit between then and now introduced the bug. It’s really useful when there are lots of commits, and it would take too long to check them one by one.

### How does it compare to manually reviewing commits?
Manually reviewing each commit can be very slow, especially in large projects. `git bisect` is much faster because it only asks you to check a few commits (usually 4–5). It automates the process and saves time by helping you find the broken commit more quickly and easily.
What makes a good commit message?
A good commit message is short, clear, and explains exactly what was changed and why. It should start with a summary line using present tense (e.g., “Add login button”), and if needed, including a short explanation below with more details. It helps make the project history easy to understand.

How does a clear commit message help in team collaboration?
Clear commit messages help teammates quickly understand what each change does without having to read through all the code. This saves time during reviews, improves communication, and makes it easier for others to troubleshoot, improve, or continue the work.

How can poor commit messages cause issues later?
Poor commit messages like “updated stuff” or “fixed bugs” don’t tell you what was actually done. Later, if someone needs to understand why something changed or fix a bug, it’s harder to trace the problem. It can lead to confusion, mistakes, and wasted time trying to figure things out.


What makes a good commit message?
A good commit message is short, clear, and explains exactly what was changed and why. It should start with a summary line using present tense (e.g., “Add login button”), and if needed, including a short explanation below with more details. It helps make the project history easy to understand.

How does a clear commit message help in team collaboration?
Clear commit messages help teammates quickly understand what each change does without having to read through all the code. This saves time during reviews, improves communication, and makes it easier for others to troubleshoot, improve, or continue the work.

How can poor commit messages cause issues later?
Poor commit messages like “updated stuff” or “fixed bugs” don’t tell you what was actually done. Later, if someone needs to understand why something changed or fix a bug, it’s harder to trace the problem. It can lead to confusion, mistakes, and wasted time trying to figure things out.

## Exploring More Git Commands

### What does each command do?

- **`git checkout main -- <file>`**: Restores a specific file from the `main` branch. Helpful when you want to undo changes to one file without affecting others.

- **`git cherry-pick <commit>`**: Takes one commit from another branch and applies it to your current branch. You can use it to bring in one useful change without merging the whole branch.

- **`git log`**: Shows the project’s commit history. You can see who made changes, when, and what they changed.

- **`git blame <file>`**: Shows who last edited each line of a file and when. Useful for tracking changes and asking questions about specific lines.

---

### When would you use these in a real project?

- Use **`checkout`** when you only want to undo changes in one file, not the whole project.
- Use **`cherry-pick`** when someone made a fix on another branch, and you want only that change.
- Use **`log`** to understand what happened in the project over time or find a specific commit.
- Use **`blame`** when debugging or trying to understand why something was written a certain way.

---

### What surprised me while testing these commands

I was surprised how easy it was to fix just one file using `git checkout`.  
`git cherry-pick` was really cool—it let me pull in one commit without merging everything.  
And `git blame` was very detailed; I could see exactly who changed each line.  
These tools are really powerful, especially when working in a team with lots of changes.
