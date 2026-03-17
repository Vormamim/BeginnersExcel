# Lesson 9: Conditional Formatting 🎨

**⏱️ Time:** About 25 minutes  
**What you'll learn:** How to make Excel automatically color cells, add icons, and highlight data based on rules — so important information jumps out at you!

---

## What is Conditional Formatting?

**Conditional Formatting** tells Excel: *"If a cell meets this condition, apply this format automatically."*

Instead of manually coloring each cell, you set a rule once and Excel handles it for every cell in the range — even if the data changes later!

**Examples of what you can do:**
- Turn all failing grades **red** automatically
- Turn all top scores **green**
- Add a color gradient from low (red) to high (green) across a column
- Add traffic-light icons (🔴🟡🟢) based on values

---

## Step 1 — Highlight Cells Greater Than a Value

Let's start with the most common use: highlighting high scores.

### Set Up the Data

Open [`../data/school_grades.csv`](../data/school_grades.csv) in Excel, or type this into a new spreadsheet:

| | A | B |
|-|---|---|
| **1** | Student | Math |
| **2** | Alex | 92 |
| **3** | Blake | 78 |
| **4** | Casey | 95 |
| **5** | Dana | 65 |
| **6** | Evan | 88 |
| **7** | Finley | 72 |
| **8** | Georgia | 98 |
| **9** | Hunter | 80 |
| **10** | Iris | 85 |
| **11** | Jordan | 75 |

### Apply the Rule

1. **Select the Math scores** — click **B2**, hold **Shift**, click **B11**.
2. Click the **Home** tab in the Ribbon.
3. Click **Conditional Formatting** → **Highlight Cells Rules** → **Greater Than…**
4. In the box that appears, type **90**.
5. In the format dropdown next to it, choose **"Green Fill with Dark Green Text"**.
6. Click **OK**.

All scores above 90 (92, 95, 98) are now highlighted green! 🟢

---

## Step 2 — Highlight Low Scores in Red

Now let's highlight struggling students.

1. With **B2:B11** still selected (or re-select it).
2. Click **Conditional Formatting** → **Highlight Cells Rules** → **Less Than…**
3. Type **70** in the box.
4. Choose **"Light Red Fill with Dark Red Text"**.
5. Click **OK**.

Scores below 70 (65) are now red! 🔴

> 💡 You can apply **multiple rules** to the same range. Excel checks all of them and applies whichever rules match.

---

## Step 3 — Between Values

What if you want to highlight scores in the **70–79 range** (a "C" grade) in yellow?

1. Select **B2:B11**.
2. Click **Conditional Formatting** → **Highlight Cells Rules** → **Between…**
3. Type **70** in the first box and **79** in the second box.
4. Choose **"Yellow Fill with Dark Yellow Text"** (or choose "Custom Format…" and pick yellow fill manually).
5. Click **OK**.

Now your column has a traffic-light look: red (failing), yellow (C grade), green (A grade)! 🚦

---

## Step 4 — Color Scales (Gradient Colors)

A **Color Scale** automatically shades an entire column from one color to another based on value. No manual rules needed!

### Apply a Color Scale to All Subjects

1. Open [`../data/school_grades.csv`](../data/school_grades.csv) in Excel.
2. Select all the grade columns (for example, **B2:G11** — all subject scores for all students).
3. Click **Conditional Formatting** → **Color Scales**.
4. Choose the **Green-Yellow-Red** color scale (the first option in the top row).

Now:
- The **highest scores** are dark green
- **Middle scores** are yellow
- The **lowest scores** are red

You can instantly see patterns across all subjects at a glance!

---

## Step 5 — Data Bars

**Data Bars** add a mini bar chart inside each cell — the longer the bar, the bigger the value.

1. Select the **Calories** column in [`../data/candy_data.csv`](../data/candy_data.csv) (after opening it in Excel).
2. Select all the calorie values (not the header).
3. Click **Conditional Formatting** → **Data Bars**.
4. Choose a color you like (blue is the default).

Each candy's calorie value now has a bar showing how it compares to the others — no chart needed!

---

## Step 6 — Icon Sets

**Icon Sets** place small icons inside cells based on their values (like stars, arrows, or traffic lights).

### Try It with Sports Scores

1. Open [`../data/sports_scores.csv`](../data/sports_scores.csv) in Excel.
2. Select the **Goals Scored** column values (not the header).
3. Click **Conditional Formatting** → **Icon Sets**.
4. Choose **"3 Traffic Lights (Unrimmed)"** or the **3-star** icon set.

Excel divides the values into thirds:
- Top third gets a green icon 🟢
- Middle third gets a yellow icon 🟡
- Bottom third gets a red icon 🔴

