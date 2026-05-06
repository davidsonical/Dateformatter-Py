# 📅 DateFormatter-Py
A lightweight Python utility designed to transform standard DD-MM-YYYY date strings into a more human-readable format. Instead of looking at 01-01-1990, your users can see 1st-Jan-1990.
## 🚀 Overview
DateFormatter-Py handles the tedious logic of stripping leading zeros, mapping month integers to their respective short-hand names, and—most importantly—applying the correct English ordinal suffixes (st, nd, rd, th) to the calendar days.
## ✨ Features
 * **Ordinal Logic:** Corrects "1" to "1st", "22" to "22nd", and handles the tricky "11th/12th/13th" exceptions.
 * **Zero Stripping:** Automatically cleans up 01 to 1 for a cleaner look.
 * **Month Mapping:** Converts numeric months (1-12) to standard three-letter abbreviations (Jan, Feb, etc.).
 * **Simple Integration:** A single function with no external dependencies.
## 🛠️ How It Works
The function processes the input string through three main stages:
 1. **Parsing:** Splits the string by the - delimiter.
 2. **Cleaning:** Strips leading zeros from the day and month segments.
 3. **Formatting:** * Checks the end of the day string to append the appropriate suffix.
   * Uses a list index to fetch the month abbreviation.
   * Recombines the parts into a f-string.
## 💻 Usage
Simply pass a string in the format DD-MM-YYYY to the changeDate function:
```python
from date_formatter import changeDate

# Example 1: Standard date
changeDate("01-05-2023") 
# Output: 1st-May-2023

# Example 2: Handling the 'teens'
changeDate("12-12-2022") 
# Output: 12th-Dec-2022

# Example 3: End of the month
changeDate("31-10-1995") 
# Output: 31st-Oct-1995

```
## 📝 Requirements
 * **Python 3.6+** (Uses f-strings for output formatting).
