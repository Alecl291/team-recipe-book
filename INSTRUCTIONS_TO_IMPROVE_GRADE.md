# URGENT: Instructions to Improve Your Team Grade

**Current Grade: C+ (78/100)**
**Potential Grade with Fixes: B+ to A- (87-92/100)**

---

## Critical Issues That Must Be Fixed

Your recipe book has good content, but several technical errors are preventing it from working properly. Follow these steps to fix them and improve your grade.

---

## STEP 1: Fix CSS Filename (5 minutes) - CRITICAL

**Problem:** Your CSS file is named `Style,css` (with a comma) instead of `Style.css` (with a period). This means the styling won't load in about.html.

**Fix:**
```bash
git mv Style,css Style.css
git commit -m "Fix CSS filename - change comma to period"
```

**Then update about.html line 7:**
- Current: `<link rel="stylesheet" href="Style.css">`
- Already correct, no change needed once file is renamed

---

## STEP 2: Fix Broken Links in index.html (5 minutes) - CRITICAL

**Problem:** Lines 16, 18, 20, and 22 have GitHub URLs as plain text that shouldn't be there.

**Fix:**
Open `index.html` and **DELETE** these 4 lines:
- Line 16: `https://github.com/Alecl291/team-recipe-book/blob/main/Alec-burgerRecipe.html`
- Line 18: `https://github.com/Alecl291/team-recipe-book/blob/main/Luckyo-recipe.html`
- Line 20: `https://github.com/Alecl291/team-recipe-book/blob/main/Samuel-recipe.html`
- Line 22: `https://github.com/Alecl291/team-recipe-book/blob/main/hamza-recipe.html`

**The file should look like this:**
```html
<h2>Our Recipes:</h2>
<ul>
    <li><a href="Alec-burgerRecipe.html">Alec's Burger Recipe</a></li>
    <li><a href="Luckyo-recipe.html">Homemade Einsteins Bagel</a></li>
    <li><a href="Samuel-recipe.html">Cookie Recipe</a></li>
    <li><a href="hamza-recipe.html">Hamza's Shawarma</a></li>
</ul>
```

**Commit:**
```bash
git add index.html
git commit -m "Remove broken GitHub URL links from index"
```

---

## STEP 3: Fix Broken Links in about.html (5 minutes) - CRITICAL

**Problem:** The navigation links on lines 14 and 15 point to files that don't exist.

**Fix:**
Open `about.html` and fix these lines:

**Line 14 - Change:**
```html
<a href="Samuel's Cookie Recipe.html">Samuel's Cookies</a>
```
**To:**
```html
<a href="Samuel-recipe.html">Samuel's Cookies</a>
```

**Line 15 - Change:**
```html
<a href="hamza-recipe.html.txt">Hamza's Shawarma</a>
```
**To:**
```html
<a href="hamza-recipe.html">Hamza's Shawarma</a>
```

**Commit:**
```bash
git add about.html
git commit -m "Fix navigation links to correct filenames"
```

---

## STEP 4: Fix HTML Formatting in Alec's Recipe (3 minutes)

**Problem:** Lines 15-18 and 25-30 in `Alec-burgerRecipe.html` use `<i>` (italics) tags instead of `<li>` (list item) tags.

**Fix:**
Open `Alec-burgerRecipe.html` and replace ALL `<i>` tags with `<li>`:

**In the Ingredients section (lines 15-18), change:**
```html
<i>1/4 cup of Beef Broth</i>
<i>American Cheese</i>
<i>Cooking oil</i>
<i>Burger Buns</i>
```
**To:**
```html
<li>1/4 cup of Beef Broth</li>
<li>American Cheese</li>
<li>Cooking oil</li>
<li>Burger Buns</li>
```

**In the Instructions section (lines 25-30), change all `<i>` to `<li>`**

**Commit:**
```bash
git add Alec-burgerRecipe.html
git commit -m "Fix HTML list formatting in burger recipe"
```

---

## STEP 5: Add CSS Styling to All Recipe Pages (10 minutes)

**Problem:** Only `about.html` has CSS linked. Recipe pages have no styling.

**Fix:**
Add this line to the `<head>` section of each recipe file:
```html
<link rel="stylesheet" href="Style.css">
```

**Files that need this:**
- `Alec-burgerRecipe.html`
- `Luckyo-recipe.html`
- `Samuel-recipe.html`
- `hamza-recipe.html` (already has `style.css` - change to `Style.css` to match)

**For hamza-recipe.html line 6, change:**
```html
<link rel="stylesheet" href="style.css">
```
**To:**
```html
<link rel="stylesheet" href="Style.css">
```

**Commit:**
```bash
git add *.html
git commit -m "Add CSS styling to all recipe pages"
```

---

## STEP 6: Add Navigation to All Pages (15 minutes)

**Problem:** Recipe pages have no way to navigate back to home or other recipes.

**Fix:**
Add this navigation bar right after the `<body>` tag in each recipe file:

```html
<nav>
    <a href="index.html">Home</a>
    <a href="Alec-burgerRecipe.html">Alec's Burger</a>
    <a href="Luckyo-recipe.html">LuckyO's Bagel</a>
    <a href="Samuel-recipe.html">Samuel's Cookies</a>
    <a href="hamza-recipe.html">Hamza's Shawarma</a>
    <a href="about.html">About Team</a>
</nav>
```

**Add to these files:**
- `Alec-burgerRecipe.html`
- `Luckyo-recipe.html`
- `Samuel-recipe.html`

**Note:** `hamza-recipe.html` already has a back link, but adding full navigation would be better.

**Commit:**
```bash
git add *.html
git commit -m "Add navigation menu to all recipe pages"
```

