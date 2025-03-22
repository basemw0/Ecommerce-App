# StackShop - Java E-Commerce Application

## 📌 Project Overview
StackShop is a **Java-based e-commerce platform** built with **JavaFX**, offering an interactive user interface for three distinct user roles:

🔹 **Customers** – Browse products, manage carts, place orders, and track order history.  
🔹 **Suppliers** – Add and manage product listings efficiently.  
🔹 **Administrators** – Oversee users, suppliers, orders, and handle supplier registration requests.

The project utilizes **FXML for UI layouts**, **CSS for styling**, and an **in-memory database** for data storage. **Session management** is implemented via `UserSession` (customers/admins) and `SuppSession` (suppliers). The application consists of **55 files** across four key folders: `main`, `controllers`, `models`, and `view`.

---
## 🎯 Key Features

### 🔑 General
✅ **User Authentication** – Secure login & sign-up with validation (`LoginController`, `SignUpController`).  
✅ **Session Management** – Tracks active users (`UserSession`, `SuppSession`).  
✅ **Data Storage** – Temporary in-memory storage (`Database` class) for users, suppliers, orders, and more.

### 🛍️ Customer Features
🛒 **Product Browsing** – View & search products by category (`ECommerceController`).  
🛒 **Cart Management** – Modify items, adjust quantities (`CartController`).  
🛒 **Checkout** – Apply promo codes (`SAVE10`, `SAVE20`), choose payment methods (`CheckoutController`).  
🛒 **Order History** – View past orders with details (`viewOrderController`).  
🛒 **Profile Management** – Edit account details (`myProfile`).  
🛒 **Personalized Interests** – Select preferred categories for recommendations (`CustomerInterestsController`).

### 🏭 Supplier Features
📦 **Product Management** – Add, edit, and remove products (`addProduct`, `ProductEditController`).  
📦 **Supplier Dashboard** – Manage listings & logout (`suppfxmlController`).  
📦 **Supplier Requests** – Submit account requests (`SignUpRequestController`).

### ⚙️ Admin Features
📊 **Admin Dashboard** – Manage users, orders, suppliers (`admindashController`).  
📊 **User Oversight** – View & manage admins (`AdminViewCtr`), customers (`AdminViewCust`).  
📊 **Supplier Oversight** – Approve or reject registration requests (`SupplierRequestController`).  
📊 **Order Tracking** – Monitor all orders (`viewOrderController`).  
📊 **Profile Management** – Update admin details (`myProfileAdmin`).

---
## 🏗️ Project Structure

📂 **`main`** –
   - `App.java`: Entry point, initializes sample data and loads `welcomePage.fxml`.

📂 **`controllers`** –
   - JavaFX controllers linking UI to logic (e.g., `LoginController`, `CartController`).

📂 **`models`** –
   - `Database`: Manages in-memory storage.
   - `Customer`, `Supplier`, `Admin`: User models.
   - `Order`, `Cart`: Order management with payment logic.
   - `PromoCode`: Handles discounts.

📂 **`view`** –
   - **FXML files**: UI layouts (e.g., `welcomePage.fxml`, `custfxml.fxml`).
   - **CSS Styling**: Enhances UI with `style.css`.

---
## 📌 Prerequisites
✅ **Java Development Kit (JDK)**: Version 8+  
✅ **JavaFX SDK**: Version 11+  
✅ **IDE**: IntelliJ IDEA, Eclipse, or any JavaFX-supported environment

---
## 🚀 Setup Instructions
1️⃣ **Clone the Repository:**  
   ```bash
   git clone <repository-url>
   ```
2️⃣ **Configure JavaFX:**  
   - Download JavaFX SDK from [openjfx.io](https://openjfx.io/).  
   - Add JavaFX to your IDE module path.  
   ```bash
   --module-path /path/to/javafx-sdk/lib --add-modules javafx.controls,javafx.fxml
   ```
3️⃣ **Run the Application:**  
   - Open project in your IDE.  
   - Ensure all resource paths (FXML, CSS) are correctly referenced.  
   - Set `main.App` as the main class and launch.  

---
## 🎮 Usage Guide
🔹 **Launch** – Run `App.java` to open `welcomePage.fxml`.  
🔹 **Customers** – Sign up/login, browse products, add to cart, checkout.  
🔹 **Suppliers** – Request approval, log in, manage products.  
🔹 **Admins** – Log in, manage users, suppliers, orders.  

---
## 📊 Sample Data (Pre-loaded in `App.java`)
👤 **Customer**: Amir – `Username: AmirtheGoat`, `Balance: $1000`  
🏭 **Suppliers**:
   - **NADA** (Approved, sells: Protein shake, Greek yogurt)  
   - **Almara3y** (Pending approval)  
🔑 **Admin**: CEO **Beso** – `Username: beso`, `Working Hours: 9 AM - 12 PM`  
📦 **Orders**: Amir’s cart pre-filled with two products.  

---
## 🔮 Potential Future Improvements
✅ **Persistent Database Integration** – Use SQLite/MySQL for better data storage.  
✅ **Enhanced Admin Features** – Save changes in admin profiles.  
✅ **Optimized Category Mapping** – Ensure accurate product categorization.  
✅ **Refined UI & UX** – Improve validation messages and design responsiveness.  

---
## 🤝 Contributing
🔹 Fork the repository.  
🔹 Create a new feature branch.  
🔹 Submit a **pull request** with a clear description.  



