# 💰 Expense Tracker App (React Native + Firebase)

A  mobile **Expense Tracker** application built with **React Native** and **Expo**. This app provides full **CRUD** (Create, Read, Update, Delete) functionality for expenses, securely persisting all data using a **Firebase Realtime Database**.

The user interface uses a **Bottom Tab Navigator** for quick access to expense lists and a **Modal Stack** for managing individual expenses.

---

## 🚀 Key Features

| Feature | Description | Firebase Integration |
| :--- | :--- | :--- |
| **➕ Add Expenses** | Quickly add new expense entries via a dedicated modal screen. | **POST** new expense data to Firebase. |
| **🗓️ All Expenses** | View a comprehensive list of every expense added to the tracker. | **GET** all expense records from Firebase. |
| **⏱️ Recent Expenses** | Filtered view showing only expenses from the **last 7 days**. | **GET** all data, then filter locally or use a database query/rule. |
| **✍️ Manage Expenses** | Dedicated screen for **Editing** and **Deleting** existing expense entries. | **PUT/PATCH** (Update) and **DELETE** methods. |
| **Global State** | Uses **Context API** for managing the local expense state, synchronized with Firebase. | Context updates immediately after successful Firebase operation. |

---

## 🧭 Navigation Flow & Structure

The app's navigation provides two clear paths for expense viewing and management, primarily built with **React Navigation's** Stack and Bottom Tabs:

### 1. Root Navigation (Stack Navigator)

The main stack handles the two top-level screens:

| Screen Name | Component | Presentation | Purpose |
| :--- | :--- | :--- | :--- |
| **`ExpensesOverview`** | (Bottom Tabs) | Hidden Header | The main interface for viewing expenses. |
| **`ManageExpense`** | `ManageExpense` | Modal | Used for adding a new expense or editing an existing one. |

### 2. Bottom Tab Navigator (`ExpensesOverview`)

This component structures the expense viewing screens and includes the primary **Add Expense** button in the header.

| Tab Name | Title | Icon | Purpose |
| :--- | :--- | :--- | :--- |
| **`RecentExpenses`** | Recent Expenses | `hourglass` (Ionicons) | Shows only expenses from the past week. |
| **`All Expenses`** | All Expenses | `calendar` (Ionicons) | Shows the complete list of all transactions. |

### Screenshots

<img width="590" height="1278" alt="IMG_2107" src="https://github.com/user-attachments/assets/7c871e8d-8ad7-4164-bdcb-7aaa9f92a0b0" style="width:200px;"/>
<img width="590" height="1278" alt="IMG_2108" src="https://github.com/user-attachments/assets/aafd0dd4-43b0-4224-bccb-1bfb988a7032" style="width:200px;"/>

<img width="590" height="1278" alt="IMG_2109" src="https://github.com/user-attachments/assets/19754c34-9367-43f4-af5c-66767fe49a41" style="width:200px;"/>
<img width="590" height="1278" alt="IMG_2110" src="https://github.com/user-attachments/assets/dc84d016-0e83-4e45-899d-724ac96a4af3" style="width:200px;"/>
