
# Simple Form Project

## Project Description
This is a simple contact form project created using HTML and CSS.

## Features
- User-friendly contact form
- Simple design
- Responsive layout

## Technologies Used
- HTML
- CSS

## Project Files
- index.html
- style.css

## Author
Paul


## Fixing the simple-form Folder Issue

### Problem
The original simple-form folder was stored as a Git submodule instead of a normal directory. This caused GitHub to display an arrow beside the folder.

### Solution
1. Removed the incorrect submodule reference.
2. Restored the normal simple-form directory.
3. Added form.html and style.css.
4. Staged and committed the corrected files.

### Git Commands Used
```bash
git rm --cached -f simple-form
git add simple-form/
git diff --cached --summary
git commit -m "Fix simple-form folder submodule issue"
```

### Result
The simple-form folder is now tracked as a normal directory containing form.html and style.css.

Commit: c838b30
## Adding a Phone Number Field

### Objective
Add a phone number field to the contact form.

### Changes Made
- Added a Phone Number label.
- Added an input field using type="tel".
- Made the phone number field required.
- Confirmed that the field displays correctly in the browser.

### Result
The contact form now collects the user's name, email address, phone number and message.