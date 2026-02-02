# Senior Project: React Application with GitHub Copilot

## 📋 Project Information

**Student Name:** Nathan Wang 
**GitHub Username:** nathanwang26
**Repository URL:** https://github.com/wang-nathan/sierracanyon-attendance
**Deployed URL:** [To be added after deployment]

---

## 🎯 Project Overview

### Project Title
Sierra Canyon Attendance

### Project Description
This web-based attendance application streamlines the logistics of handling faculty attendance at an educational institution. It modernizes faculty absence management and the coordination of substitutes at Sierra Canyon. React is used as the frontend for the application, and a Google Sheets backend database is utilized. The application addresses disorganized communication by replacing constant manual back-and-forth via email and inconsistent spreadsheet formatting. It is an automated system that tracks covered and assigned periods, as well as substitute assignments. Target users are school administrators, HR, and faculty members; they need a secure and effective way to manage and record daily schedule changes.

This application is unique because it heavily emphasizes automation and security. I will utilize Microsoft Azure Identity and Access Management (IAM) for authentication. The system processes absence requests and also automates the assignment of eligible faculty to cover unassigned periods. It sends absence and claim notices via email.

For administrators, the platform makes this challenging and decentralized task into a manageable process. It provides oversight tools for HR and financial purposes. It allows administrators and department chairs to "force-assign" substitutes when necessary and send mass emails to request coverage to all faculty if needed. This approach reduces chaos in the search for a substitute and provides valuable information for institutional records.

### Motivation
I chose this project because I noticed the need for many Sierra Canyon faculty to have a system that they can rely on to request, claim, assign, and email faculty efficiently without having to worry about handling the backend of an application. Many staff have come up to me and agreed that this application will help organize their workflow. This application is a solution to the constant struggle for department chairs and HR to see an automated and up-to-date report of substitutes without having to add them to a database manually. I am planning to major in Computer Science and Artificial Intelligence, and I am interested in how CS and AI can impact businesses and society in the modern world. I want to develop an application and learn about frontend-backend communication in an application. I wish to develop an application and utilize technology to impact the future.

---

## 🛠️ Technical Specifications

### Core Features
- [ ] **Feature 1:** Report an Absence: This screen displays an option to report an absence at least 48 hours in advance prior to the date of the coverage. Include dropdowns for the Reason for Absence (Sick/Personal Day), Date (mm/dd/yyyy), and Class Periods that are being covered. For each class period, allow an option to upload associated files, linking to Google Drive storage, and descriptions for each class period. If the class period is lunch duty, require "Truck" or "Cafeteria" to be inputted into the field, and remove any file upload option. After the user presses "Submit Report," an email to available faculty will be sent.
- [ ] **Feature 2:** Claim a Period: This screen will display periods that administrators approve to be shown to any faculty viewing the application. It allows faculty to claim a period that requires coverage, only if the administrator or department chair clicks a release to all faculty button in the administrator panel.
- [ ] **Feature 3:** Periods Claimed By Me: This screen displays the information, files, and description associated with each claimed period for the faculty member who is signed in. It will allow the faculty to cancel a claimed period, only if the cancellation occurs 48 hours prior to the date of the coverage.
- [ ] **Feature 4:** Settings: This screen displays the option to input a country code and phone number, validating the phone number associated with the country code that is specified by the user. Create two toggle switches to enable/disable push notifications via phone or email for general faculty absence reports by other faculty (this toggle will be overridden if any administrator forces an email to be sent out).
- [ ] **Feature 5:** Administrator Panel: This panel sorts faculty absence reports by the department, based on the department of the currently logged-in department chair or administrator. Only administrators are allowed to this admin page. It displays a list of all of the reports in the future and has a "Manage Report" button for each report.
- [ ] **Feature 6:** Absence Report Description (Administrator End): This screen displays the description of the absence reports. It includes faculty that are available for this specified absence report, and it is sortable by department (it is set to the department of the faculty member who requested this absence by default). There are four buttons: "Force Assign Selected Faculty" (forcefully assign a faculty to this absence report, not giving the faculty selected a choice), "Email Request to Selected Faculty" (send an email to request a faculty member to cover this period), "Send Email to School for All Unassigned Periods" (this releases all of the periods associated with the absence report for this faculty member to the "Claim a Period" screen), and "Disable Release to All Faculty" (removes the associated periods for this faculty member from the "Claim a Period" screen).

### Technology Stack

