# 🧱 Minecraft Excel Hand-In Task

**Subject:** Digital Technology — Spreadsheets  
**Time:** Up to 1 hour  
**Level:** Beginner (Year 7 / Age 12)

---

## 🎮 The Scenario

You are a Minecraft wiki editor! Your job is to build a spreadsheet that helps players quickly understand the items in the game — how strong they are, how rare they are, and which ones are worth crafting.

You have been given a data file with **30 Minecraft items**. Your job is to organise it, analyse it, and make it look great using the Excel skills you've learned.

---

## 📂 The Data

Type (or copy) the following data into a **new Excel spreadsheet**, starting in cell **A1**.

> 💡 Alternatively, open the file [`../data/minecraft_items.csv`](../data/minecraft_items.csv) in Excel.

| Item | Type | Damage | Durability | Stack Size | Craftable | Enchantable | Rarity Score |
|------|------|--------|------------|------------|-----------|-------------|--------------|
| Diamond Sword | Weapon | 7 | 1561 | 1 | Yes | Yes | 9 |
| Iron Sword | Weapon | 6 | 250 | 1 | Yes | Yes | 6 |
| Stone Sword | Weapon | 5 | 131 | 1 | Yes | Yes | 4 |
| Wooden Sword | Weapon | 4 | 59 | 1 | Yes | Yes | 2 |
| Golden Sword | Weapon | 4 | 32 | 1 | Yes | Yes | 3 |
| Diamond Pickaxe | Tool | 5 | 1561 | 1 | Yes | Yes | 9 |
| Iron Pickaxe | Tool | 4 | 250 | 1 | Yes | Yes | 6 |
| Stone Pickaxe | Tool | 3 | 131 | 1 | Yes | Yes | 4 |
| Wooden Pickaxe | Tool | 2 | 59 | 1 | Yes | Yes | 2 |
| Diamond Axe | Tool | 9 | 1561 | 1 | Yes | Yes | 9 |
| Iron Axe | Tool | 9 | 250 | 1 | Yes | Yes | 6 |
| Bow | Ranged | 0 | 384 | 1 | Yes | Yes | 5 |
| Arrow | Ammo | 0 | 0 | 64 | Yes | No | 2 |
| Bread | Food | 5 | 0 | 64 | Yes | No | 3 |
| Golden Apple | Food | 4 | 0 | 64 | No | No | 8 |
| Cooked Beef | Food | 8 | 0 | 64 | No | No | 5 |
| Raw Beef | Food | 3 | 0 | 64 | No | No | 2 |
| Carrot | Food | 3 | 0 | 64 | No | No | 2 |
| Cookie | Food | 2 | 0 | 64 | Yes | No | 1 |
| Dirt | Block | 0 | 0 | 64 | No | No | 1 |
| Cobblestone | Block | 0 | 0 | 64 | No | No | 2 |
| Obsidian | Block | 0 | 0 | 64 | No | No | 8 |
| TNT | Block | 0 | 0 | 64 | Yes | No | 7 |
| Diamond | Material | 0 | 0 | 64 | No | No | 10 |
| Iron Ingot | Material | 0 | 0 | 64 | No | No | 5 |
| Gold Ingot | Material | 0 | 0 | 64 | No | No | 6 |
| Redstone | Material | 0 | 0 | 64 | No | No | 4 |
| Leather Armour Helmet | Armour | 0 | 55 | 1 | Yes | Yes | 3 |
| Iron Helmet | Armour | 0 | 165 | 1 | Yes | Yes | 6 |
| Diamond Helmet | Armour | 0 | 363 | 1 | Yes | Yes | 9 |

---

## ✅ Task Checklist

Work through each task below. Tick them off as you go!

---

### Task 1 — Format Your Spreadsheet 🖊️  
*(Skills from Lessons 1–3)*

- [ ] Make **Row 1** (the headers) **bold**.  
- [ ] Give Row 1 a **blue background fill colour** and change the text to **white**.  
- [ ] Make all columns **wide enough** so you can read all the text (double-click the column border to auto-fit).  
- [ ] **Centre-align** all the data in columns C to H (Damage through to Rarity Score).

> 💡 **Hint:** Select multiple columns at once by clicking the column letter at the top, then holding Shift and clicking the last column letter.

---

### Task 2 — Basic Formulas 🔢  
*(Skills from Lesson 3)*

In a **new area of your spreadsheet** (try starting at cell **J1**), answer these questions using formulas:

| Cell | Label (type this in column J) | Formula to write in column K |
|------|-------------------------------|------------------------------|
| J1 | Highest Damage | `=MAX(C2:C31)` |
| J2 | Lowest Rarity Score | `=MIN(H2:H31)` |
| J3 | Average Rarity Score | `=AVERAGE(H2:H31)` |
| J4 | Total Items | `=COUNTA(A2:A31)` |
| J5 | Highest Durability | `=MAX(D2:D31)` |

> 💡 **Hint:** COUNTA counts cells that contain any text or number — perfect for counting a list of item names!

---

### Task 3 — Sort Your Data 📋  
*(Skills from Lesson 6)*

1. Click anywhere inside your data table.  
2. Go to **Data** → **Sort**.  
3. Sort by **Rarity Score** from **Largest to Smallest**.  
4. Look at the result — which item is now at the top? (It should be Diamond with a score of 10!)

> 💡 After sorting, your row numbers won't match the table above anymore — that's completely fine!

---

### Task 4 — Use a Filter 🔍  
*(Skills from Lesson 6)*

