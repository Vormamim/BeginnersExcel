# Lesson 6: Sorting and Filtering 🔢🔤

**⏱️ Time:** About 25 minutes  
**What you'll learn:** How to sort data alphabetically or numerically, and how to filter data to show only what you need

---

## Why Sort and Filter?

Imagine you have 100 rows of data — finding the student with the highest grade, or showing only the movies rated above 8, would take forever if you had to look manually. **Sorting** and **filtering** let Excel do that work for you in seconds!

- **Sorting** = puts your data in a specific order (A–Z, Z–A, lowest to highest, highest to lowest)
- **Filtering** = hides rows that don't match a condition so you only see what you care about

---

## Step 1 — Open the School Grades Data

1. Open [`../data/school_grades.csv`](../data/school_grades.csv) in Excel.
   - Click **File** → **Open** → find the file.
2. You'll see a table with student names and grades for different subjects.
3. **Bold the header row** (Row 1) and give it a colored background to make it stand out.

Your data should look something like this:

| Student Name | Math | Science | English | History | Art | PE |
|-------------|------|---------|---------|---------|-----|----|
| Alex Johnson | 92 | 88 | 95 | 85 | 90 | 98 |
| Blake Smith | 78 | 82 | 75 | 80 | 95 | 90 |
| … | … | … | … | … | … | … |

---

## Step 2 — Sort A to Z (Alphabetical Order)

Let's sort the students by name, A to Z.

1. Click on **any cell** inside your data (for example, cell **A2**).
2. Click the **Data** tab in the Ribbon.
3. Click the **Sort A to Z** button (it looks like **A↓Z** with an arrow).
4. Excel sorts the entire table alphabetically by the column you were in — Student Name!

> 💡 Excel is smart: when you sort one column, **all the other columns move with it** so your data stays matched up correctly.

### Try It!
Sort the students in **reverse alphabetical order** (Z to A):
1. Click any cell in the **Student Name** column (column A).
2. Click the **Sort Z to A** button (**Z↓A**) in the Data tab.
3. The list should now start with names near the end of the alphabet.

---

## Step 3 — Sort Numbers (Highest to Lowest)

Now let's find who has the highest Math score.

1. Click on any cell in the **Math** column (column B).
2. Click **Data** → **Sort Largest to Smallest** (the button with numbers and a down arrow: **9↓1**).
3. The student with the highest Math score jumps to the top!

### Try It!
Sort by **PE** score from **smallest to largest** (lowest score first):
1. Click any cell in the **PE** column.
2. Click **Data** → **Sort Smallest to Largest** (**1↑9**).
3. Who has the lowest PE score?

---

## Step 4 — Sort by Multiple Columns (Custom Sort)

What if you want to sort by **Genre**, and then by **Rating** within each genre? That's a **multi-level sort**!

1. Open [`../data/movies.csv`](../data/movies.csv) in Excel.
2. Click any cell inside the data.
3. Click the **Data** tab → **Sort** button (the big Sort button, not the A–Z shortcut).
4. The **Sort dialog box** opens.
5. Under **Sort by**, choose **Genre** from the dropdown. Keep order as **A to Z**.
6. Click **Add Level** at the top left of the dialog.
7. Under **Then by**, choose **Rating (out of 10)**. Change order to **Largest to Smallest**.
8. Click **OK**.

Now your movies are grouped by genre, and within each genre the highest-rated movie comes first!

---

## Step 5 — Adding a Filter

Filters are like a magic sieve — they hide the rows you don't need.

### Turn On AutoFilter

1. Go back to your **school_grades.csv** data.
2. Click on any cell inside the data (like **A1**).
3. Click the **Data** tab → **Filter** button (it looks like a funnel 🔽).
4. Small **dropdown arrows** (▾) appear in every header cell — that means filtering is on!

---

## Step 6 — Using a Filter

Let's say you want to see **only the movies with a Rating above 7.5**.

1. Open [`../data/movies.csv`](../data/movies.csv) in Excel.
2. Turn on **AutoFilter** (Data → Filter).
3. Click the dropdown arrow ▾ in the **Rating (out of 10)** column header.
4. A menu appears. Click **Number Filters** → **Greater Than…**
5. In the box that appears, type **7.5** and click **OK**.
6. Excel hides all movies with a rating of 7.5 or below — only the top-rated movies are visible!

> 💡 Notice that the row numbers on the left skip numbers — the hidden rows are still there, just not shown.

### Clear the Filter
1. Click the dropdown arrow ▾ on the **Rating** column again.
2. Click **Clear Filter From "Rating (out of 10)"**.
3. All movies reappear!

---

## Step 7 — Filter by Text

You can also filter by matching specific words.

1. With **movies.csv** open and AutoFilter on, click the dropdown arrow ▾ on the **Genre** column.
2. The filter list shows all unique genres. **Uncheck "Select All"** first (this deselects everything).
3. Then check **"Animation"** only.
4. Click **OK**.
5. Only Animation movies are shown!

### Turn Off AutoFilter
When you're done filtering, click **Data** → **Filter** again to remove all filters and show all rows.

---

## Step 8 — Practice with Video Games Data 🎮

1. Open [`../data/video_games.csv`](../data/video_games.csv) in Excel.
2. **Sort** the games from **most copies sold to fewest** (Copies Sold column, Largest to Smallest).
3. Turn on **AutoFilter**.
4. Filter the **Genre** column to show only **"Sandbox"** games.
5. How many Sandbox games are in the list?
6. Clear the filter when you're done.

---

## ✅ Lesson 6 Recap

You learned:
- ✔️ **Sorting A–Z / Z–A** — put text data in alphabetical order
- ✔️ **Sorting Largest to Smallest / Smallest to Largest** — order numbers
- ✔️ **Multi-level Sort** — sort by more than one column at a time
- ✔️ **AutoFilter** — add dropdown arrows to column headers
- ✔️ **Number Filters** — show only rows matching a condition (e.g., > 7.5)
- ✔️ **Text Filters** — show only rows matching a specific word

---

## 🎯 Activity: Top Students Report

1. Open [`../data/school_grades.csv`](../data/school_grades.csv) in Excel.
2. **Sort** by the **Math** column from highest to lowest. Who are the top 3 Math students?
3. Turn on **AutoFilter** and filter the **Math** column to show only students who scored **90 or above** (Number Filters → Greater Than Or Equal To → 90).
4. How many students scored 90+ in Math?
5. Now clear that filter and filter the **Science** column instead — who scored 90+ in Science?

---

➡️ **Next Lesson:** [Lesson 7 — IF Statements](lesson7-if-statements.md)  
⬅️ **Previous Lesson:** [Lesson 5 — Fun Projects](lesson5-fun-projects.md)