---

## Step 7 — Creating a Custom Rule

You can write your own rule using a formula. This gives you total control!

### Example: Highlight the Entire Row

Let's highlight the **entire row** for any candy with a Teeth Danger rating of 4 or above.

1. Open [`../data/candy_data.csv`](../data/candy_data.csv) in Excel.
2. Select all the data rows — click **A2**, hold **Shift**, and click the last cell in the last row.
3. Click **Conditional Formatting** → **New Rule…**
4. Choose **"Use a formula to determine which cells to format"**.
5. In the formula box, type (adjust column letter to match your Teeth Danger column — it's column H):

```
=$H2>=4
```

6. Click **Format…**, click the **Fill** tab, choose an **orange** color, click **OK**.
7. Click **OK** again.

Any row where Teeth Danger is 4 or 5 is now highlighted orange across the whole row! 🟠

> 💡 **The $ before the column letter is important!** `$H2` means "always look in column H, but move down the rows". This is called a **mixed reference** and is what makes the rule apply to each row correctly.

---

## Step 8 — Managing and Deleting Rules

If you have multiple rules and want to see, edit, or remove them:

1. Select the cells that have conditional formatting applied.
2. Click **Conditional Formatting** → **Manage Rules…**
3. A list of all rules for the selected range appears.
4. You can:
   - **Edit** a rule — click it and click **Edit Rule…**
   - **Delete** a rule — click it and click **Delete Rule**
   - **Change priority** — use the ▲▼ buttons (rules at the top apply first)
5. Click **OK** when done.

### Clear All Rules from a Range
1. Select the cells.
2. Click **Conditional Formatting** → **Clear Rules** → **Clear Rules from Selected Cells**.

---

## Step 9 — Practice with Movie Ratings 🎬

1. Open [`../data/movies.csv`](../data/movies.csv) in Excel.
2. Select the **Rating (out of 10)** column values.
3. Apply these three Conditional Formatting rules:
   - **Greater than 8** → **Green fill** (great film!)
   - **Between 7 and 8** → **Yellow fill** (pretty good)
   - **Less than 7** → **Red fill** (not your favorite)
4. Now you can see at a glance which movies are top-rated!
5. Also apply a **Color Scale** to the **Fun Level (1-10)** column.

---

## ✅ Lesson 9 Recap

You learned:
- ✔️ **Highlight Cells Rules** — color cells greater than, less than, or between values
- ✔️ **Color Scales** — gradient colors automatically showing high vs. low values
- ✔️ **Data Bars** — mini bar charts inside cells
- ✔️ **Icon Sets** — traffic lights, stars, or arrows based on value
- ✔️ **Custom formula rules** — highlight entire rows using a formula with `$`
- ✔️ **Manage Rules** — view, edit, prioritize, or delete conditional formatting rules

---

## 🎯 Activity: Student Performance Dashboard

1. Open [`../data/school_grades.csv`](../data/school_grades.csv) in Excel.
2. Apply a **Color Scale** (Green-Yellow-Red) to all subject scores (**B2:G11**).
3. Apply a **Highlight Cells Rule** to the **Math** column:
   - Scores **≥ 90** → **Green fill**
   - Scores **< 70** → **Red fill**
4. Apply **Data Bars** to the **PE** column so you can visually compare students.
5. Use **Icon Sets** (traffic lights) on the **Science** column.
6. Take a moment to look at your colorful spreadsheet — what patterns do you notice? Which students are consistently strong? Which might need some extra help?

---

## 🎓 Congratulations — You've Levelled Up!

You've now completed all 9 lessons! Here's your full skill list:

| Skill | ✅ |
|-------|---|
| Navigate the Excel UI | ✔️ |
| Enter and edit data | ✔️ |
| Format cells (bold, color, alignment) | ✔️ |
| Use basic formulas (SUM, AVERAGE, MAX, MIN) | ✔️ |
| Create charts and graphs | ✔️ |
| Build real spreadsheet projects | ✔️ |
| Sort and filter data | ✔️ |
| Write IF statements and nested IFs | ✔️ |
| Use VLOOKUP to search tables | ✔️ |
| Apply conditional formatting | ✔️ |

### What Could You Explore Next?

- **PivotTables** — summarize large datasets with a few clicks
- **Named Ranges** — give your data ranges friendly names
- **Data Validation** — control what people can type into cells
- **Macros & VBA** — automate repetitive tasks with code

---

⬅️ **Previous Lesson:** [Lesson 8 — VLOOKUP](lesson8-vlookup.md)  
🏠 **Back to Start:** [README](../README.md)
