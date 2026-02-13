# Student Registration System

A Java Swing application for student registration with form validation, MVC architecture, and CardLayout navigation.

## Overview

This is a student registration application built with Java Swing that allows users to register student information and view the details in a separate panel. The application implements the Model-View-Controller pattern with comprehensive input validation.

## Features

- **Student Registration Form** with the following fields:
  - First Name and Last Name (text fields)
  - Age (JSpinner)
  - Email (formatted text field)
  - Phone Number (formatted text field with mask)
  - Continent (JComboBox dropdown)
  - Hobbies (JTextArea with scroll pane)
  - Date of Birth (JDateChooser)
  - Profile Photo (image upload)

- **View Details Panel** displaying registered information in read-only format with disabled fields

- **Navigation System** using CardLayout within a SplitPane to switch between Form and View panels

- **Complete Validation** for all input fields with error messages

## Technology Stack

- Java SE 8+
- Java Swing
- JCalendar Library (for JDateChooser)
- Apache NetBeans IDE

## Project Structure
```
StudentRegistrationSystem/
├── src/
│   ├── model/
│   │   └── User.java                    # User model with all attributes
│   └── ui/
│       ├── MainJFrame.java              # Main application window
│       ├── Form.java                     # Registration form panel
│       └── ViewJPanel.java              # Read-only view panel
├── validation/               # Screenshots of validation errors
└── README.md
```

## Running the Application

1. Open the project in NetBeans or your preferred Java IDE
2. Ensure JCalendar library is added to the project classpath
3. Run `MainJFrame.java` from the ui package
4. The registration form will appear on startup

## How to Use

1. Fill in all required fields on the registration form
2. Upload a profile photo using the Upload button
3. Click Submit to validate and register
4. If there are validation errors, fix them and resubmit
5. On successful registration, a confirmation dialog appears
6. The application automatically switches to the View panel
7. Use the navigation buttons to switch between Form and View

## Validation Rules

- **First Name & Last Name**: Required, alphabetic characters only
- **Age**: Must be between 1-120
- **Date of Birth**: Required, cannot be in the future, must be after 1/1/1900, must match the entered age
- **Email**: Required, must be valid email format
- **Phone**: Required, must be complete (no underscores remaining)
- **Continent**: Must select from dropdown (not default option)
- **Hobby**: Required, cannot be empty
- **Photo**: Required, must upload an image

## MVC Architecture

**Model**: `User.java` contains all student attributes with getters, setters, constructor, and toString method

**View**: `Form.java` and `ViewJPanel.java` handle the user interface

**Controller**: `MainJFrame.java` manages navigation and coordinates between views and model

## Bonus Feature

The application includes JDateChooser for date of birth selection with validation that cross-checks the entered age against the calculated age from the date of birth.

## Screenshots

The `validation-screenshots` folder contains images demonstrating various validation scenarios and successful registration.

---

**Note**: Requires JCalendar library (jcalendar-1.4.jar) in classpath.