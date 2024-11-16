# Addressing Bug #3229 on P5.js

For the #3229 bug on P5.js, I’ve decided to focus on the JavaScript files rather than the HTML and CSS files I was looking at earlier. My main goal is to fix the specific error without making unnecessary changes to the rest of the code. I was considering previously to make broader updates and improve other parts of the code, but I think it’s important to stick to just fixing the bug to avoid causing other errors or making my pull request harder to approve.

I’m also thinking about adding a hook to make the process of handling language updates smoother and more dynamic. This would make it easier to manage language changes without needing to make big adjustments to other parts of the code. The two files I’m focusing on, LoginForm.jsx and SignupForm.jsx, are quite similar in both appearance and functionality. For instance, both include functions (SignupForm and LoginForm) that handle user interactions pretty much in the same way.

One thing that stands out in both files is the use of `t`, a shared function for translations. This might be part of what’s causing the issue. If `t` isn’t updating properly, it could explain the translation errors. By focusing on this, I can fix the bug while keeping the rest of the code intact.

---

## Next Steps

- Implement the changes I am envisioning.
- Investigate the `t` and how this library works in react.
- Implement my hook.
