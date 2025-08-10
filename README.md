# 🏢 Visitor Management System

A simple **web application** for managing visitor check-ins and check-outs with SMS and Email notifications to the host. Designed for offices, events, or any place where visitor tracking is essential.

---

## 📖 Introduction
The application provides two main options: **Check-In** and **Check-Out**.

1. **Check-In**
   - Visitor enters their own details along with the host's details.
   - An SMS and email are sent to the host containing the visitor's information.

2. **Check-Out**
   - Visitor enters their registered email ID for verification.
   - Upon verification, the visitor is checked out of the system.

---

## 🔄 Workflow
1. Visitor chooses **Check-In**.
2. Fills in:
   - **Visitor Details** (Name, Email, Phone)
   - **Host Details** (Name, Email, Phone)
3. Visitor may later choose **Check-Out**.
4. Enters their **email ID** for verification.
5. After verification, the system checks them out.
6. Visitors can check in and out independently of other visitors.

---

## 🗄 Database Structure
The database `user` has **three collections** to avoid redundancy:
### Clients
| Field  | Description       |
|--------|-------------------|
| name   | Visitor Name       |
| email  | Visitor Email      |
| phone  | Visitor Phone      |

### Hosts
| Field  | Description       |
|--------|-------------------|
| hname  | Host Name          |
| hemail | Host Email         |
| hphone | Host Phone         |

### Visits
| Field    | Description         |
|----------|---------------------|
| email    | Visitor Email        |
| checkin  | Check-In Timestamp   |
| checkout | Check-Out Timestamp  |
| hemail   | Host Email           |



I have made 3 collections so as to reduce redundancy in the database. Even if a visitor has visited the office more than once, his details will only be stored once in the Clients collection. The same goes for the Host's Details.

Screenshots:
Entry Management System's Home Page.
<img width="1920" height="1030" alt="Home" src="https://github.com/user-attachments/assets/ee823cf8-d878-4a84-9096-ae21d1ccf2c3" />

Check-in Portal.
<img width="1920" height="1027" alt="Checkin" src="https://github.com/user-attachments/assets/c9b0944d-ef10-44e0-bf4f-25b03b6b3651" />

Check-in Success Message.
<img width="1920" height="1027" alt="Success_checkin" src="https://github.com/user-attachments/assets/a1a1a154-e4d2-44b4-a65d-0ef9b522b5b6" />

Check-out Portal.
<img width="1920" height="1027" alt="Checkout" src="https://github.com/user-attachments/assets/2a468f9c-9349-4765-9e6a-b158b6ef88ce" />

Check-out Success Message.
<img width="1920" height="1027" alt="Success_checkout" src="https://github.com/user-attachments/assets/855d586f-f900-4cf6-b12d-8e98dc90d9d6" />

Error Messages.
<img width="1915" height="726" alt="Error1" src="https://github.com/user-attachments/assets/40e54816-fa0b-47bd-9cf4-8d499b83b844" />

<img width="1795" height="682" alt="Error2" src="https://github.com/user-attachments/assets/c3e21e98-6885-4d24-a344-db275c06507a" />

<img width="1445" height="472" alt="Error3" src="https://github.com/user-attachments/assets/a5d861fb-004b-4c00-8436-8e485ce07b4e" />

## ⚠️ Corner Cases
1. A visitor **cannot check in** again without first checking out.
2. A visitor **cannot check out** with an email ID that was never used for check-in.
3. A visitor **cannot check out** twice.



