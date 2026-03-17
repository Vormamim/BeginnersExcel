# Lesson 7: IF Statements 🤔

**⏱️ Time:** About 30 minutes  
**What you'll learn:** How to make Excel show different things in a cell depending on a condition — like a smart decision-maker inside your spreadsheet!

---

## What is an IF Statement?

An **IF statement** is a formula that checks something and gives one answer if it's true, and a different answer if it's false.

Think of it like this:

> "**IF** it is raining, **THEN** take an umbrella, **OTHERWISE** wear sunglasses."

In Excel it looks like this:

```
=IF(condition, value_if_true, value_if_false)
```

**Three parts — always in this order:**
1. **Condition** — what Excel checks (e.g., is B2 greater than 50?)
2. **Value if TRUE** — what to show when the condition is met
3. **Value if FALSE** — what to show when the condition is not met

---

## Step 1 — Your First IF Formula

Let's try a simple example. A student **passes** if their score is 50 or above.

### Set Up the Data

Type this into a new spreadsheet starting at **A1**:

| | A | B | C |
|-|---|---|---|
| **1** | Student | Score | Result |
| **2** | Alex | 72 | |
| **3** | Blake | 45 | |
| **4** | Casey | 91 | |
| **5** | Dana | 38 | |
| **6** | Evan | 55 | |

### Write the IF Formula

1. Click on cell **C2**.
2. Type: `=IF(B2>=50,"Pass","Fail")`
3. Press **Enter**.
4. Cell C2 should show **Pass** (because 72 ≥ 50 ✅).

**Breaking down the formula:**
- `B2>=50` — the condition: "Is B2 greater than or equal to 50?"
- `"Pass"` — show this word if TRUE
- `"Fail"` — show this word if FALSE

> 💡 Text values in IF formulas always go inside **quotation marks** `" "`. Numbers do not need quotes.

---

## Step 2 — Copy the Formula Down

Now let's fill in C3 to C6 using the fill handle.

1. Click on **C2** (your formula cell).
2. Move your mouse to the **bottom-right corner** of C2 until you see the small **+** cursor.
3. **Click and drag** down to **C6**.
4. Release — all 5 students now show either "Pass" or "Fail"!

Check your results:
- Alex (72) → **Pass**
- Blake (45) → **Fail**
- Casey (91) → **Pass**
- Dana (38) → **Fail**
- Evan (55) → **Pass**

---

## Step 3 — IF with Numbers (not just text)

IF can also return a number. Let's calculate **bonus points**: students who score above 80 get +10 bonus points, others get +0.

1. Add a header **"Bonus"** in **D1**.
2. In **D2**, type: `=IF(B2>80,10,0)`
3. Copy down to **D6**.

Results:
- Alex (72) → **0** (not above 80)
- Blake (45) → **0**
- Casey (91) → **10** (above 80 ✅)
- Dana (38) → **0**
- Evan (55) → **0**

---

## Step 4 — Comparison Operators

You can use these symbols in your IF conditions:

| Symbol | Meaning | Example |
|--------|---------|---------|
| `>` | Greater than | `B2>80` |
| `<` | Less than | `B2<50` |
| `>=` | Greater than or equal to | `B2>=50` |
| `<=` | Less than or equal to | `B2<=100` |
| `=` | Equal to | `B2=100` |
| `<>` | Not equal to | `B2<>0` |

### Try It!
In column **E**, write an IF formula that shows **"Perfect!"** if the score is exactly 100, or **"Keep going!"** otherwise.

Formula: `=IF(B2=100,"Perfect!","Keep going!")`

---

## Step 5 — Practice with School Grades Data 🎓

Now let's use a real dataset!

1. Open [`../data/school_grades.csv`](../data/school_grades.csv) in Excel.
2. Find the **Math** column (column B).
3. Add a new column header **"Math Grade"** next to it (in the first empty column after the data).
4. In the first data row of that new column, type an IF formula:

