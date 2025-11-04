# Student Catalog Management System (JavaFX)

This is a desktop application for managing a student academic catalog, built as a personal project. It allows for full CRUD (Create, Read, Update, Delete) operations for students, courses, and grades.

## Features

* Student Management
* Course Management
* Gradebook and Reporting
* Data persistence using CSV files

## Technologies Used

* **Core:** Java 17
* **UI:** JavaFX
* **Architecture:** MVC (Model-View-Controller) with a Service and Repository layer.

## Challenge & Solution

During development, I encountered a `NullPointerException` related to the JavaFX controller lifecycle. The `initialize()` method was trying to access the `CatalogService` before it was injected.

I solved this by re-architecting the controller's loading sequence, creating a separate `setService()` method to act as a manual dependency injector. This ensured the service was fully instantiated before the UI components attempted to load data.
