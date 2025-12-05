## 1. Improve README: Complete Node.js Setup & Local Run Instructions

The current README does not provide enough detail for new contributors to correctly install Node.js, verify npm installation, or run the project locally.
The following steps should be added to the README under a Setup or Getting Started section.

### A. Node.js Installation (Windows)

1. Download Node.js visit: https://nodejs.org/en/download
2. Download the Windows Installer (recommended version).
3. Install Node.js
4. During the installation process, in the Feature Selection step:
   a. Ensure that “npm package manager” is selected.
   b. Do not select only “Node.js runtime”; npm must be included
   c. Verify Installation
5. Open Git Bash or the VS Code terminal and run:
- node -v
- npm -v
- If both commands return version numbers, installation is successful.

### B. Fixing npm Scripting Error on Windows

- Sometimes npm -v shows a PowerShell execution policy error.
- To fix it:
  1. Open Windows PowerShell as Administrator.
  2. Run: "Set-ExecutionPolicy RemoteSigned -Scope CurrentUser", Press Y to confirm.
  3. Close PowerShell and return to Git Bash/VS Code terminal.

### C. Running the Project Locally
1. Fork and clone the repository:" git clone https://github.com/mutahir-muhammad/Cohort.git "
2. cd Cohort
3. Install dependencies: " npm install "
4. Resolve vulnerabilities (if prompted):
5. If npm suggests: run "npm audit fix"
6. If it again recommends: run "npm audit fix --force"
7. Start the development server: run "npm run dev"
8. Open the project in your browser. The terminal will show a localhost link.
9. Ctrl + Click the link to preview the site.

## 2. Add a Proper Usage Guide / Workflow Explanation

The README does not explain how to use the site, which can confuse first-time users.
Add a Usage or How to Use the App section describing the workflow.

### Recommended User Flow
1. Roles Tab
Add or remove the roles required for your team structure using the delete icon in bottom-right.
Example:
If you only want Lead, Co-lead, and Developer, delete roles like Architect, QA, or Designer.

2. Personnels Tab
   a. Add all personnel who will be considered for team assignment
   b. Assign each person a role from the left-side dropdown.
   c. Remove the default placeholder personnel entries first.
   d. Ensure every person has a role assigned.

3. Template Tab
Define how many of each role should appear in each team.
Example team template:
    a. Leads x1
    b. Developer x3
    c. Co-lead x1

4. Generate Tab
   a. Select the number of teams you want.
   b. Click Generate:
      "Teams are created randomly based on available personnel and template."
   c. If the system lacks enough personnel for a role:
   d. A message will appear in the display panel.
   e. If you want a fresh distribution:
   f. Use Reshuffle → then Generate again.

5. After Generation
   a. Review generated teams.
"(Suggested feature enhancement ↓) Export teams to share with others."

## 3. Suggested Feature: Export / Download Teams
1. To improve usability, the app should support downloading generated teams in a formatted document.
2. Recommended Export Options
   a. PDF — for print-friendly, shareable output.
   b. CSV — for spreadsheet editing.
   c. Optional: Styled HTML preview before download.
3. Information to include:
   a. Team number or name
   b. Members with their roles
   c. Template configuration
   d. Date/time of generation
This feature would allow users to easily share team lists via WhatsApp, email, etc.

## 4. Recommended README File Structure
1. A cleaner, more complete README could follow this format:
2. Project Title & Description
3. Screenshots or Demo (optional)
4. Prerequisites
5. Node.js Setup (with Windows steps)
6. How to Run Locally
7. Usage / Workflow Explanation
8. Export Feature (if added)
9. Troubleshooting
10. Contributing Guide
11. License (if required)

## 5. Troubleshooting Section to Add
Include the following common fixes:
1. PowerShell Execution Policy Error: "Set-ExecutionPolicy RemoteSigned -Scope CurrentUser"
2. Fix npm Vulnerabilities
   a. npm audit fix
# or if needed:
   b. npm audit fix --force
