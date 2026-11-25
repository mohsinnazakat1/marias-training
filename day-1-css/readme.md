
# Round 1 – CSS Foundations

## Part E: Specificity Puzzle

### 1. My Predictions (Before Browser Testing)

| Paragraph | Expected Color | Winning Selector | Specificity (IDs, Classes, Elements) |
|---|---|---|---|
| First | green| #box p | (0,1,0) |
| Second | green | #box p  |  (1,0,1) |
| Third | green | #box p | (1,0,1) |

### 2. Browser Testing Results

| Paragraph | Actual Color | Winning Selector | Was My Prediction Correct? |
|---|---|---|---|
| First | green | #box p| (1,0,1)
| Second | green | #box p | (1,0,1) |
| Third | orange | inline | inline|
no

### 3. After Removing the `#box p` Rule

| Paragraph | Expected Color | Winning Selector | Specificity |
|---|---|---|---|
| First | purple |
| Second | purple | 
| Third | orange | 
### 4. Explanation
Because .note.important and .panel .note have the same specificity, the rule written later in the CSS file wins.
**Q: Two rules have exactly the same specificity. How does the browser decide?**

My explanation:
When two CSS rules have exactly the same specificity, the browser applies the rule that is written last in the stylesheet.

### 5. What I Learned

- What I learned about Cascade:The cascade is the process CSS uses to decide which style rule should be applied when multiple rules target the same element.
- What I learned about Specificity:Inheritance means some CSS properties, such as color and font-family, are passed from a parent element to its child elements.
- What I learned about Inheritance:When two CSS rules have the same specificity, the rule written later in the stylesheet wins.
- What I found difficult: I had some difficulty understanding inline styles, inheritance, and specificity.
- How I solved it:I reviewed examples, practiced with CSS selectors, and checked the results using Chrome DevTools.
