# Fake Profile Identification using Machine Learning and NLP

![Python](https://img.shields.io/badge/Python-3.7%2B-blue.svg) ![Django](https://img.shields.io/badge/Django-3.2-green.svg) ![Scikit-learn](https://img.shields.io/badge/scikit--learn-brightgreen.svg) ![MySQL](https://img.shields.io/badge/MySQL-blue.svg)
## 📖 Project Overview

Social networking sites are an integral part of modern life, but they also present significant security challenges. Malicious actors often create fake profiles to engage in undesirable activities, including fraud, campaigning, and identity theft. This project proposes a robust system to identify such fake profiles by analyzing various profile attributes. It uses a combination of machine learning classifiers like **Support Vector Machine (SVM)** and **Naïve Bayes** to achieve a higher detection accuracy rate compared to traditional methods.

## ✨ Key Features

This application is divided into two main roles: the Service Provider (Admin) and the Remote User.

### Service Provider (Admin)
* **Secure Login:** Access to a dedicated admin dashboard.
* **Model Training:** Ability to train the ML models on user profile datasets.
* **Performance Visualization:** View the accuracy of trained models through results tables and bar charts.
* **Prediction Monitoring:** See the identity predictions for all profiles in the system.
* **User Management:** View and authorize registered users.
* **Data Export:** Download the datasets with prediction results.

### Remote User
* **User Authentication:** Secure registration and login functionality.
* **Profile Prediction:** Submit profile information to check if it's predicted as fake or genuine.
* **Profile Management:** View their own user profile.

## 🧠 Methodology

The core of this project lies in its analytical approach to distinguishing between real and fake profiles.

1.  **Data Collection:** The system analyzes profiles based on both static and dynamic data.
    * **Static Data:** Information provided by the user at the time of profile creation (e.g., name, bio, creation date).
    * **Dynamic Data:** Details observed by the system about the user's behavior and network locality.

2.  **Feature Extraction:** Key attributes from a user's profile are used for classification. These include:
    * `statuses_count`, `followers_count`, `friends_count`, `description`, `location`, `created_at`, and whether the profile uses a default image.

3.  **Machine Learning Models:** The project implements and analyzes several classification algorithms to find the most effective model.
    * **Proposed Models:** Support Vector Machine (SVM) and Naïve Bayes.
    * **Other Analyzed Models:** Decision Tree, Logistic Regression, and Random Forest.

## 🛠️ Tech Stack

This project is built using a combination of modern web development and data science technologies.

* **Backend:** Python, Django-ORM
* **Frontend:** HTML, CSS, JavaScript
* **Database:** MySQL
* **Web Server:** Apache (via XAMPP)
* **Machine Learning:** Scikit-learn (inferred from the use of SVM, Naive Bayes, etc.)
* **Deployment Environment:** Windows

## 🏗️ System Architecture

The application follows a client-server architecture where the Django backend processes all user queries and interacts with the MySQL database.

* **Remote Users** and the **Service Provider** interact with the web interface.
* The **Web Server** (Django application) handles logic for training models, making predictions, and managing data.
* The **MySQL Database** stores user data, profile datasets, and prediction results.

## ⚙️ Installation and Setup

Follow these steps to get the project running on your local machine.

### Prerequisites
* [XAMPP](https://www.apachefriends.org/index.html) (includes Apache and MySQL)
* [Python 3.x](https://www.python.org/downloads/)

### 1. Database Setup
1.  Install and launch the **XAMPP Control Panel**.
2.  Start the **Apache** and **MySQL** services.
3.  Open your web browser and navigate to `http://localhost/phpmyadmin/`.
4.  Create a new database and name it `fake_profile_identification`.
5.  Select the new database and go to the "Import" tab.
6.  Upload and import the `.sql` file provided in the project's database folder.

### 2. Project Setup
1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/your-username/fake-profile-identification.git](https://github.com/your-username/fake-profile-identification.git)
    cd fake-profile-identification
    ```

2.  **Create a virtual environment and install dependencies:**
    ```bash
    python -m venv venv
    venv\Scripts\activate
    pip install -r requirements.txt
    ```
    *(Note: A `requirements.txt` file should be created containing `Django`, `mysqlclient`, `scikit-learn`, `pandas`, etc.)*

3.  **Apply database migrations:**
    The project may have unapplied migrations. Run the following command:
    ```bash
    python manage.py migrate
    ```

4.  **Run the development server:**
    ```bash
    python manage.py runserver
    ```
    The application will be available at `http://127.0.0.1:8000`.

## 🚀 Usage

After successfully setting up the project, you can interact with it as follows:

### As a Remote User
1.  Open your browser to `http://127.0.0.1:8000`.
2.  Click on **"Register"** to create a new user account.
3.  Log in with your credentials.
4.  Navigate to the **"Predict Profile Identification Status"** page to use the prediction feature.

### As a Service Provider (Admin)
1.  From the main page, click on **"Service Provider"** to access the admin login portal.
2.  Log in using the admin credentials.
3.  From the dashboard, you can:
    * Train and test the machine learning models.
    * View detailed accuracy results.
    * Manage and authorize users.

## 🧩 Project Modules

The system is logically divided into the following key modules as described in the implementation:

* **Service Provider Module:** Handles all administrative functionalities, including model management and user authorization.
* **Remote User Module:** Manages user registration, login, and the prediction interface for end-users.
* **Testing Module:** The project documentation details a comprehensive testing strategy, including Unit, Integration, System, and User Acceptance testing to ensure robustness and reliability.

## 👨‍💻 Authors

This project was submitted as a field-based project for the Bachelor of Technology in Computer Science and Engineering (DS) by:

* **P.V. KRISHNA GAURAV**
  
## 📄 License

This project is unlicensed. You may want to consider adding an open-source license to define how others can use, modify, and distribute your code. The [MIT License](https://choosealicense.com/licenses/mit/) is a popular and permissive choice for academic projects.
