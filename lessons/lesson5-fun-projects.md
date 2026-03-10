# Lesson 5: Projects

**Time:** 45–60 minutes  
**What you'll learn:** Apply everything you've learned to create awesome real-world spreadsheets!

---

## Introduction

You've learned the basics of Excel — now let's put them all together in fun, creative projects. Choose any project (or do them all!)

---

## Project 1: Ultimate Video Game Tracker

Create a spreadsheet to track your favorite video games!

### What You'll Build
A game tracker with scores, ratings, genres, and charts.

### Step-by-Step Instructions

**Step 1: Set up your headers**

Start a new Excel file. In **Row 1**, type these headers:

| A | B | C | D | E | F |
|---|---|---|---|---|---|
| Game Title | Platform | Genre | Hours Played | My Rating (1-10) | Completed? |

**Step 2: Add your data**

Fill in rows 2–11 with your 10 favorite games (real or made up!). Example:

| Game Title | Platform | Genre | Hours Played | My Rating | Completed? |
|------------|----------|-------|--------------|-----------|------------|
| Minecraft | PC | Sandbox | 200 | 10 | No |
| Mario Kart 8 | Switch | Racing | 50 | 9 | Yes |
| Fortnite | PC | Battle Royale | 120 | 8 | No |
| Zelda: BOTW | Switch | Adventure | 85 | 10 | Yes |
| Roblox | PC | Sandbox | 300 | 7 | No |

**Step 3: Add formulas (Row 13 onward)**

Below your data, add these calculations:
- **A13:** `Total Hours Played:` → **E13:** `=SUM(D2:D11)`
- **A14:** `Average Rating:` → **E14:** `=AVERAGE(E2:E11)`
- **A15:** `Highest Rated Game:` → **E15:** `=MAX(E2:E11)`
- **A16:** `Total Games:` → **E16:** `=COUNT(E2:E11)`

**Step 4: Format your spreadsheet**
1. Make **Row 1** headers **bold** with a colored background.
2. Auto-fit all columns (Ctrl+A, then double-click any column border).
3. Center all text in Row 1.

**Step 5: Create a chart**
1. Select the **Game Title** and **Hours Played** columns.
2. Create a **Bar Chart** titled **"Time Spent on Each Game"**.

---

## Project 2: Sports Season Tracker

Track your favorite sports team's season!

### What You'll Build
A season tracker with wins/losses, goals, and standings.

### Step-by-Step Instructions

**Step 1: Set up your headers**

| A | B | C | D | E | F |
|---|---|---|---|---|---|
| Game # | Opponent | Goals For | Goals Against | Result | Points |

**Step 2: Add sample data**

| Game # | Opponent | Goals For | Goals Against | Result | Points |
|--------|----------|-----------|---------------|--------|--------|
| 1 | Tigers | 3 | 1 | Win | 3 |
| 2 | Eagles | 0 | 2 | Loss | 0 |
| 3 | Sharks | 2 | 2 | Draw | 1 |
| 4 | Lions | 4 | 0 | Win | 3 |
| 5 | Wolves | 1 | 3 | Loss | 0 |
| 6 | Bears | 3 | 1 | Win | 3 |
| 7 | Hawks | 2 | 2 | Draw | 1 |
| 8 | Foxes | 5 | 1 | Win | 3 |

**Step 3: Season Summary (below the table)**

- `=SUM(C2:C9)` — Total Goals Scored
- `=SUM(D2:D9)` — Total Goals Conceded
- `=SUM(F2:F9)` — Total Points
- `=COUNTIF(E2:E9,"Win")` — Total Wins *(new function!)*
- `=COUNTIF(E2:E9,"Loss")` — Total Losses
- `=COUNTIF(E2:E9,"Draw")` — Total Draws

> **New Function Alert! COUNTIF**
> `=COUNTIF(range, "criteria")` counts cells that match a specific word or value.
> Example: `=COUNTIF(E2:E9,"Win")` counts all the "Win" results.

**Step 4: Create Charts**
1. A **pie chart** showing Wins vs. Losses vs. Draws.
2. A **column chart** showing Goals For vs. Goals Against per game.

