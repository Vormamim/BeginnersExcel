# Lesson 3: Basic Formulas 🧮

**⏱️ Time:** About 30 minutes  
**📚 What you'll learn:** How to use Excel formulas to add, average, and analyze numbers — no calculator needed!

---

## What is a Formula?

A **formula** is a math instruction you give to Excel. It always starts with an **equals sign (=)**.

When you type `=2+2` in a cell and press **Enter**, Excel shows **4**. Magic! 🪄

---

## Step 1 — Basic Math Operators

Excel can do all kinds of math:

| Symbol | Operation | Example | Result |
|--------|-----------|---------|--------|
| `+` | Addition | `=5+3` | 8 |
| `-` | Subtraction | `=10-4` | 6 |
| `*` | Multiplication | `=6*7` | 42 |
| `/` | Division | `=20/4` | 5 |
| `^` | Power (exponent) | `=2^3` | 8 |

### 🎯 Try It!
1. Click on an empty cell (like **D1**).
2. Type `=5+3` and press **Enter**. You should see **8**.
3. Try `=100/4` in **D2**. What do you get? (**25**)
4. Try `=3^2` in **D3**. What's 3 squared? (**9**)

---

## Step 2 — Using Cell References

Instead of typing numbers directly, you can **reference cells**. This is super powerful!

**Example:** If **A1** contains 10 and **B1** contains 5:
- `=A1+B1` shows **15**
- `=A1*B1` shows **50**

When the numbers in A1 or B1 change, the formula **automatically updates**! 🔄

### 🎯 Try It!
1. Type **10** in cell **A1** and **5** in cell **B1**.
2. In cell **C1**, type `=A1+B1` and press Enter. It shows **15**.
3. Now change **A1** to **20**. Watch **C1** update to **25** automatically!

---

## Step 3 — The SUM Function

Adding up a long list of numbers one by one is boring. Use **SUM** instead!

**Syntax:** `=SUM(first cell:last cell)`

**Example:** `=SUM(B2:B6)` adds all numbers from B2 to B6.

### 🎯 Try It!

Set up this table of game scores:

| | A | B |
|-|---|---|
| **1** | Player | Score |
| **2** | Alex | 150 |
| **3** | Blake | 230 |
| **4** | Casey | 175 |
| **5** | Dana | 310 |
| **6** | Evan | 190 |
| **7** | **TOTAL** | |

1. Click on **B7**.
2. Type `=SUM(B2:B6)` and press **Enter**.
3. The total of all scores appears! (Should be **1055**)

---

## Step 4 — The AVERAGE Function

**AVERAGE** calculates the mean (the typical middle value) of a range.

**Syntax:** `=AVERAGE(first cell:last cell)`

### 🎯 Try It!
1. Click on an empty cell below your total (like **B8**).
2. Type **Average:** in **A8**.
3. In **B8**, type `=AVERAGE(B2:B6)` and press **Enter**.
4. The average score appears! (Should be **211**)

---

## Step 5 — MAX and MIN Functions

- **MAX** — finds the **biggest** number in a range
- **MIN** — finds the **smallest** number in a range

**Syntax:**
```
=MAX(B2:B6)
=MIN(B2:B6)
```

### 🎯 Try It!
1. In **A9**, type **Highest Score:** and in **B9** type `=MAX(B2:B6)`.
2. In **A10**, type **Lowest Score:** and in **B10** type `=MIN(B2:B6)`.
3. You can now see who scored the highest and lowest!

Your table should now look like this:

| | A | B |
|-|---|---|
| **1** | Player | Score |
| **2** | Alex | 150 |
| **3** | Blake | 230 |
| **4** | Casey | 175 |
| **5** | Dana | 310 |
| **6** | Evan | 190 |
| **7** | TOTAL | 1055 |
| **8** | Average | 211 |
| **9** | Highest Score | 310 |
| **10** | Lowest Score | 150 |

---

## Step 6 — COUNT Function

**COUNT** counts how many cells have **numbers** in them.

**Syntax:** `=COUNT(B2:B6)`

### 🎯 Try It!
1. In **A11**, type **Number of Players:**
2. In **B11**, type `=COUNT(B2:B6)` — it should show **5**.

---

## Step 7 — AutoSum Button ⚡

Excel has a shortcut called **AutoSum** that writes the SUM formula for you!

1. Click the cell where you want the total (right below or to the right of numbers).
2. In the **Home** tab, click the **AutoSum** button (Σ symbol).
3. Excel guesses the range — press **Enter** to confirm!

---

## Step 8 — Copying Formulas

You can copy a formula to multiple cells quickly!

1. Type a formula in one cell (like `=B2*2` in **C2**).
2. Click the cell with the formula.
3. Move your mouse to the **bottom-right corner** of the cell until you see a small **+** (called the fill handle).
4. **Click and drag** down to fill the formula into other cells.

Excel automatically adjusts the cell references — **C2** becomes `=B2*2`, **C3** becomes `=B3*2`, etc.

---

## Step 9 — Practice with Candy Data! 🍬

1. Open [`../data/candy_data.csv`](../data/candy_data.csv) in Excel.
2. Look at the **Sugar (grams)** column.
3. Below the data, calculate:
   - **Total sugar** in all candies (use SUM)
   - **Average sugar** per candy (use AVERAGE)
   - **Highest sugar** candy (use MAX)
   - **Lowest sugar** candy (use MIN)

---

## ✅ Lesson 3 Recap

You learned:
- ✔️ Formulas always start with `=`
- ✔️ Basic math: +, -, *, /, ^
- ✔️ Cell references update automatically
- ✔️ `=SUM()` — adds a range of numbers
- ✔️ `=AVERAGE()` — finds the mean
- ✔️ `=MAX()` and `=MIN()` — find the biggest and smallest
- ✔️ `=COUNT()` — counts number cells
- ✔️ How to copy formulas with the fill handle

---

## 🎮 Activity: Sports Stats Tracker

1. Open [`../data/sports_scores.csv`](../data/sports_scores.csv) in Excel.
2. Add these calculations at the bottom of the **Goals Scored** column:
   - Total goals scored (SUM)
   - Average goals per game (AVERAGE)
   - Most goals in one game (MAX)
   - Fewest goals in one game (MIN)
3. Make these label cells **bold** and the number cells formatted as **Number**.

---

➡️ **Next Lesson:** [Lesson 4 — Charts & Graphs](lesson4-charts-graphs.md)  
⬅️ **Previous Lesson:** [Lesson 2 — Entering Data](lesson2-entering-data.md)
