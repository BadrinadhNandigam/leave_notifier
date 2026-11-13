# 🏖️ Leave Notifier

A lightweight, installable **Progressive Web Application (PWA)** designed to simplify employee leave management and team notifications.

Leave Notifier allows employees to apply for leave, track approval status, manage team information, receive leave-day reminders, and notify team members through WhatsApp.

Built using **HTML5, CSS3, and Vanilla JavaScript**, with browser Local Storage and Service Worker support.

**GitHub Repository:** [Leave Notifier](https://github.com/BadrinadhNandigam/leave_notifier)

**live deployment link:** https://leavenotifier-55ac.vercel.app/

---

## 📌 Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Application Screens](#application-screens)
- [Application Workflow](#application-workflow)
- [Technology Stack](#technology-stack)
- [Project Structure](#project-structure)
- [Installation and Setup](#installation-and-setup)
- [GitHub Pages Deployment](#github-pages-deployment)
- [Team Configuration](#team-configuration)
- [Data Storage and Privacy](#data-storage-and-privacy)
- [Known Limitations](#known-limitations)
- [Future Enhancements](#future-enhancements)
- [License](#license)
- [Author](#author)

---

## 📖 Overview

Leave Notifier is a simple and efficient leave management application developed to make team leave coordination easier.

The application allows users to:

- Apply for employee leave.
- Select leave types and date ranges.
- Submit leave requests with reasons.
- Track Pending, Approved, and Rejected applications.
- Notify team members through WhatsApp.
- View employees currently on leave.
- Configure leave-day alarms.
- Maintain leave application history.

The application provides a responsive interface and can be installed on supported mobile devices and desktop browsers as a Progressive Web App.

## ✨ Features

### 1. Leave Application Management

- Select an employee from the predefined team.
- Choose different leave types:
  - Casual Leave
  - Sick Leave
  - Earned Leave
  - Half Day
  - Other
- Select leave starting and ending dates.
- Enter the reason for leave.
- Validate date selections.
- Calculate the total number of leave days.
- Submit leave applications.

### 2. WhatsApp Notifications

- Generate formatted WhatsApp notification messages.
- Notify all five configured team members.
- Open WhatsApp using `wa.me` links.
- Include employee name, leave type, dates, and reason.
- Copy notification messages.
- Share notification messages.
- Resend notifications after approval or rejection.
- Send test messages to verify phone numbers.

**Note:** WhatsApp messages are not sent automatically. The application opens WhatsApp with a pre-filled message, and the user must manually send it.

### 3. Leave Approval Management

Every submitted leave application receives an initial status of **Pending**.

Available status options:

- **Pending:** Leave application submitted and awaiting a decision.
- **Approved:** Leave application approved.
- **Rejected:** Leave application rejected.

Additional operations:

- Approve leave requests.
- Reject leave requests.
- Resend status notifications.
- Delete individual leave records.

### 4. Dashboard

The dashboard provides an overview of leave activities.

It displays:

- Total leave applications.
- Pending applications.
- Approved applications.
- Rejected applications.
- Employees currently on leave.
- Recent leave applications.
- Leave-day alarm status.

### 5. Leave History and Filters

- View all leave applications.
- Filter leave records by employee.
- View leave dates and duration.
- Check application status.
- Review leave reasons.
- Approve or reject requests.
- Resend WhatsApp notifications.
- Delete leave records.

### 6. Leave-Day Alarm

- Enable or disable leave-day alarms.
- Configure preferred alarm time.
- Display reminders for employees on leave.
- Play an audible alarm.
- Vibrate supported devices.
- Enable browser notifications.
- Snooze alarms for 10 minutes.
- Dismiss alarms.
- Notify team members through WhatsApp.

The in-app alarm works while the application is running.

For reminders when the application is closed, users can create Google Calendar events using the Phone alarm option.

### 7. Google Calendar Integration

- Generate Google Calendar event links.
- Include employee names and leave dates.
- Include leave type and reason.
- Allow users to review and save calendar events.

### 8. Team Management

- Manage five predefined team members.
- Configure WhatsApp phone numbers.
- Include country codes.
- Test WhatsApp numbers.
- Clear saved phone numbers.

Example phone number format:

`919876543210`

### 9. CSV Export

- Generate leave records in CSV format.
- Copy CSV data to the clipboard.
- Export information by pasting it into Microsoft Excel or other spreadsheet applications.

### 10. Progressive Web Application (PWA)

- Installable web application.
- Responsive mobile-first interface.
- Web app manifest configuration.
- Custom application icons.
- Service Worker implementation.
- Offline caching support.
- Network-first caching strategy.
- Light and dark theme support.

---

## 🖥️ Application Screens

| Screen | Description |
|---|---|
| Home | Dashboard displaying leave statistics and recent activities |
| Apply | Submit new leave applications |
| Log | View and manage leave records |
| Team | Configure team WhatsApp numbers |
| More | Manage alarms, notifications, exports, and settings |

---

## 🔄 Application Workflow

### Leave Application Workflow

1. Open the Leave Notifier application.
2. Navigate to the Apply screen.
3. Select an employee.
4. Choose the leave type.
5. Select From and To dates.
6. Enter the leave reason.
7. Click **Submit & Notify All 5**.
8. The application saves the leave request.
9. The request receives Pending status.
10. WhatsApp notification links are generated.
11. Open WhatsApp and manually send notifications.
12. Navigate to the Log screen.
13. Approve or reject the leave application.
14. Resend the updated notification when required.

### Leave-Day Alarm Workflow

1. Navigate to the More screen.
2. Enable the leave-day alarm.
3. Configure the preferred alarm time.
4. Keep the application running.
5. The application checks employees currently on leave.
6. When the configured time is reached, a reminder appears.
7. Choose Notify Team on WhatsApp, Snooze, or Dismiss.

---

## 🛠️ Technology Stack

| Technology | Purpose |
|---|---|
| HTML5 | Application structure |
| CSS3 | Styling and responsive design |
| JavaScript | Application functionality |
| Local Storage | Store leave records and settings |
| Web App Manifest | PWA configuration |
| Service Worker | Offline caching |
| WhatsApp `wa.me` Links | WhatsApp message preparation |
| Google Calendar URL | Calendar reminders |
| Notifications API | Browser notifications |
| Web Audio API | Alarm sound |
| Vibration API | Device vibration |

**No external JavaScript framework or package manager is required.**

---

## 📂 Project Structure

```text
leave_notifier/
│
├── index.html
│   └── Main application containing HTML, CSS and JavaScript
│
├── manifest.json
│   └── Progressive Web App configuration
│
├── sw.js
│   └── Service Worker and offline caching
│
├── icon-192.png
│   └── Application icon (192 × 192)
│
├── icon-512.png
│   └── Application icon (512 × 512)
│
├── privacy.html
│   └── Browser-viewable privacy policy
│
├── PRIVACY.md
│   └── Privacy policy documentation
│
├── LICENSE
│   └── MIT License
│
└── README.md
    └── Project documentation
```

---

## 💻 Installation and Setup

### Prerequisites

- Python or Visual Studio Code.
- Modern web browser.
- Git.
- GitHub account.

### Step 1: Clone the Repository

```bash
git clone https://github.com/BadrinadhNandigam/leave_notifier.git
```

### Step 2: Navigate to the Project Folder

```bash
cd leave_notifier
```

### Step 3: Start the Local Server

Using Python:

```bash
python -m http.server 8000
```

### Step 4: Open the Application

Open the following URL in your browser:

```text
http://localhost:8000
```

Alternatively, use the Live Server extension in Visual Studio Code.

---

## 🚀 GitHub Pages Deployment

Follow these steps to deploy the application using GitHub Pages.

1. Open the GitHub repository.
2. Navigate to **Settings**.
3. Select **Pages**.
4. Under Build and Deployment, select **Deploy from a branch**.
5. Select the `main` branch.
6. Select the `/ (root)` folder.
7. Click **Save**.
8. Wait for GitHub Pages deployment to complete.

### Live Application

[https://badrinadhnandigam.github.io/leave_notifier/](https://badrinadhnandigam.github.io/leave_notifier/)

---

## 👥 Team Configuration

The application initially contains five predefined team members.

The team configuration is available in the `M` array inside `index.html`.

Example:

```javascript
var M = [
  { id: 1, n: "Prasad", i: "🚢" },
  { id: 2, n: "Manga Raju", i: "⚓" },
  { id: 3, n: "Kiran", i: "🛠️" },
  { id: 4, n: "Patrudu", i: "🧭" },
  { id: 5, n: "Sekhar", i: "🏗️" }
];
```

You can customize:

- Employee names.
- Employee icons.
- Employee background colors.
- WhatsApp phone numbers.

Keep employee IDs unique because they are used to associate team members with leave records.

---

## 🔐 Data Storage and Privacy

Leave Notifier is a client-side application.

- No user account is required.
- No backend server is used.
- Data is stored in browser Local Storage.
- Phone numbers remain on the user's device.
- Leave records remain on the user's device.
- Alarm settings are stored locally.
- No analytics or advertisements are included.
- WhatsApp notifications are initiated manually.
- Google Calendar integration is optional.

**Important:** Data is not synchronized between different devices or users. Clearing browser data may permanently remove saved records.

For additional information, refer to:

- [Privacy Policy](PRIVACY.md)
- [Privacy Policy – HTML](privacy.html)

---

## ⚠️ Known Limitations

- No centralized database.
- No user authentication.
- No multi-user synchronization.
- WhatsApp messages require manual sending.
- In-app alarms depend on the application running.
- Browser notification support varies by device.
- Five team members are predefined in the JavaScript source.
- No attendance percentage calculation is implemented.
- No automatic 75% examination eligibility validation is implemented.

---

## 🔮 Future Enhancements

Potential improvements for future versions:

- Student and administrator login.
- Attendance management system.
- Automatic attendance percentage calculation.
- 75% attendance eligibility validation.
- Database integration.
- Real-time synchronization.
- Role-based access control.
- Advanced leave approval workflow.
- Employee and department management.
- Improved background notifications.
- Downloadable attendance and leave reports.
- Holiday and weekend management.

These are proposed enhancements and are not included in the current implementation.

---

## 📜 License

This project is distributed under the **MIT License**.

Refer to the [LICENSE](LICENSE) file for complete licensing information.

---

## ⚖️ Disclaimer

Leave Notifier is an independent project and is not affiliated with or endorsed by WhatsApp or Meta.

WhatsApp is a third-party service. Users initiate and send messages themselves.

The application is provided on an "AS IS" basis under the terms of the included MIT License.

---

## 👨‍💻 Author

**Badrinadh Nandigam**

GitHub: [@BadrinadhNandigam](https://github.com/BadrinadhNandigam)

---

⭐ If you find this project useful, consider giving the repository a star!
