# Lesson 8: VLOOKUP 🔍

**⏱️ Time:** About 35 minutes  
**What you'll learn:** How to search for a value in a table and automatically pull back related information — like looking something up in a phone book!

---

## What is VLOOKUP?

**VLOOKUP** stands for **Vertical Lookup**. It searches down the **first column** of a table to find a value you specify, and then returns something from the **same row** in another column.

**Real-life analogy:** Imagine you have a class list with names and grades. You type a student's name and Excel instantly finds their grade — no scrolling needed!

**Syntax:**
```
=VLOOKUP(lookup_value, table_array, col_index_num, [range_lookup])
```

**The four parts:**

| Part | What It Means | Example |
|------|--------------|---------|
| `lookup_value` | The value you're searching for | `"Alex"` or cell `A2` |
| `table_array` | The table to search in | `A1:F20` |
| `col_index_num` | Which column number to return (1 = first column, 2 = second, etc.) | `3` |
| `range_lookup` | `FALSE` = exact match, `TRUE` = approximate match | `FALSE` |

> 💡 **Always use FALSE** as the fourth argument unless you specifically need approximate matching. Exact match (FALSE) is what beginners need almost every time.

---

## Step 1 — A Simple VLOOKUP Example

Let's build a lookup tool for student grades.

### Set Up Sheet 1 (Data Table)

Open a new spreadsheet. On **Sheet1**, type this data starting at **A1**:

| | A | B | C |
|-|---|---|---|
| **1** | Student Name | Math | Science |
| **2** | Alex | 92 | 88 |
| **3** | Blake | 78 | 82 |
| **4** | Casey | 95 | 91 |
| **5** | Dana | 65 | 70 |
| **6** | Evan | 88 | 84 |

### Set Up a Lookup Area

In a different spot on the same sheet (for example, starting at **E1**), type:

| | E | F |
|-|---|---|
| **1** | Look up student: | |
| **2** | Casey | |

Now in **F2**, type this VLOOKUP formula to find Casey's **Math** score:

```
=VLOOKUP(E2, A1:C6, 2, FALSE)
```

Press **Enter** — it should show **95**!

**What happened?**
- `E2` = the name to search for ("Casey")
- `A1:C6` = the table to search in
- `2` = return the value from column 2 (Math)
- `FALSE` = exact match only

### Try It!
Change **E2** to **"Blake"** — the formula instantly updates to show Blake's Math score (**78**)!

---

## Step 2 — Looking Up Different Columns

To get **Science** instead of Math, just change the column number:

```
=VLOOKUP(E2, A1:C6, 3, FALSE)
```

- Column 1 = Student Name
- Column 2 = Math  
- Column 3 = Science

Now it returns the Science score for whoever is in E2.

---

## Step 3 — VLOOKUP Across the School Grades Data

1. Open [`../data/school_grades.csv`](../data/school_grades.csv) in Excel.
2. Look at the columns — Student Name is column 1, Math is column 2, Science is column 3, English is column 4, History is column 5, Art is column 6, PE is column 7.
3. In an empty area (for example, starting at **I1**), set up a lookup panel:

| | I | J |
|-|---|---|
| **1** | Student: | Georgia Moore |
| **2** | Math: | `=VLOOKUP(J1, A:G, 2, FALSE)` |
| **3** | Science: | `=VLOOKUP(J1, A:G, 3, FALSE)` |
| **4** | English: | `=VLOOKUP(J1, A:G, 4, FALSE)` |
| **5** | History: | `=VLOOKUP(J1, A:G, 5, FALSE)` |
| **6** | Art: | `=VLOOKUP(J1, A:G, 6, FALSE)` |
| **7** | PE: | `=VLOOKUP(J1, A:G, 7, FALSE)` |

4. Type in **J1**: `Georgia Moore`
5. All 6 subject grades appear instantly!
6. Change **J1** to another student name — all grades update automatically!

> 💡 Using `A:G` (entire columns) instead of a specific range like `A1:G11` means you don't have to worry about the exact range — Excel searches the whole column.

---

## Step 4 — VLOOKUP Across Two Sheets

A very common use of VLOOKUP is pulling data from one sheet into another.

### Set Up Two Sheets

1. In your school grades file, right-click the **Sheet1** tab at the bottom.
2. Click **"Insert"** → **"Worksheet"** → **OK** (or click the **+** button next to the sheet tabs).
3. You now have **Sheet1** (the grades data) and **Sheet2** (empty).

### Create a Summary on Sheet 2

