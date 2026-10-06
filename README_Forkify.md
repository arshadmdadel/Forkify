# Forkify: QA Testing Project

Manual QA project on **Forkify**, a recipe search and management web app, completed as part of the SQA training program at the A1QA training center (QATC).

## Overview

Forkify lets users search for recipes, view their details, adjust the number of servings, bookmark favorites, and upload their own recipes. This repository documents the testing performed and the defects found in version **1.0**.

## Application Features Under Test

- **Search**: find recipes by keyword.
- **Recipe view**: ingredients, preparation time, servings, publisher, and source link.
- **Servings control**: increase or decrease servings, with ingredient quantities updating to match.
- **Bookmarks**: add and remove recipes from a saved list.
- **Add recipe**: upload a recipe with title, URL, image URL, publisher, preparation time, servings, and up to six ingredients.

## Scope of Testing

| Type | Focus |
|------|-------|
| Functional | Search behavior, servings calculation, bookmarks, recipe upload, input validation, authentication |
| GUI | Label text and display after recipe actions |
| Negative / boundary | Empty input, negative and very large numbers, very long text, special characters, whitespace-only input, wrong ingredient format |

## Test Environment

| Item | Details |
|------|---------|
| OS | Windows 11 (64-bit) |
| Browser | Google Chrome 150.0.7871.115 |
| Application version | 1.0 |
| Defect tracking | Jira (project: Training Center, component: Forkify) |

## Defect Summary

**27 defects** were reported, all currently **Open**.

| Priority | Count |
|---|---|
| Major | 27 |

| Error type | Count |
|---|---|
| Functional | 25 |
| GUI | 2 |

### Defect categories

| Category | Examples |
|----------|----------|
| Search | Search is case-sensitive; searching by ingredient returns no recipes; endless loading spinner on an empty search |
| Servings and ingredients | Quantities do not match the servings value after revisiting a recipe; page freezes when servings is 0 and "+" is clicked; "Minutes" label becomes misspelled after upload or a servings change |
| Bookmarks | Re-bookmarked recipe missing from the list; unbookmarked recipe hard to find again; list does not scroll with many items; uploaded recipes are bookmarked automatically |
| Recipe upload: validation | Negative, very large, or non-numeric values accepted; very long titles accepted; missing or invalid URLs accepted; whitespace-only and special-character data accepted; ingredient rows can be missing values |
| Recipe upload: workflow | Wrong ingredient format blocks further uploads until the page is refreshed; cannot add a new recipe after a successful upload; "Add more" does not appear after six ingredient fields |
| Recipe management | No edit or delete for uploaded recipes; no dashboard to view uploaded recipes |
| Authentication | No login or registration, recipes can be added without authentication; no logout option |

## Defect Report Format

Each defect was logged in Jira with:

- Title and summary
- Steps to reproduce
- Actual result and expected result
- Environment (OS, browser)
- Priority, severity, and error type (Functional / GUI)
- Screenshots as attachments

## Skills Demonstrated

- Functional and GUI testing
- Input validation, boundary value, and negative testing
- Exploratory testing of user workflows (search, bookmark, upload)
- Clear, reproducible bug reporting
- Defect tracking in Jira

## Author

**Arshad Md. Adel**: SQA trainee, CSE graduate of United International University (UIU).
