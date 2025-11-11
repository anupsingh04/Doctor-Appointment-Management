# 🏥 ZeeCare - Hospital Appointment Management System

Welcome to ZeeCare, a full-stack web application designed to streamline hospital appointment management. This system provides a seamless, role-based experience for patients and administrators, built on the MERN stack (MongoDB, Express.js, React.js, Node.js).

---

### 🚀 Live Demo

* **Frontend (Patient App):** [https://doctor-appointment-management-silk.vercel.app/](https://doctor-appointment-management-silk.vercel.app/)
* **Dashboard (Admin App):** [https://doctor-appointment-management-dashb.vercel.app/](https://doctor-appointment-management-dashb.vercel.app/)

---

### ✨ Key Features

#### Patient (Frontend)
* **User Authentication**: Secure Patient registration and login.
* **Browse Doctors**: View a list of all available doctors and their specializations.
* **Book Appointment**: Fill out a comprehensive form to book an appointment with a specific doctor from a specific department.
* **Send Messages**: A "Contact Us" form for patients to send messages directly to the hospital staff.
* **Responsive UI**: A fully responsive design for seamless use on all devices.

#### Admin (Dashboard)
* **Secure Admin Login**: Separate, role-protected login for administrators.
* **Main Dashboard**: An overview of total appointments, registered doctors, and other key stats.
* **Appointment Management**: View all appointments with the ability to update their status (Pending, Accepted, Rejected).
* **Doctor Management**: Add new doctors to the system (with avatar uploads) and view all registered doctors.
* **Admin Management**: Add new administrators to the dashboard.
* **View Messages**: Read and manage all messages sent by patients via the contact form.
* **Role-Based Access Control**: Securely ensures that only authenticated admins can access the dashboard and its features.

---

### 💻 Tech Stack

| Category | Technology |
| :--- | :--- |
| **Backend** | Node.js, Express.js, MongoDB (Mongoose), JWT (JSON Web Tokens), Bcrypt, Cloudinary (for image uploads) |
| **Frontend** | React.js, Vite, React Router DOM, Axios, React Toastify |
| **Dashboard** | React.js, Vite, React Router DOM, Axios, React Toastify, React Context API |
| **Database** | MongoDB Atlas |

---

### 🚀 Getting Started: Running Locally

To get a local copy up and running, follow these steps.

#### Prerequisites

You will need the following software installed on your machine:
* [Node.js](https://nodejs.org/en/) (v18 or later)
* [Git](https://git-scm.com/)
* [MongoDB Atlas](https://www.mongodb.com/cloud/atlas) account (for the database)
* [Cloudinary](https://cloudinary.com/) account (for image storage)

#### 1. Fork & Clone the Repository

1.  **Fork** the repository by clicking the 'Fork' button on the top-right corner of the GitHub page.
2.  **Clone** your forked repository to your local machine:
    ```bash
    git clone [https://github.com/](https://github.com/)<YOUR_GITHUB_USERNAME>/DOCTOR_APPOINTMENT_MANAGEMENT_WEB_APPLICATION.git
    ```
3.  Navigate into the project's root directory:
    ```bash
    cd DOCTOR_APPOINTMENT_MANAGEMENT_WEB_APPLICATION
    ```

#### 2. Backend Setup

The backend server is the brain of the application.

1.  Navigate into the `backend` directory:
    ```bash
    cd backend
    ```
2.  Install all required npm packages:
    ```bash
    npm install
    ```
3.  Create a `.env` file in the `backend` directory and add the following environment variables.

    **`backend/.env`**
    ```env
    # MongoDB Connection String
    MONGO_URI=your_mongodb_connection_string

    # JWT (Authentication)
    JWT_SECRET_KEY=your_super_secret_jwt_key
    JWT_EXPIRES=10d

    # Cloudinary (Image Uploads)
    CLOUDINARY_CLOUD_NAME=your_cloudinary_cloud_name
    CLOUDINARY_API_KEY=your_cloudinary_api_key
    CLOUDINARY_API_SECRET=your_cloudinary_api_secret

    # Client URLs (Crucial for CORS & Cookies)
    # --- For Local Development ---
    FRONTEND_URL=http://localhost:5173
    DASHBOARD_URL=http://localhost:5174
    
    # --- For Production (after deploying) ---
    # FRONTEND_URL=[https://doctor-appointment-management-silk.vercel.app](https://doctor-appointment-management-silk.vercel.app)
    # DASHBOARD_URL=[YOUR_DEPLOYED_DASHBOARD_URL]
    ```

#### 3. Frontend (Patient) Setup

This is the public-facing client.

1.  From the root directory, navigate into the `frontend` directory:
    ```bash
    cd ../frontend
    ```
2.  Install all required npm packages:
    ```bash
    npm install
    ```
3.  Create a `.env` file in the `frontend` directory. This tells the React app where to find the backend API.

    **`frontend/.env`**
    ```env
    # --- For Local Development (points to local backend) ---
    VITE_API_URL=http://localhost:4000/api/v1
    
    # --- For Production (points to deployed backend) ---
    # VITE_API_URL=[YOUR_DEPLOYED_BACKEND_URL]/api/v1
    ```

#### 4. Dashboard (Admin) Setup

This is the secure admin client.

1.  From the root directory, navigate into the `dashboard` directory:
    ```bash
    cd ../dashboard
    ```
2.  Install all required npm packages:
    ```bash
    npm install
    ```
3.  Create a `.env` file in the `dashboard` directory. This also tells the admin app where to find the backend API.

    **`dashboard/.env`**
    ```env
    # --- For Local Development (points to local backend) ---
    VITE_API_URL=http://localhost:4000/api/v1
    
    # --- For Production (points to deployed backend) ---
    # VITE_API_URL=[YOUR_DEPLOYED_BACKEND_URL]/api/v1
    ```

#### 5. Run the Application

You will need to open **three separate terminals** to run all parts of the application.

* **Terminal 1 (Backend):**
    ```bash
    cd backend
    npm start 
    # (or `npm run dev` if you have a dev script)
    # > Server running on port 4000
    ```

* **Terminal 2 (Frontend):**
    ```bash
    cd frontend
    npm run dev
    # > Vite server running at http://localhost:5173
    ```

* **Terminal 3 (Dashboard):**
    ```bash
    cd dashboard
    npm run dev
    # > Vite server running at http://localhost:5174
    ```

You can now access the applications:
* **Patient App:** `http://localhost:5173`
* **Admin Dashboard:** `http://localhost:5174`

---

### 🤝 How to Contribute

Contributions are welcome! If you'd like to contribute, please follow these steps:

1.  **Fork** the repository (if you haven't already).
2.  **Clone** your fork to your local machine.
3.  Create a new branch for your feature or bug fix:
    ```bash
    git checkout -b feature/your-awesome-feature
    ```
4.  Make your changes and commit them with descriptive messages:
    ```bash
    git commit -m "feat: Add your-awesome-feature"
    ```
5.  Push your changes to your forked repository:
    ```bash
    git push origin feature/your-awesome-feature
    ```
6.  Open a **Pull Request (PR)** from your branch to this repository's `main` branch. Please provide a clear description of your changes.

---

### 👤 Author

**Anup Kumar**
* GitHub: [@anupsingh04](https://github.com/anupsingh04)
* Mail: [anupsingh727716@gmail.com](https://mailto:anupsingh727716@gmail.com/)