---

## Project 3: Movie Night Planner

Create a spreadsheet to rate movies and find your favorites!

### What You'll Build
A movie database with ratings and recommendations.

### Step-by-Step Instructions

**Step 1: Set up your headers**

| A | B | C | D | E | F |
|---|---|---|---|---|---|
| Movie Title | Year | Genre | My Rating (1-10) | Friend's Rating | Watch Again? |

**Step 2: Add 10 movies** you've seen (check the [`../data/movies.csv`](../data/movies.csv) file for ideas!).

**Step 3: Calculate averages**

In a summary area, use:
- `=AVERAGE(D2:D11)` — Your average rating
- `=AVERAGE(E2:E11)` — Friend's average rating
- `=MAX(D2:D11)` — Your highest rated movie's score
- `=COUNTIF(F2:F11,"Yes")` — How many you'd watch again

**Step 4: Make it look amazing**
1. Add a **gradient fill** color to the header row.
2. Make movies you'd watch again have a **green** background.
3. Make movies you wouldn't watch again have a **red** background.

> **How to manually color specific rows:**
> 1. Click on the row with a "Yes" in the Watch Again column.
> 2. In the **Home** tab, click **Fill Color** and choose green.
> 3. Repeat for "No" rows in red.

---

## Project 4: Lollies Shop Simulator

Use the lollies data to run a pretend candy shop!

### What You'll Build
A lollies shop inventory and sales tracker.

### Step-by-Step Instructions

**Step 1: Open the candy data**
Open [`../data/candy_data.csv`](../data/candy_data.csv).

**Step 2: Add new columns**

After the existing columns, add:
| Column | Header | Formula |
|--------|--------|---------|
| Next empty | Price ($) | Enter manually (make them up!) |
| Next empty | Quantity in Stock | Enter manually |
| Next empty | Total Value | `=Price * Quantity` |

**Step 3: Calculate shop totals**
- Total inventory value: `=SUM(Total Value column)`
- Most expensive lollies: `=MAX(Price column)`
- Average price: `=AVERAGE(Price column)`

**Step 4: Create a chart**
Make a **bar chart** showing the price of each lollies.

---

## 🌟 Bonus Challenge: Design Your Dream Spreadsheet

Now create something **totally your own!** Some ideas:

- 📚 **Book tracker** — books you've read, want to read, author, rating
- 🎵 **Music tracker** — favorite songs, artists, number of times listened
- 🌤️ **Weather log** — record the temperature each day for a month
- 🎂 **Birthday planner** — friends' birthdays, gift ideas, budget
- 🏅 **Achievement tracker** — track your personal goals and progress

Use everything you've learned:
- ✅ Proper headers with bold formatting
- ✅ At least one SUM, AVERAGE, MAX, or MIN formula
- ✅ At least one chart
- ✅ Colors and formatting that make it easy to read

---

## ✅ Lesson 5 Recap

You applied:
- ✔️ Data entry and organization
- ✔️ Text and number formatting
- ✔️ SUM, AVERAGE, MAX, MIN, COUNT, COUNTIF formulas
- ✔️ Creating and customizing charts
- ✔️ Building real-world useful spreadsheets

---

## 🎓 Congratulations — You're an Excel Beginner! 🎉

You've completed all 5 lessons! Here's everything you can now do:

| Skill | ✅ |
|-------|---|
| Navigate the Excel UI | ✔️ |
| Enter and edit data | ✔️ |
| Format cells (bold, color, alignment) | ✔️ |
| Use basic formulas | ✔️ |
| Create charts and graphs | ✔️ |
| Build real spreadsheet projects | ✔️ |

### What's Next?

When you're ready to level up, explore:
- 🔍 **Sorting and Filtering** — organize data alphabetically or numerically
- 🔒 **IF Statements** — make cells show different things based on conditions
- 🔗 **VLOOKUP** — search for data across sheets
- 🎨 **Conditional Formatting** — automatically color cells based on their values

---

⬅️ **Previous Lesson:** [Lesson 4 — Charts & Graphs](lesson4-charts-graphs.md)  
🏠 **Back to Start:** [README](../README.md)