| Category | Technology/Library |
|----------|-------------------|
| **Frontend Framework** | React 18.2 |
| **UI Library** | Custom CSS (no UI framework); styling in an App.css file |
| **State Management** | React local state/hooks (useState and useEffect) |
| **APIs/Backend** | Google Apps Script + Google Sheets/Google Drive (env vars) |
| **Routing** | React Router (BrowserRouter / Routes) |
| **HTTP Client** | Fetch API; Axios |
| **Additional Libraries** | XLSX helper; Jest + Testing Library tests; webpack/dotenv |

### User Interface Design

**Main Views:**
1. Faculty Member - Allow faculty members to claim, cancel, create, or get information about faculty absence reports. They are able to easily access reports that they have claimed and report an absence, so that other faculty members can cover for their class period. They have access to the Report an Absence, Claim a Period, Periods Claimed by Me, and Settings panels described above.
2. Administrator/Department Chair - Administrators and department chairs have the ability to access the panels available to Faculty Members, as well as an additional Administrator Panel screen to manage all faculty reports, sorted by department, releasing requested periods to all faculty, force-assigning faculty, emailing faculty, and disabling requested periods from all faculty.
3. HR and Financial Personnel - HR and Financial Personnel have view access to the backend Google Sheets database with all of the absences that have been reported. This will simplify income reporting and automate the process of absence management and record-keeping.

### Data Management
The application stores attendance/absence reports (faculty name/email, date, reason, periods, and the claim state) and uploaded lesson-plan files and descriptions to Google services. Rows are written to Google Sheets via Google Apps Script endpoints. Files are uploaded to Google Drive using an Apps Script upload endpoint. Email notifications are sent through Apps Script mail endpoints. The faculty roster and configuration are fetched at runtime from a published XLSX (on Google Sheets) and parsed on the client-side. The frontend only handles the UI state in React and does not use localStorage or an on-device database. Environment endpoints GOOGLE_SCRIPT_URL, GOOGLE_UPLOAD_URL, and XLSX_LINK are connected to the client.

---

## 🤖 GitHub Copilot Integration

### Planned Use Cases
- [ ] Component scaffolding and boilerplate code
- [ ] API integration and data fetching logic
- [ ] Writing unit tests
- [ ] [Other use case]

---

## 📅 Project Timeline & Milestones [__I am told that I have finished the final project due to special circumstances.__]

### Milestone 1: Project Setup ✅
**Target Date:** [Completed Project in September 2025]

**Deliverables:**
- [X] Initialize React project
- [X] Set up GitHub repository
- [X] Configure GitHub Copilot
- [X] Create basic project structure

---

### Milestone 2: Core Features 🚧
**Target Date:** [Completed Project in September 2025]

**Deliverables:**
- [X] Welcome, Credits Screen, Login, Settings, and Other Minor Screens
- [X] Faculty Member Screen - Claim, Cancel, Create, Information about Faculty Absence Reports
- [X] Administrator/Department Chair Screen - Management of Faculty Absence Reports and Emails
- [X] HR and Financial Personnel - Backend and Database Development

---

### Milestone 3: UI/UX Polish 📋
**Target Date:** [Completed Project in September 2025]

**Deliverables:**
- [X] Improve glassmorphism inside user interface
- [X] Style application to be Sierra Canyon themed dark blue/navy with animations
- [X] Added loading prompts to display screens, allowing user to know the reason for a potential slow load time
- [X] Applied high-contrast text shadows (App.css) ad descriptive alt attributes for images.

---

### Milestone 4: Testing & Deployment 🚀
**Target Date:** [Completed Project in September 2025]

**Deliverables:**
- [X] Wrote Jest and React Testing Library integration tests for claiming and canceling workflows.
- [X] Implemented Promise.all for concurrent fetching and corrected API action naming mismatches (ClaimPeriod.js).
- [X] Configured process.env variables to manage environment-specific backend endpoints.
- [X] Prepare final presentation - Presented in front of Mr. DeVaughn-Brown, Mr. Staude, and Mr. Evjen.

---

## ✅ Success Criteria

- [X] All core features are functional
- [ ] Application is deployed and accessible online
- [X] Code is well-documented with clear comments
- [X] README.md is detailed and thorough
- [X] Application directory nicely organized

---

## 📁 Project Structure

