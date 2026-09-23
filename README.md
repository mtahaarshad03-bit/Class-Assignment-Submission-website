# 🎓 Student Assignment Submission Portal

An automated, modern, and high-performance **Student Assignment Submission System**. Built with a sleek Glassmorphic UI and integrated seamlessly with an **n8n Automation Engine** to manage file uploads directly to Google Drive and log record entries into Google Sheets.

---

## ✨ Features

- **🎨 Modern Glassmorphism UI:** Built with pure HTML5, CSS3, and JavaScript featuring smooth animations and custom inputs.
- **📋 Pre-configured Roll Numbers:** Embedded dropdown selection for student roll numbers (`SU72-BSAIM-F24-***` and `SU72-BSAIM-S25-***`).
- **📁 File Type Validation:** Client-side validation enforcing archive uploads (`.zip`, `.rar`, `.7z` only).
- **🔒 Webhook Automated Pipeline:** Direct integration with an **n8n Workflow** to handle file storage and spreadsheet logging automatically.
- **⚡ Dynamic Feedback:** Clear, real-time visual feedback for loading, success, and error states.

---

## 🛠️ Tech Stack

- **Frontend:** HTML5, CSS3 (CSS Variables, Flexbox, Glassmorphism design), Vanilla JavaScript (Fetch API)
- **Automation Pipeline:** n8n Workflow Automation
- **Storage & Logging:** Google Drive API & Google Sheets API

---

## 🚀 How It Works

1. **Input Submission:** The student enters their details (Name, Roll Number, Email) and attaches their assignment archive.
2. **Client Validation:** JavaScript validates the file extension (`.zip`, `.rar`, `.7z`) before processing the request.
3. **Webhook Trigger:** Upon submission, data is sent as a `FormData` payload via HTTP POST to the **n8n Webhook Endpoint**.
4. **Automated Processing:**
   - **Folder Management:** n8n checks or creates a dedicated student folder on Google Drive.
   - **Drive Upload:** Uploads the assignment file directly to the assigned folder.
   - **Sheets Integration:** Appends the record (Student Name, Roll No, Assignment No, File Link) into Google Sheets.
   - **Email Confirmation:** Generates automated response notifications.

---

## 📁 Project Structure

```text
├── index.html        # Main submission portal frontend
└── README.md         # Project documentation
