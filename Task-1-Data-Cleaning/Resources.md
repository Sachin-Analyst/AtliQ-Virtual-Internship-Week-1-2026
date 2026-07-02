# Task 1 Data Cleaning

Attendance_data.csv | Power BI | Power Query | DAX

---

## 01. Data Cleaning

5 requests in the raw dataset, fixed one by one in Power Query.

### 1. Check for duplicates in the dataset and remove them.

**Problem**
Total Rows before removing duplicates — 6336

**Approach**
Home > Transform Data > Left click on "date column" > Shift Key + Left click on "Status Column" > Right Click > Remove Duplicates

**Result**
Total Rows After removing duplicates — 6208

---

### 2. Standardize the date values to the format YYYY-MM-DD and extract the month name and day type from them.

**Problem**
Date formatted dd-MM-yyyy

**Approach**
First duplicated "date column" > then navigated to Add column ribbon > clicked custom column > entered column name "Date-New-Format" and entered the following as custom column formula

```
=Date.ToText([date],"yyyy-MM-dd")
```

- Remaining requests: duplicated date column > then Home Ribbon > clicked Date & Time Column > Month > Name of the Month
- Remaining requests: duplicated date column > then Home Ribbon > clicked Date & Time Column > Day > Day of the week
- Navigated to Add column Ribbon > clicked conditional column > then written If condition > Value 0 equals > Weekend, Else If Value 6 equals > Weekend Else Weekday

**Result**
Date formatted into yyyy-MM-dd

---

### 3. Remove any extra characters, such as special characters, from the employee ID values. Some IDs may contain a '@' character at the end, which can be cleaned and brought to a common format.

**Problem**
Extra characters in the employee_id (e.g. Atq-458@)

**Approach**
- First clicked employee_id column > Right clicked > split column > by delimiter > custom > @
- Removed the employee_id.2 because it holds extra characters

**Result**
Removed extra characters in the employee_id (e.g. Atq-458)

---

### 4. Standardize the capitalization of names. Convert all names to title case, which means capitalizing the first letter of each word.

**Problem**
Employee names are not in proper format

**Approach**
First clicked name column > Right clicked > Transformed > clicked capitalized by each word

**Result**
Employee names are in proper format

---

### 5. Map the corresponding values in the status column with the given abbreviations:

Work From Office --> WFO | Work From Home --> WFH | Birthday Leave --> BL
Menstrual Leave --> ML | Paid Leave --> PL | Sick Leave --> SL | Weekly Off --> WO

**Problem**
The status is in long text

**Approach**
- Navigated to Add column Ribbon > Clicked conditional column > then written If condition > Value Work From Home equals > WFH, 
-Else If Value Work From Office equals > WFO Else Weekday
- Likewise written for all the status

**Result**
The status has been changed to its abbreviations

---