1. Click anywhere in your data.  
2. Go to **Data** → **Filter** (this adds dropdown arrows to your headers).  
3. Click the dropdown arrow on the **Type** column.  
4. Untick **"Select All"**, then tick only **"Weapon"**.  
5. You should now see only the 5 weapons!

**Answer this question in a cell below your data:**  
*How many weapons are in the list?* (Type: `Weapons: 5`)

6. Click the dropdown arrow again and choose **"Select All"** to show all items again.

---

### Task 5 — IF Formula 🤔  
*(Skills from Lesson 7)*

In column **I**, add a new header called **"Worth Crafting?"** in cell **I1**.

In cell **I2**, write this formula:

```
=IF(H2>=7,"Must Craft!","Maybe Later")
```

- This checks if the Rarity Score is **7 or above**.  
- If it is → it shows **"Must Craft!"**  
- If not → it shows **"Maybe Later"**

**Copy this formula down** for all 30 rows (click I2, then drag the small square in the bottom-right corner of the cell down to I31).

> 💡 **Hint:** Items with a rarity of 7+ are: Diamond Sword, Obsidian, TNT, Golden Apple, Diamond, and Diamond items!

---

### Task 6 — VLOOKUP 🔎  
*(Skills from Lesson 8)*

In a new area (try cell **J8**), create a quick item lookup tool!

| Cell | What to type |
|------|-------------|
| J8 | `Item Lookup:` |
| K8 | `Diamond Sword` *(you can change this to any item name!)* |
| J9 | `Rarity Score:` |
| K9 | *(write your VLOOKUP formula here)* |

The formula for **K9** is:
```
=VLOOKUP(K8,A2:H31,8,FALSE)
```

This looks up whatever item name is in **K8** and returns its **Rarity Score** from column 8.

**Test it!** Change K8 to `Obsidian` — the rarity score should change to **8**.

---

### Task 7 — Create a Chart 📊  
*(Skills from Lesson 4)*

Let's make a bar chart showing the **Rarity Score** of just the weapons and tools.

1. Hold **Ctrl** and select:  
   - **A1:A11** (Item names for the first 11 items — Weapons and Tools)  
   - **H1:H11** (Rarity Scores for those items)  
2. Go to **Insert** → **Bar Chart** → choose the first **Clustered Bar** option.  
3. Give your chart the title: **"Rarity Scores — Weapons & Tools"**  
4. Move the chart so it sits neatly below your data.

> 💡 **Hint:** To select two non-touching columns, select the first one, then hold **Ctrl** and select the second.

---

### Task 8 — Conditional Formatting 🎨  
*(Skills from Lesson 9)*

Make your Rarity Score column instantly show which items are rare, common, or in between!

#### Part A — Highlight High Rarity Items
1. Select cells **H2:H31** (all Rarity Scores).  
2. Go to **Home** → **Conditional Formatting** → **Highlight Cells Rules** → **Greater Than…**  
3. Type **8** in the box.  
4. Choose **"Green Fill with Dark Green Text"**.  
5. Click **OK**.

#### Part B — Highlight Low Rarity Items
1. With **H2:H31** still selected.  
2. Go to **Conditional Formatting** → **Highlight Cells Rules** → **Less Than…**  
3. Type **3** in the box.  
4. Choose **"Light Red Fill with Dark Red Text"**.  
5. Click **OK**.

#### Part C — Add a Color Scale to Damage
1. Select cells **C2:C31** (all Damage values).  
2. Go to **Conditional Formatting** → **Color Scales**.  
3. Choose the **Green-Yellow-Red** scale.

#### Part D — Add Data Bars to Durability
1. Select cells **D2:D31** (all Durability values).  
2. Go to **Conditional Formatting** → **Data Bars**.  
3. Choose the **Blue** data bar.

You should now be able to see at a glance which items are rare, durable, and powerful! ⚔️

---

## 📸 Finished? Save Your Work!

1. Press **Ctrl + S** to save.  
2. Save the file as: `Minecraft_Excel_Task_[YourName].xlsx`  
3. Submit your `.xlsx` file to your teacher.

---

## ✅ Marking Checklist

Your teacher will check for the following:

| Task | What's being checked | Marks |
|------|----------------------|-------|
| Task 1 | Bold headers, blue fill, white text, column widths, centred alignment | 4 |
| Task 2 | All 5 formulas correct (MAX, MIN, AVERAGE, COUNTA, MAX) | 5 |
| Task 3 | Data sorted by Rarity Score, largest to smallest | 2 |
| Task 4 | Filter used, weapon count answered correctly | 2 |
| Task 5 | IF formula correct and copied down all 30 rows | 4 |
| Task 6 | VLOOKUP formula correct, lookup tool works | 4 |
| Task 7 | Bar chart created with correct title | 4 |
| Task 8 | All four conditional formatting rules applied | 5 |
| **Total** | | **30** |

---

## 💡 Stuck? Here Are Some Tips

| Problem | Try This |
|---------|----------|
| My formula shows `#REF!` | Check the cell range in your formula — you may have the wrong column letters |
| My VLOOKUP shows `#N/A` | Make sure you've spelled the item name exactly right in K8 (capital letters matter!) |
| My chart looks wrong | Make sure you selected both the Item column AND the Rarity Score column |
| My conditional formatting isn't showing | Check you selected the right cells before applying the rule |
| I can't see all my text in a cell | Double-click the line between two column letters to auto-fit the width |

---

🏠 **Back to Start:** [README](../README.md)
