# CSS Round 1 — CSS Foundations

## Part A — Base Styles

- Used `box-sizing: border-box` for all elements.
- Used `font: inherit` for form controls.
- Created 4 CSS variables in `:root`.
- Created a page container with a maximum width of 720px.
- Used margin auto to center the page.

## Part B — Course Card

- Created a course card with a width of 320px.
- Added 24px padding and a border.
- Added rounded corners and a white background.
- Added an image placeholder with 160px height.
- Added a category, title, description and price.
- Used 32px margin between cards.
- Created multiple cards using the same CSS class.

## Part C — Buttons and States

- Added an Enroll button and a Details link.
- Used `inline-block` for the Details link.
- Added hover styling to both actions.
- Added focus-visible styling for keyboard navigation.
- Added disabled styling for the Course Full button.
- Tested buttons and links using mouse and keyboard.

## Part D — Three Cards and Featured Modifier

- Created three cards with different course content.
- Added `course-card--featured` to one card.
- Added a Featured label.
- Used a thicker brand-colored border for the featured card.
- Used higher specificity for the featured modifier without `!important`.


## Part F — Box Model Notes

### Content-box

- Width: 320px
- Padding: 24px on each side.
- Border: 1px on each side.

Calculation:

320 + 48 + 2 = **370px**

### Border-box

- Total width: 320px.
- Padding and border are included in the total width.

Calculation:

320 - 48 - 2 = **270px content width**

### DevTools Screenshot



### Why did the Details link need a display change?

The anchor is inline by default, so its width does not work properly. I used `inline-block` to make width and padding work correctly.

### How does the featured card win over the base card?

The featured modifier uses higher specificity than the base card selector, so its border styling wins without `!important`.

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
