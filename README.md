# Simple Form Project

## 1. Project Description

This is a simple contact form project created using HTML and CSS. Git and GitHub were used to track changes, manage versions, create branches, and restore previous versions.

## 2. Features

- User-friendly contact form
- Name, email and message fields
- Phone number field (added during the project)
- Arithmetic CAPTCHA input
- Simple and responsive design

## 3. Technologies Used

- HTML
- CSS
- JavaScript
- Git
- GitHub
- Visual Studio Code

## 4. Project Files

- `index.html`
- `style.css`
- `README.md`
- `simple-form/form.html`
- `simple-form/style.css`

## 5. Fixing the simple-form Folder Issue

### Problem
The original `simple-form` folder was stored as a Git submodule instead of a normal directory. This caused GitHub to display an arrow beside the folder.

### Solution
1. Removed the incorrect submodule reference.
2. Restored the normal `simple-form` directory.
3. Added `form.html` and `style.css`.
4. Staged and committed the corrected files.

### Git Commands Used

```bash
git rm --cached -f simple-form
git add simple-form/
git diff --cached --summary
git commit -m "Fix simple-form folder submodule issue"
```

### Result
The `simple-form` folder is now tracked as a normal directory containing `form.html` and `style.css`.

Commit: `c838b30`

## 6. Adding a Phone Number Field

### Objective
Add a phone number field to the contact form.

### Changes Made
- Added a Phone Number label.
- Added an input field using `type="tel"`.
- Made the phone number field required.
- Confirmed that the field displayed correctly in the browser.

### Result
The contact form was updated to collect the user's name, email address, phone number and message.

Commit: `f2eb9f8`

## 7. Viewing Git History

### Command Used

```bash
git log --oneline
```

### Purpose
To view the project's commit history in a short format.

### Result
The command displayed previous changes and their commit IDs.

## 8. Restoring a Previous Version of the Form

### Objective
Restore `form.html` to an earlier working version using Git.

### Command Used

```bash
git checkout c838b30 -- simple-form/form.html
```

### Result
The phone number field was removed, and the earlier version of the form was restored.

This demonstrates how Git can recover an earlier version of a file without deleting the project's commit history.

Commit: `5c2241d`

## 9. Creating a Feature Branch and Adding CAPTCHA

### Objective
Create a separate branch for adding CAPTCHA functionality.

### Branch Created

```bash
git switch -c feature-add-captcha
```

### Changes Made
- Added an arithmetic CAPTCHA question: What is 5 + 3?
- Added a number input field for the CAPTCHA answer.
- Added CSS styling for the CAPTCHA section.
- Added JavaScript intended to validate the submitted answer.

### Git Commands Used

```bash
git add simple-form/form.html simple-form/style.css
git commit -m "Add CAPTCHA to contact form"
git push -u origin feature-add-captcha
```

Commit: `9e9f489`

Note: The CAPTCHA field was displayed in the browser, but its JavaScript validation still requires final testing.

## 10. Merging the Feature Branch into Main

### Objective
Merge the CAPTCHA feature into the main branch.

### Git Commands Used

```bash
git switch main
git merge feature-add-captcha
git push origin main
```

### Result
The feature branch was successfully merged into `main`, and the changes were pushed to GitHub.

## 11. Discarding Unwanted CSS Changes

### Objective
Practise discarding uncommitted changes to the CSS file.

### Change Made
Added a temporary comment to `simple-form/style.css`.

### Git Commands Used

```bash
git status
git restore simple-form/style.css
git status
```

### Result
The temporary change was discarded, and the original committed CSS file was restored.

Git confirmed that the working tree was clean.

## 12. Pulling Updates from GitHub

### Command Used

```bash
git pull origin main
```

### Result
Git confirmed that the local repository was already up to date with the remote `main` branch.

## 13. Final Repository Status

### Command Used

```bash
git status
```

### Final Result

- Current branch: `main`
- Local branch: Up to date with `origin/main`
- Working tree: Clean
- No outstanding changes to commit.

## 14. Conclusion

This project demonstrates how Git and GitHub can be used to manage a simple web development project.

The exercise covered repository management, staging and committing files, viewing commit history, restoring previous versions, creating feature branches, merging changes, discarding unwanted changes and synchronising a local repository with GitHub.

## Author

Paul