1. Click on **Sheet2**.
2. In **A1**, type: `Enter student name:`
3. In **B1**, type: `Alex Johnson`
4. In **A3**, type: `Math Score:`
5. In **B3**, type this formula:

```
=VLOOKUP(B1, Sheet1!A:G, 2, FALSE)
```

**Notice `Sheet1!` before `A:G`** — this tells Excel to look in Sheet1's columns A to G.

6. Press Enter — Alex Johnson's Math score appears on Sheet2!
7. Add more rows for other subjects by changing the column number (3 for Science, 4 for English, etc.).

---

## Step 5 — Handling "Not Found" Errors

If you type a name that doesn't exist in the table, VLOOKUP shows an ugly **#N/A** error. We can fix that!

Wrap your VLOOKUP in an **IFERROR** function:

```
=IFERROR(VLOOKUP(E2, A1:C6, 2, FALSE), "Student not found")
```

**How IFERROR works:**
- If the VLOOKUP works correctly → show the result
- If there's any error → show "Student not found" instead

### Try It!
1. In your lookup panel, change the student name to something that doesn't exist (like "Zzz Zzz").
2. Without IFERROR you see `#N/A`. With IFERROR you see "Student not found".

---

## Step 6 — VLOOKUP with the Movies Data 🎬

1. Open [`../data/movies.csv`](../data/movies.csv) in Excel.
2. Your columns are: Movie Title, Year, Genre, Runtime (min), Rating (out of 10), Age Rating, Fun Level (1-10).
3. In an empty area (say, column **I**), set up a movie lookup:

| | I | J |
|-|---|---|
| **1** | Movie Title: | Moana |
| **2** | Rating: | `=IFERROR(VLOOKUP(J1, A:G, 5, FALSE), "Not found")` |
| **3** | Genre: | `=IFERROR(VLOOKUP(J1, A:G, 3, FALSE), "Not found")` |
| **4** | Fun Level: | `=IFERROR(VLOOKUP(J1, A:G, 7, FALSE), "Not found")` |

4. Type in **J1**: `Moana`
5. The rating, genre, and fun level appear!
6. Try changing the movie name to see the details update.

---

## Step 7 — VLOOKUP with the Candy Data 🍬

1. Open [`../data/candy_data.csv`](../data/candy_data.csv) in Excel.
2. Columns: Candy Name, Type, Sugar (grams), Calories, Price ($), Fun Colors?, Rating (1-10), Teeth Danger (1-5).
3. Set up a candy lookup in an empty area:

| | I | J |
|-|---|---|
| **1** | Candy: | Skittles |
| **2** | Calories: | `=IFERROR(VLOOKUP(J1, A:H, 4, FALSE), "Not found")` |
| **3** | Price: | `=IFERROR(VLOOKUP(J1, A:H, 5, FALSE), "Not found")` |
| **4** | Rating: | `=IFERROR(VLOOKUP(J1, A:H, 7, FALSE), "Not found")` |

4. Try changing **J1** to other candy names from the list!

---

## ✅ Lesson 8 Recap

You learned:
- ✔️ VLOOKUP searches down the **first column** of a table for a value
- ✔️ Syntax: `=VLOOKUP(lookup_value, table_array, col_index_num, FALSE)`
- ✔️ The **column number** tells VLOOKUP which column to return
- ✔️ Always use **FALSE** for exact matches
- ✔️ Use **Sheet1!** before the range to look up data on another sheet
- ✔️ Wrap with **IFERROR** to handle "not found" situations gracefully

---

## 🎯 Activity: Video Game Info Finder

1. Open [`../data/video_games.csv`](../data/video_games.csv) in Excel.
2. Your columns are: Rank, Game Title, Platform, Genre, Year, Copies Sold (millions), Publisher, Note.
3. In an empty area, create a "Game Lookup" panel:
   - A cell where you type the **Game Title**
   - A cell that uses VLOOKUP to show the **Platform**
   - A cell that uses VLOOKUP to show the **Genre**
   - A cell that uses VLOOKUP to show **Copies Sold**
   - A cell that uses VLOOKUP to show the **Publisher**
4. Wrap every VLOOKUP in IFERROR so you get a friendly message if the game isn't found.
5. Test it by looking up: `Minecraft`, `Tetris`, and `Hollow Knight`.

---

➡️ **Next Lesson:** [Lesson 9 — Conditional Formatting](lesson9-conditional-formatting.md)  
⬅️ **Previous Lesson:** [Lesson 7 — IF Statements](lesson7-if-statements.md)
