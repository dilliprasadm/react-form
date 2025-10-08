# React Form with Validation, File Uploads, and Previews
The Form is live in Github Pages : https://dilliprasadm.github.io/react-form/

## Overview

This project is a **React-based form** built using **React 18** and **Babel standalone**. It demonstrates:

- Controlled form components
- Custom form validation
- File upload with **image and resume preview**
- Radio buttons, checkboxes, and dropdowns
- Reset functionality

The form **prevents the browser’s default validation messages** and displays **custom error messages** using React state.

---

## Features

1. **Form Fields**
   - Name, Email, Age, Phone
   - Gender (radio buttons)
   - Range (dropdown select)
   - Image upload
   - Resume upload (PDF/Docs)
   - Privacy policy agreement (checkbox)

2. **Validation**
   - Required fields
   - Email format check
   - Phone number must be numeric
   - Image and file required
   - Checkbox must be checked

3. **File Previews**
   - Selected image is previewed immediately
   - Resume file is previewed in an `<embed>` (PDF/Docs)

4. **Reset Button**
   - Clears all input fields
   - Clears image and file previews
   - Clears error messages

5. **Controlled Components**
   - All inputs are tied to React state
   - Radio buttons and checkboxes are fully controlled
   - Form data is displayed in JSON format after submission
  
## Technical Details

- **React Hooks Used**: 
  - `useState` – For form data, errors, and submitted status
  - `useEffect` – For generating image/file previews using `URL.createObjectURL`
  
- **Validation Logic**:
  - Implemented in the `handleSubmit` function
  - Errors are stored in an `error` state object and displayed conditionally

- **File Previews**:
  - `imagePreview` and `filePreview` use `URL.createObjectURL`  
  - Memory is cleaned up with `URL.revokeObjectURL` inside `useEffect`

- **Controlled Inputs**:
  - `value` and `checked` attributes are tied to React state
  - Ensures proper reset and validation
