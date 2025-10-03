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

<img width="361" height="809" alt="Screenshot 2025-10-03 at 16 31 18" src="https://github.com/user-attachments/assets/f3bd4c73-64e6-4c13-af93-948791864fbc" style="width:200px;"/>
<img width="370" height="811" alt="Screenshot 2025-10-03 at 16 31 26" src="https://github.com/user-attachments/assets/56e6e925-ee6b-4fde-a6b8-81199c452752" style="width:200px;"/>
<img width="357" height="808" alt="Screenshot 2025-10-03 at 16 31 34" src="https://github.com/user-attachments/assets/e3837ac2-06cd-4eec-a80a-d9fb7a2e4dee" style="width:200px;"/>
<img width="367" height="799" alt="Screenshot 2025-10-03 at 16 31 54" src="https://github.com/user-attachments/assets/00996e7b-a936-417d-910d-1e15e77d3363" style="width:200px;"/>
<img width="367" height="808" alt="Screenshot 2025-10-03 at 16 32 07" src="https://github.com/user-attachments/assets/79934eaa-206b-4a33-b9a4-d1462178ce00" style="width:200px;"/>
