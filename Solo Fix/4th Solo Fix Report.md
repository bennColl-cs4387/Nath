
## Bug Report: [Missing Text in Case Studies Boxes](https://github.com/kubernetes/website/pull/48841)

### **Description of the Bug**

The issue occurred on the Kubernetes website, where text inside the **Case Studies** boxes was not appearing as expected.

I found the issue in the css/gridpage.css file. 

#### **Observed Behavior**
- Words inside the **Case Studies** boxes were not displayed.
- The issue was traced back to improper CSS styling rules.

#### **Expected Behavior**
- Text in the **Case Studies** boxes should appear clearly and be styled appropriately.

---

### **My Fix**

The solution was implemented in the `/css/gridpage.css` file. The updated CSS ensured that the text appeared properly with appropriate styles. Below is the code I added:

```css
.gridPage p:not(.announcement-main > p) {
    color: rgb(5 5 5);
    margin-left: 0 !important;
    padding-left: 0 !important;
    font-weight: 300 !important;
}
```

#### **Explanation**
- **Color**: Ensures text is visible using a dark color (`rgb(5 5 5)`).
- **Margin and Padding**: Removes unwanted indentation or padding (`margin-left: 0` and `padding-left: 0`).
- **Font Weight**: Sets the font weight to `300` to keep in the same pattern as the other text in the website. 

---

### **Timeline and Contribution**

I worked on identifying and fixing this bug on **11/23**. Before submitting my pull request, I noticed that someone else had also submitted a PR for the same issue. 

#### **Evidence**
- I have a **screenshot** of my fix with the timestamp, showing I resolved the issue before any commits or solutions were submitted.
- The attached screenshot includes my solution in `/css/gridpage.css` with the date of implementation.

#### **Link to Evidence**
[Screenshot and Timestamp](https://docs.google.com/document/d/1-X9dALOLbhhlevTOohiYoRn-cVNqc7wD5mZGmYxkKng/edit?usp=sharing)

---

### **Conclusion**

The bug was caused by incorrect CSS rules, which I identified and fixed. My solution solves the problem and makes the text in the Case Studies boxes now appear correctly. This is the second time I’ve encountered a situation where I’ve fixed an issue before someone else, but they managed to submit their PR first. So I am documenting my solution to show the work I did both identifying and solving this bug.