---

## STEP 7: Improve README.md (5 minutes)

**Problem:** README is too basic and doesn't describe the project.

**Fix:**
Replace the current README.md content with:

```markdown
# Team Recipe Book 🍔🥯🍪🥙

A collaborative recipe collection created by Group 7 for CSCE 1015.

## Team Members
- **Alec Lara** (EUID: alec291) - Burger Master
- **Lucky Onyedebelu** (EUID: lucky0) - Bagel Artist
- **Samuel Solis** (EUID: samuel123) - Cookie Scientist
- **Hamza Shakur** (EUID: 0062) - Shawarma King

## Recipes Included
1. Alec's Juicy Burger Recipe
2. LuckyO's Homemade Einstein Bagel
3. Samuel's Chocolate Chip Cookies
4. Hamza's Authentic Shawarma

## How to View
1. Clone this repository
2. Open `index.html` in your web browser
3. Navigate through our recipes using the menu

## Technologies Used
- HTML5
- CSS3
- Git & GitHub for team collaboration

## Project Stats
- 4 recipes created
- Professional CSS styling
- Responsive navigation
- About page with team info

---
Built with teamwork and delicious food! 🍽️
```

**Commit:**
```bash
git add README.md
git commit -m "Improve README with project details and team info"
```

---

## STEP 8: **LUCKY - YOU MUST CONTRIBUTE** (30-45 minutes) - REQUIRED FOR PASSING GRADE

**Problem:** Lucky Onyedebelu has **ZERO commits**. Your recipe file exists but was created by Alec, not you.

**Current Grade: F (0%)**
**Possible Grade with Work: B (80-85%)**

### What Lucky Must Do:

#### Option 1: Enhance Your Existing Recipe (Easier - 30 min)
1. Open `Luckyo-recipe.html`
2. Add detailed ingredients with measurements
3. Add step-by-step cooking instructions
4. Add an image of bagels using:
```html
<img src="https://images.unsplash.com/photo-1555507036-ab1f4038808a?w=400" alt="Homemade Bagels">
```
5. Add CSS link and navigation (from Steps 5 & 6 above)
6. Make it the most detailed recipe on the team
7. **Commit YOUR changes using YOUR GitHub account:**
```bash
git add Luckyo-recipe.html
git commit -m "Complete bagel recipe with detailed instructions - Lucky"
git push origin main
```

#### Option 2: Create a New Feature (Better - 45 min)
1. Create a new file called `tips.html` with cooking tips from each team member
2. Add a "Tips & Tricks" section with:
   - Burger tips from Alec
   - Bagel tips from you
   - Cookie tips from Samuel
   - Shawarma tips from Hamza
3. Link it in the navigation
4. Style it with CSS
5. **Commit using YOUR account:**
```bash
git add tips.html
git commit -m "Add cooking tips page - Lucky"
git push origin main
```

#### Option 3: Improve Team Infrastructure (Best - 45 min)
1. Fix ALL the issues in Steps 1-7 above yourself
2. Test all the links work
3. Add a footer to every page
4. Make commits for each fix using YOUR GitHub account
5. This shows initiative and technical skill

**WARNING:** You MUST make at least 5 meaningful commits using your own GitHub account, or you will fail this project. Your teammates cannot do the work for you.

---

## STEP 9: Fix Hamza's Multiple GitHub Accounts (2 minutes)

**Problem:** Hamza is using 3 different accounts: FIRMz, HamzaShakur, hamza12330-lab

**Fix:**
Hamza should pick ONE account (recommend: HamzaShakur) and configure git:
```bash
git config user.name "HamzaShakur"
git config user.email "your-email@example.com"
```

Use only this account for all future commits.

---

## STEP 10: Push All Changes to GitHub

After completing all fixes:

```bash
git status  # Check what you've changed
git add .   # Stage all changes
git commit -m "Fix all critical issues - improve recipe book"
git push origin main
```

**Then verify on GitHub:**
- CSS file is named correctly
- All links work
- Navigation appears on all pages
- README looks professional
- Lucky has made commits

---

## Grade Improvement Breakdown

| Task | Points | Who Should Do It |
|------|--------|------------------|
| Fix CSS filename | +3 | Alec |
| Fix broken links in index | +3 | Alec |
| Fix broken links in about | +2 | Alec |
| Fix HTML formatting | +2 | Alec |
| Add CSS to all pages | +3 | Hamza or Samuel |
| Add navigation | +4 | Hamza or Samuel |
| Improve README | +2 | Samuel |
| Lucky's contribution | +15 | **LUCKY** |
| Consolidate accounts | +1 | Hamza |

**Total Possible: +35 points**

**New Grade if ALL completed: 78 + 14 = 92/100 (A-)**
**Lucky's individual grade: 0 + 80 = 80/100 (B-)** if he does substantial work

---

## Timeline

**Complete these fixes within 48 hours to receive full grade improvement.**

**Minimum Required (for C to B):**
- Steps 1, 2, 3, 4 (critical bugs) - 18 minutes
- Lucky makes at least 5 commits - 30 minutes

**Recommended for Full Credit (B+ to A-):**
- All steps 1-10 completed
- Lucky contributes significantly
- All links tested and working

---

## Questions?

If you get stuck:
1. Check that you're in the correct directory: `pwd`
2. Make sure you have the latest code: `git pull origin main`
3. Test your changes by opening `index.html` in a browser
4. Verify each link clicks through correctly

**IMPORTANT:** Lucky must participate or risk failing the project. Everyone else should help fix the technical issues.

Good luck! Your team has good content - you just need to fix the technical errors and ensure everyone participates.
