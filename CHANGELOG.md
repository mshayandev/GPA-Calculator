# Changelog

All notable changes to this project are documented in this file.

## [Unreleased]

### Added
- Transcript PDF upload section in the hero panel
- PDF parsing with pdf.js and transcript auto-fill workflow
- Add One More Course action for each semester table
- Potential GPA per course for max-CGPA projection
- Per-course CGPA Lift badges after calculation
- Top Boost highlight for the highest-impact course
- README and CHANGELOG project documentation

### Changed
- Upgraded UI to a modern responsive design with custom typography, gradients, and card layout
- Reworked course-entry tables and result presentation
- Switched course input model to Credit Hours + Grade Points
- Course GPA is now auto-derived from Grade Points / Credit Hours
- Result table now includes current and max weighted values per semester
- CGPA summary now displays Current CGPA, Maximum Obtainable CGPA, and Possible Improvement

### Fixed
- Corrected semester/course row calculation logic for reliable weighted totals
- Corrected final CGPA aggregation logic
- Improved handling of empty rows and invalid input combinations
