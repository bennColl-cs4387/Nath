# Solo Fix Progress Report

**Project**: Appsmith & P5.js  
**Primary Issue**: Appsmith - [Issue #37281: Rapid Clicks on "Create Workspace" Button Causing Duplicate Workspaces](https://github.com/appsmithorg/appsmith/issues/37281)  
**Objective**: Address a bug that causes duplicate workspaces to be created when clicking the "create new workspace" button rapidly.

---

### Progress and Exploration

Setting up the Appsmith server locally has been challenging, especially with the need to configure WSL2, Docker, OpenJDK, and environment variables on my Windows system—areas I hadn’t worked with before. Despite these challenges, I’ve made significant progress in understanding system configurations, although I am still navigating some aspects of the setup.

In the Appsmith issue I’m working on, rapidly clicking "create a new workspace" leads to multiple workspaces with identical names. I successfully reproduced the bug on my setup, allowing me to trace its origin within the codebase.

### Proposed Solution

To resolve this, I am implementing logic to make the button inactive immediately after the first click. The button will then reactivate once the workspace creation process completes, ensuring only one workspace is created per click. This fix will enhance data integrity and user experience by preventing unintended duplicates.

### Current Challenges

- **System Setup**: Configuring WSL2, Docker, and OpenJDK in Windows has been a learning curve, but it has strengthened my understanding of cross-platform setup.
- **Button State Management**: Ensuring that the button correctly disables and re-enables only after the workspace creation process completes, which involves testing and refining the timing of button state changes.

**Secondary Issue**: P5.js Web Editor - [Issue #3145: Wrong Language Displayed in Console](https://github.com/processing/p5.js-web-editor/issues/3145)  