```
=IF(B2>=90,"A",IF(B2>=80,"B",IF(B2>=70,"C","D")))
```

5. Copy that formula down for all students.

> 💡 **Nested IFs!** You can put an IF inside another IF. Excel checks the first condition, and if it's false, checks the next one, and so on. This lets you create multiple categories.

**How the nested IF works:**
- If Math ≥ 90 → **"A"**
- Else if Math ≥ 80 → **"B"**
- Else if Math ≥ 70 → **"C"**
- Otherwise → **"D"**

---

## Step 6 — IF with the Candy Data 🍬

1. Open [`../data/candy_data.csv`](../data/candy_data.csv) in Excel.
2. Look at the **Teeth Danger (1–5)** column.
3. Add a new column called **"Dentist Warning"**.
4. Use an IF formula: if the Teeth Danger rating is **4 or higher**, show **"⚠️ Be Careful!"**, otherwise show **"😊 OK"**.

Formula: `=IF(H2>=4,"⚠️ Be Careful!","😊 OK")`

*(Adjust the column letter to match where "Teeth Danger" actually is in your spreadsheet.)*

---

## Step 7 — IFS Function (Excel 2019 and later)

If you have a newer version of Excel, there's an even neater way to write multiple conditions: **IFS**.

**Syntax:**
```
=IFS(condition1, value1, condition2, value2, condition3, value3, …)
```

**Example — Letter Grade:**
```
=IFS(B2>=90,"A", B2>=80,"B", B2>=70,"C", B2>=60,"D", B2<60,"F")
```

This reads as: check each condition in order and return the matching value for the first true one.

### Try It!
In your school grades data, use IFS to assign a letter grade based on the **Science** column:
- 90 and above → **"A"**
- 80 and above → **"B"**
- 70 and above → **"C"**
- 60 and above → **"D"**
- Below 60 → **"F"**

---

## Step 8 — COUNTIF Review

You saw COUNTIF briefly in Lesson 5. Now you know how IF works, COUNTIF will make even more sense!

**COUNTIF counts cells that match a condition:**

```
=COUNTIF(range, condition)
```

**Examples:**
```
=COUNTIF(B2:B11,">=90")     ← counts students with Math ≥ 90
=COUNTIF(C2:C11,"Pass")     ← counts how many "Pass" results
```

### Try It!
At the bottom of your school grades spreadsheet, add:
1. `=COUNTIF(B2:B11,">=90")` — how many students got an A in Math?
2. `=COUNTIF(B2:B11,"<70")` — how many students are struggling in Math?

---

## ✅ Lesson 7 Recap

You learned:
- ✔️ `=IF(condition, value_if_true, value_if_false)` — the basic IF structure
- ✔️ Comparison operators: `>`, `<`, `>=`, `<=`, `=`, `<>`
- ✔️ IF can return text (in quotes) or numbers
- ✔️ **Nested IFs** — put IF inside IF for multiple categories
- ✔️ **IFS function** — a cleaner way to handle multiple conditions
- ✔️ **COUNTIF** — count cells that match a condition

---

## 🎯 Activity: Video Game Rating Classifier

1. Open [`../data/video_games.csv`](../data/video_games.csv) in Excel.
2. Find the **Copies Sold (millions)** column.
3. Add a new column called **"Popularity"**.
4. Use an IF formula (or IFS) to classify each game:
   - **200 million or more** → `"Mega Hit"`
   - **50 million or more** → `"Big Hit"`
   - **Less than 50 million** → `"Solid Performer"`
5. Copy the formula down for all games.
6. At the bottom, use COUNTIF to count how many games fall into each category.

---

➡️ **Next Lesson:** [Lesson 8 — VLOOKUP](lesson8-vlookup.md)  
⬅️ **Previous Lesson:** [Lesson 6 — Sorting and Filtering](lesson6-sorting-filtering.md)