```
project-root/
├── .babelrc
├── .env
├── jest.config.js
├── package.json
├── README.md
├── webpack.config.js
├── public/
│   └── index.html
├── resources/
│   └── ...
├── src/
│   ├── AccessInfo.js
│   ├── AdminPanel.js
│   ├── App.css
│   ├── App.js
│   ├── ClaimedByMe.js
│   ├── ClaimedByMe.test.js
│   ├── ClaimLink.js
│   ├── ClaimPeriod.js
│   ├── ClaimPeriod.test.js
│   ├── index.css
│   ├── index.js
│   ├── MainMenu.js
│   ├── Modal.js
│   ├── NextWindow.js
│   ├── NextWindow.test.js
│   ├── ParticleCanvas.js
│   ├── ReportAbsence.js
│   ├── ReportAbsence.test.js
│   ├── Settings.js
│   └── utils/
│       ├── buttonArrows.js
│       ├── buttonLights.js
│       ├── date.js
│       ├── faculty.js
│       ├── fetch.js
│       ├── period.js
│       ├── settings.js
│       ├── xlsx.js
│       └── ...
└── tools/
    └── insert-jsdoc.js
```

---

## 🧪 Testing

Unit + integration tests use Jest with React Testing Library. Tests mock network calls and the XLSX helper functions; configuration is in jest.config.js, and test scripts are in package.json.

```bash
# Run tests
npm test

# Run tests with coverage
npm test -- --coverage

# Run tests in watch mode
npm test -- --watchAll
```

---

## 🌐 Deployment

[Describe your deployment process and platform]

**Deployment Platform:** [Vercel/Netlify/GitHub Pages/etc.]

**Live URL:** [To be added]

---

## 📸 Video Demo

Full-Length Video: https://youtu.be/IwVt9URoGRQ
Rapid Demo Video: https://youtu.be/df1khpN26p0

---

## 🎓 Reflections & Learnings

### What I Learned
I learned how to integrate an npm application with Google Apps Script and Sheets APIs. I included a robust XLSX parsing system and added row handling inside of fetchAndParseXLSX. I normalized and handled class periods and time logic using parsePeriods and UTC date checks in date.js. I polished UI and UX with button effects. I also added app routing and auth flow in App.js.

### Challenges Faced
Parsing XLSX reliably with sheet indexing was difficult and required my own research into connecting Google Sheets with an app. I fixed this using iterative parsing in fetchAndParseXLSX. I handled timezone and date edge cases, which required thoughtful consideration for advance/cancellation windows using UTC-normalized checks. I created file uploads and connected them to form submission using an Apps Script endpoint, and I ensured CORS and format correctness in ReportAbsence.js. The CORS header took me a while to fix, but I did more research on Google and found a solution.

### GitHub Copilot Experience
GitHub Copilot accelerated documentation and assisted in bug-fixing with CORS headers and parsing XLSX. It also helped me build my ideal UI from a long prompt I provided with a detailed description of each screen. I included follow-up discussions after each long prompt to improve each part and screen specifically. I verified that the generated suggestions match real endpoints and were not made up. I saved time on developing the boilerplate for the app, but it still required my manual (human) review for accuracy.

### Future Improvements
I would add more unit and integration tests for XLSX parsing and claiming periods. I will extract common network and email logic into a service and add retry buttons and error notices (or potential reasons why things error) for the user. I can integrate the application with Microsoft Calendar directly in the future. I will also create a virtual phone number to send SMS notifications to users. I can also add different theming options for the users to customize the application.

---

## 📚 Resources & References

