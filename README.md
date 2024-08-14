# ITEM Donation Management System

## Overview

The ITEM BANK application is a desktop-based application built using Python's `tkinter` library and MySQL for managing item donations. The application allows users to:

- Enter donor details.
- Enter item details for donation.
- Make requests for items and view matching items from the database.

## Components

### 1. Database

The application uses a MySQL database to store donor and item information. The database schema includes:

- **Table `donorss`**:
  - `donorid` (VARCHAR)
  - `name` (VARCHAR)
  - `age` (VARCHAR)
  - `gender` (VARCHAR)
  - `address` (VARCHAR)
  - `contactno` (VARCHAR)

- **Table `itemss`**:
  - `donorid` (VARCHAR)
  - `itemname` (VARCHAR)
  - `rating` (VARCHAR)
  - `details` (VARCHAR)

### 2. Application Interface

The application is built using `tkinter` to provide a graphical user interface. The main window includes options to:

- **Enter Donor Details**: Opens a form to input donor information.
- **Enter Item Details**: Opens a form to input details about items to be donated.
- **Request Items**: Allows users to request items and view matching items from the database.
- **Exit**: Closes the application.

### 3. Functions

**Main Window** (`root`):
- **Buttons**:
  - **Donor Details**: Opens a new window for entering donor information.
  - **Item Details**: Opens a new window for entering item details.
  - **Request Item**: Opens a new window for making item requests.
  - **Exit**: Closes the application.

**Functions**:
- **`insertDonor(donorid, name, age, gender, address, contactno)`**:
  Inserts a new donor into the `donorss` table.

- **`insertitem(donorid, itemname, rating, details)`**:
  Inserts a new item into the `itemss` table.

- **`retrieve(itd)`**:
  Retrieves matching items from the `itemss` table based on the item name and joins with `donorss` table.

- **`donordetails()`**:
  Opens a window for entering donor details.

- **`itemdetails()`**:
  Opens a window for entering item details.

- **`grid1(itd)`**:
  Displays a window listing matching items based on a request.

- **`requestitem()`**:
  Opens a window to request items and view the results.

- **`stop(root)`**:
  Closes the current `tkinter` window.

## Setup Instructions

### 1. Install Dependencies

Ensure you have Python installed and set up the MySQL connector library. You can install the MySQL connector library using:

```bash
pip install mysql-connector-python
