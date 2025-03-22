
# StackShop - Java E-Commerce Application

## Project Overview
StackShop is a Java-based e-commerce platform built with JavaFX, offering a graphical user interface for three user roles: **Customers**, **Suppliers**, and **Administrators**.  
- **Customers** can browse products, manage carts, place orders, and view order history.  
- **Suppliers** can add and manage product listings.  
- **Admins** can oversee users, suppliers, orders, and supplier registration requests.  

The application uses FXML files for UI layouts, a CSS file for styling, and an in-memory `Database` class for data storage. Session management is implemented with `UserSession` for customers and admins, and `SuppSession` for suppliers. The project consists of 55 files distributed across four folders: `main`, `controllers`, `models`, and `view`.

## Features

### General
- **User Authentication**: Role-based login and sign-up with validation (`LoginController`, `SignUpController`, `SignUpRequestController`).  
- **Session Management**: Tracks logged-in users via `UserSession` (customers/admins) and `SuppSession` (suppliers).  
- **Data Storage**: In-memory storage using the `Database` class for users, suppliers, orders, admins, and supplier requests.  

### Customer Features
- **Product Browsing**: View products by category (e.g., Electronics, Fashion) or search, with an "Add to Cart" option (`ECommerceController`).  
- **Cart Management**: Adjust quantities, remove items, and view totals (`CartController`).  
- **Checkout**: Apply promo codes (e.g., `SAVE10`, `SAVE20`), choose payment methods (cash or balance), and complete orders (`CheckoutController`).  
- **Order History**: View past orders with details like status and total price (`viewOrderController`).  
- **Profile Management**: Edit username, password, address, and balance (`myProfile`).  
- **Interests**: Select preferred categories for personalized recommendations (`CustomerInterestsController`).  

### Supplier Features
- **Product Management**: Add products (`addProduct`) and edit prices/stock (`ProductEditController`).  
- **Supplier Dashboard**: Access product management and logout options (`suppfxmlController`).  
- **Registration Requests**: Submit supplier account requests for admin approval (`SignUpRequestController`).  

### Admin Features
- **Dashboard**: Navigate to profile, orders, admins, customers, suppliers, and requests (`admindashController`).  
- **User Oversight**: View admins (`AdminViewCtr`) and customers (`AdminViewCust`) in tables.  
- **Supplier Oversight**: View suppliers (`AdminViewSupp`) and manage registration requests (`SupplierRequestController`).  
- **Order Monitoring**: View all system orders (`viewOrderController`).  
- **Profile Management**: View/edit admin details (`myProfileAdmin`).  

## Project Structure
- **`main`**:  
  - `App.java`: Entry point, initializes sample data (users, products) and loads `welcomePage.fxml`.  
- **`controllers`** (25 files):  
  - JavaFX controllers linking FXML views to logic (e.g., `LoginController`, `CartController`, `addProduct`).  
- **`models`** (14 files):  
  - `Database`: In-memory storage for all data.  
  - `Customer`, `Supplier`, `Admin`: User classes extending `Person`.  
  - `SupplierProduct`, `CustomerProduct`: Product classes for stock and cart management.  
  - `Order`, `Cart`: Manage orders and carts with payment/promo logic.  
  - `PromoCode`: Defines discount codes with rules.  
  - `Category`, `Product`, `View`: Support categorization and display.  
  - `App`: Console-based demo (not GUI-integrated).  
- **`view`** (15 files):  
  - FXML files (e.g., `welcomePage.fxml`, `custfxml.fxml`, `myCart.fxml`) for UI layouts.  
  - `style.css`: Stylesheet for visual customization.  

## Prerequisites
- **Java Development Kit (JDK)**: Version 8 or higher.  
- **JavaFX SDK**: Version 11 or later (required for GUI).  
- **IDE**: IntelliJ IDEA, Eclipse, or similar with JavaFX support.  

## Setup Instructions
1. **Clone the Repository**:  
   ```bash
   git clone <repository-url>
   ```
2. **Configure JavaFX**:  
   - Download the JavaFX SDK from [openjfx.io](https://openjfx.io/).  
   - In your IDE, add the SDK to the module path:  
     - IntelliJ: `File > Project Structure > Libraries > + > JavaFX SDK lib folder`.  
     - Or use VM options:  
       ```bash
       --module-path /path/to/javafx-sdk/lib --add-modules javafx.controls,javafx.fxml
       ```
3. **Compile and Run**:  
   - Open the project in your IDE.  
   - Ensure FXML and CSS files are in the resource directory (e.g., `src/main/resources/views/`).  
   - Set `main.App` as the main class and run.  
4. **Verify Resource Paths**:  
   - Check that controllers reference FXML files correctly (e.g., `/views/welcomePage.fxml`).  

## Usage
1. **Launch**: Run `App.java` to open `welcomePage.fxml`.  
2. **Customers**: Sign up or log in, browse products, manage cart, and checkout.  
3. **Suppliers**: Request registration, await approval, then log in to manage products.  
4. **Admins**: Log in, use the dashboard to manage users, suppliers, and orders.  

## Sample Data (Initialized in `App.java`)
- **Customer**: "Amir" (username: "AmirtheGoat", balance: 1000, interests: Electronics, Fashion).  
- **Suppliers**:  
  - "NADA" (approved, products: Protein shake, Greek yogurt).  
  - "almara3y" (pending request).  
- **Admin**: "beso" (username: "beso", role: CEO, hours: 9-12).  
- **Orders**: Amir’s cart with two products.  

### Potential Improvements
- **Persistent Storage**: Add a database like SQLite or MySQL to save user data, orders, and products between sessions, making the app more robust.
- **Admin Profile Functionality**: Enable saving changes in the admin profile section to allow updates to admin details.
- **Category Mapping**: Fix inconsistent category mappings (e.g., ensuring "Beauty & Fragrance" links to the right category) for a smoother browsing experience.
- **GUI Integration**: Either fully integrate the console-based demo or remove it to streamline the focus on the graphical interface.
- **User Experience**: Improve the UI with better validation messages and a responsive design for a more polished feel.

## Contributing
- Fork the repository.  
- Create a branch for your changes.  
- Submit a pull request with a clear description.  

## Acknowledgments
- Built with JavaFX for a modern UI.  
- Designed for scalability, with potential for future database integration.




