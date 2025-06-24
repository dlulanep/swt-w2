# 🧪 Functional Testing Report

## 👤 Student Information
- **Full Name**: Pathiswa Dlulane  
- **Cohort**: February 2025  
- **Date**: 24-06-2025  

---

## 🧪 What I Tested

What I Tested

| Test Type            | Description                                                                 |
|----------------------|-----------------------------------------------------------------------------|
| **Unit Test**        | Tested the `saveNote()` function for correct behavior and input validation.  |
| **Integration Test** | Verified that saving a note updates the UI and the notes array as expected. |
| **System Test**      | Simulated the full note lifecycle: create, edit, and delete; ensuring all UI and data updates worked |
---

## 🐛 Bugs / Issues Identified

| Type             | Description                                                                                      |
|------------------|--------------------------------------------------------------------------------------------------|
| Unit             | Notes can be saved even when the title or content is empty.                                      |
| Integration      | After clicking "Save Note", the note does not always appear in the list until the page reloads.  |
| System           | Editing a note deletes it without repopulating the input fields, causing accidental data loss.   |
| UI / UX          | No feedback or confirmation is shown after saving or deleting a note, leaving users uncertain.   |
| Accessibility    | Input fields lack labels, making the app difficult to use with screen

** GitHub Issues Filed: 
Save_Note - https://github.com/dlulanep/swt-w2.git
Save_Note_2 - https://github.com/dlulanep/swt-w2.git
Save_Note_3 - https://github.com/dlulanep/swt-w2.git

---

## 💬 Reflection

### 1. What did you learn from testing this app?
>   The importance of thorough input validation, user feedback, safe        
    editing logic, and accessibility. It also showed that both functional and exploratory testing are needed to deliver a user friendly application.

### 2. Which part of the app had the most bugs or problems?
> Note input and editing logic specifically:
    - Input Validation
    - Editing Function
    - UI Feedback
These issues affected both the reliability and usability of the app

### 3. What testing strategy worked best for you?
> Risk-based testing and exploratory testing. 

### 4. What was challenging during this lab?
> Setting up Jest for DOM-based tests was tricky at first.

---

## ✅ Checklist

- ✅ I wrote and ran unit, integration, and system tests using Jest  
- ✅ I filed 3 functional GitHub Issues with clear descriptions  
- ✅ I completed this Test Report and reflected on the process  
