# CGPA Calculator

A modern browser-based CGPA calculator with:
- Semester-wise course entry
- Current CGPA and maximum obtainable CGPA estimation
- Per-course improvement impact (CGPA lift)
- Optional transcript PDF auto-fill
- Manual add-more-course flow after auto-fill

## Features

- Modern responsive UI using Bootstrap + custom styles
- Dynamic semester and course table generation
- Course GPA auto-calculated from:

  GPA = Grade Points / Credit Hours

- Maximum obtainable CGPA using Potential GPA per course
- Per-course impact badge showing estimated CGPA lift
- Top boost highlighting for the highest-impact course
- PDF transcript parsing and auto-population (pdf.js)

## How It Works

### 1. Build semester forms
- Enter number of semesters
- Click Build Semester Forms
- For each semester, enter number of courses and create a table

### 2. Enter course data
For each course:
- Course Name
- Credit Hours
- Grade Points
- Potential GPA

The app auto-computes Course GPA as:

GPA = Grade Points / Credit Hours

### 3. Calculate results
Click Calculate CGPA to see:
- Semester totals and GPA
- Current CGPA
- Maximum Obtainable CGPA
- Possible CGPA improvement
- Per-course CGPA lift badges

## Formula Reference

### Course GPA
GPA_course = GradePoints / CreditHours

### Current weighted points
CurrentWeighted = sum(GradePoints)

### Max weighted points
MaxWeighted = sum(CreditHours * max(CurrentCourseGPA, PotentialGPA))

### Current CGPA
CurrentCGPA = CurrentWeighted / TotalCreditHours

### Maximum Obtainable CGPA
MaxCGPA = MaxWeighted / TotalCreditHours

### Per-course lift contribution
CourseLift = (CreditHours * (PotentialGPA - CurrentCourseGPA)) / TotalCreditHours

## PDF Auto-Fill Notes

- Upload transcript PDF and click Auto Fill From PDF
- The parser uses text heuristics and may require manual adjustments depending on transcript format
- You can always edit values and add more rows after auto-fill

## Tech Stack

- HTML
- CSS
- JavaScript (vanilla)
- Bootstrap 5
- pdf.js (CDN)

## Run Locally

No build step required.

1. Open index.html in a browser
2. Or serve the folder with any static server

## Future Enhancements

- Better transcript parsing for institution-specific layouts
- Rank Top 3 courses to improve in a dedicated summary panel
- Optional backend AI suggestions (Gemini or others)
