# Solo Fix Progress Report

**Project**: Appsmith & P5.js  

---

### **Primary Issue**: Appsmith - [Issue #37281: Rapid Clicks on "Create Workspace" Button Causing Duplicate Workspaces](https://github.com/appsmithorg/appsmith/issues/37281)  
**Objective**: Address a bug that causes duplicate workspaces to be created when clicking the "create new workspace" button rapidly.

### Progress and Exploration

Setting up the Appsmith server locally has been challenging, especially with the need to configure WSL2, Docker, OpenJDK, and environment variables on my Windows system—areas I hadn’t worked with before. Despite these challenges, I’ve made significant progress in understanding system configurations, although I am still navigating some aspects of the setup.

In the Appsmith issue I’m working on, rapidly clicking "create a new workspace" leads to multiple workspaces with identical names. I successfully reproduced the bug on my setup, allowing me to trace its origin within the codebase.

### Proposed Solution

To resolve this, I am implementing logic to make the button inactive immediately after the first click. The button will then reactivate once the workspace creation process completes, ensuring only one workspace is created per click. This fix will enhance data integrity and user experience by preventing unintended duplicates.

### Current Challenges

- **System Setup**: Configuring WSL2, Docker, and OpenJDK in Windows has been a learning curve, but it has strengthened my understanding of cross-platform setup.

### **Secondary Issue**: P5.js Web Editor - [Issue #3145: Wrong Language Displayed in Console](https://github.com/processing/p5.js-web-editor/issues/3145)  

Since the P5.js Web Editor is separate from the main P5.js website, I had to set up a new development environment specifically for the Web Editor. I was able to reproduce the bug and confirmed that it exists across multiple devices. I tracked the issue to the `app.7125da892f4be04cf9b4.css` and `app.9458286023106da484d7.js` files. Reviewing the code, I found that the return message defaults to English regardless of the selected language. This issue is also linked to the HTML file, so I need to brainstorm the best solution to fix this bug.