- [React Documentation](https://react.dev)
- [GitHub Copilot Documentation](https://docs.github.com/copilot)
- [Webpack Docs](https://webpack.js.org)
- [Jest Docs](https://jestjs.io)
- [Google Apps Script](https://developers.google.com/apps-script)

---

# 📊 Grading Rubric

## Total Points: 100

### 1. Project Planning & Documentation (20 points)

| Criteria | Excellent (5) | Good (4) | Fair (3) | Poor (1-2) |
|----------|--------------|----------|----------|-----------|
| **Project Proposal** | Complete, clear, well-thought-out proposal | Mostly complete with minor gaps | Basic proposal with significant gaps | Incomplete or unclear |
| **README.md** | Professional, comprehensive, includes all sections | Good documentation with minor omissions | Basic documentation | Minimal or missing |
| **Code Comments** | Clear, helpful comments throughout | Good comments on complex sections | Some comments present | Few or no comments |
| **Milestone Tracking** | All milestones met on time | Most milestones met with minor delays | Several milestones delayed | Poor milestone adherence |

---

### 2. Technical Implementation (35 points)

| Criteria | Excellent (9-10) | Good (7-8) | Fair (5-6) | Poor (1-4) |
|----------|-----------------|-----------|-----------|-----------|
| **React Components** | Well-structured, reusable, follows best practices | Good structure with minor issues | Basic components with some poor practices | Poorly structured |
| **State Management** | Effective state management throughout | Good state management with minor inefficiencies | Basic state management | Poor state handling |
| **API Integration / Data Handling** | Robust error handling, efficient data flow | Good implementation with minor gaps | Basic implementation | Incomplete or buggy |
| **Code Quality & Organization** | Clean, organized, follows conventions | Mostly clean and organized | Some organization issues | Messy or disorganized |

---

### 3. Feature Completion & Functionality (25 points)

| Criteria | Excellent (9-10) | Good (7-8) | Fair (5-6) | Poor (1-4) |
|----------|-----------------|-----------|-----------|-----------|
| **Core Features** | All features fully implemented and working | Most features working with minor bugs | Some features incomplete or buggy | Many missing or broken features |
| **User Experience** | Intuitive, smooth, professional | Good UX with minor usability issues | Functional but not polished | Poor or confusing UX |
| **Testing & Bug Fixes** | Thorough testing, minimal bugs | Good testing, few minor bugs | Some testing, several bugs | Little testing, many bugs |

---

### 4. GitHub Copilot Usage & Learning (10 points)

| Criteria | Excellent (5) | Good (4) | Fair (3) | Poor (1-2) |
|----------|--------------|----------|----------|-----------|
| **Effective Use of Copilot** | Strategic use, understands suggestions, improves productivity | Good use with some reliance | Basic use, limited understanding | Minimal or blind acceptance |
| **Code Understanding** | Can explain all code, modifies suggestions appropriately | Understands most code | Limited understanding | Cannot explain code |

---

### 5. Presentation & Deployment (10 points)

| Criteria | Excellent (5) | Good (4) | Fair (3) | Poor (1-2) |
|----------|--------------|----------|----------|-----------|
| **Final Presentation** | Clear, engaging, demonstrates deep understanding | Good presentation with minor issues | Basic presentation | Unclear or unprepared |
| **Deployment** | Successfully deployed, fully functional online | Deployed with minor issues | Deployed but with significant issues | Not deployed or non-functional |

---

# 🎯 Detailed Milestone Guide

## Milestone 1: Project Initiation & Planning (Week 1-2)

### Deliverables
- ✅ Completed project proposal document
- ✅ GitHub repository created with initial README
- ✅ React project initialized with basic folder structure
- ✅ GitHub Copilot configured and tested
- ✅ Wireframes or mockups of main views

### Success Criteria
- Clear project scope and feature list defined
- Development environment fully set up
- Can successfully create and commit code to GitHub

---

## Milestone 2: Core Functionality Development (Week 3-5)

### Deliverables
- 🔲 Basic component structure implemented
- 🔲 At least 2-3 core features working
- 🔲 State management implemented
- 🔲 API integration or data handling in place
- 🔲 Regular commits showing progress

### Success Criteria
- Application demonstrates core concept/purpose
- Components are reusable and well-organized
- Data flows correctly through the application

---

## Milestone 3: Feature Completion & UI Polish (Week 6-8)

### Deliverables
- 🔲 All planned features implemented
- 🔲 UI styled with chosen library or CSS framework
- 🔲 Responsive design working on mobile and desktop
- 🔲 Error handling and loading states implemented
- 🔲 Code comments and documentation added

### Success Criteria
- Application looks professional and polished
- User experience is intuitive and smooth
- No major bugs in core functionality

---

## Milestone 4: Testing, Optimization & Deployment (Week 9-10)

### Deliverables
- 🔲 Comprehensive testing completed
- 🔲 All known bugs fixed
- 🔲 Performance optimized
- 🔲 Application deployed to hosting platform (Vercel, Netlify, etc.)
- 🔲 README updated with deployment URL and instructions

### Success Criteria
- Application is live and accessible via URL
- All features work correctly in production
- Documentation is complete and accurate

---

## Milestone 5: Final Presentation (Week 11)

### Deliverables
- 🔲 Presentation slides or demo prepared
- 🔲 Live demonstration of application
- 🔲 Code walkthrough highlighting key components
- 🔲 Discussion of GitHub Copilot usage and lessons learned
- 🔲 Reflection on challenges and solutions

### Presentation Requirements (10-15 minutes)
1. Project overview and motivation
2. Live demo of key features
3. Technical highlights and interesting code
4. How GitHub Copilot helped (with specific examples)
5. Challenges faced and how you overcame them
6. What you learned and future improvements


## Code Quality
- 📝 Write clean, readable code
- 📝 Follow consistent naming conventions
- 📝 Keep components small and focused
- 📝 Extract reusable logic into custom hooks
- 📝 Handle errors gracefully
- 📝 Add loading states for async operations
