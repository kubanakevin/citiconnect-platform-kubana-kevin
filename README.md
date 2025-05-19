CitiConnect-Kubana-Kevin

### You have first to run this becouse i remove the Node_modules file of Frontend (folder) for making project small
.... cd frontend
..... npm install
..... npm start

## 🏡CitiConnect

A web-based platform that allows citizens to submit, track, and get responses to complaints related to public services. Government agencies can respond to complaints and update their statuses in real time.

---

## 📌 Features

* Citizens can submit complaints about public services.
* Users can track the status of complaints using their Complaint ID / National ID.
* Agencies can respond to complaints and update their status.
* Admin panel for viewing all complaints, responses, and citizen details.

---

## 📁 Project Structure

```
📆citizen-complaint-system
 ├ 📂frontend           # React frontend
 ┗ 📂backend          # Express backend 
   ├ 📌server.js
   ├ 📌citiconnect(database)
   ├
```

---

## ⚙️ Tech Stack

* **Frontend:** React, Bootstrap
* **Backend:** Node.js, Express
* **Database:** MySQL
* **HTTP Client:** Axios

---

## 🚀 Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/citizen-complaint-system.git
cd citizen-complaint-system
```

### 2. Set Up the Backend

```bash
cd server
npm install
cp .env.example .env  # Add your MySQL credentials here

# Example .env
DB_HOST=localhost
DB_USER=root
DB_PASS=yourpassword
DB_NAME=citiconnect
PORT=8081
```

Create your database and import the schema:

```sql
CREATE DATABASE complaints_db;

-- Example table (simplified)
CREATE TABLE complaints (
  complaint_id INT AUTO_INCREMENT PRIMARY KEY,
  citizen_name VARCHAR(100),
  nationalid VARCHAR(16),
  agency_name VARCHAR(100),
  category VARCHAR(100),
  subject VARCHAR(255),
  description TEXT,
  status VARCHAR(50)
);

CREATE TABLE responses (
  response_id INT AUTO_INCREMENT PRIMARY KEY,
  complaint_id INT,
  responder_id VARCHAR(50),
  message TEXT,
  FOREIGN KEY (complaint_id) REFERENCES complaints(complaint_id)
);


users(user_id,username,email,phone,agency,password,created_at)
```

Start the server:

```bash
npm run dev
```

Server will run at `http://localhost:8081`

---

### 3. Set Up the Frontend

```bash
cd ../client
npm install
npm start
```

Frontend will run at `http://localhost:3000`

---

## 🥪 How to Use the System

### Submit a Complaint

1. Navigate to the homepage.
2. Fill in your personal information and complaint details.
3. Submit the complaint and receive a **Complaint ID or Use NAtional Id**.

### Track Complaint Status

1. Go to the **Track Status** page.
2. Enter your **Complaint ID or National ID**.
3. View the latest status and response from the agency.

### Respond to Complaint (Agency Side)

1. Log in to the agency dashboard (if implemented).
2. View list of assigned complaints.
3. Click on a complaint and submit a response.
4. Status will update to **In Progress** or **Resolved**.

---

## 📸 Screenshots

| Submit Complaint                    
 | --------------------------------- |
![submit compla](https://github.com/user-attachments/assets/e053eacb-8000-4800-b310-938c4c92cb4b)

 
| Track Status                      |
| -----------------------------------
| |![track Status](https://github.com/user-attachments/assets/205ea8f5-ba5e-4949-8353-792bc8973613) 


---

## 👨‍💼 Contributing

1. Fork the repo
2. Create a feature branch: `git checkout -b feature-name`
3. Commit changes: `git commit -m 'Add feature'`
4. Push to the branch: `git push origin feature-name`
5. Create a pull request

---

## 📜 License

MIT License © 2025 KUBANA Kevin



## First User 
. I made the free account creation so it can be easy to use it but i can hide the account creation for agency header but i made it free , you will see it on the Login page 
.Enter Username,Email,Phone,Password,add Agency your
.click Register in order to get access to system 
