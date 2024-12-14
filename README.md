# Asir Connect

## Project Description
**Asir Connect** is a social network developed for the SAD module. Its purpose is to share information in an educational environment, facilitating collaboration and communication among students.

---

## Features
- **User Authentication:**
  - Secure registration with password hashing.
  - Login protected by session management.
- **Profile Management:**
  - Avatar upload and profile updates.
  - Option to delete user accounts.
- **Social Features:**
  - Post text and images.
  - View and interact with posts from all users.
- **Security Features:**
  - Password validation rules.
  - SQL injection prevention using prepared statements.
  - Cross-Site Scripting (XSS) protection with `htmlspecialchars`.

---

## Development and Deployment Requirements

To develop and deploy this web application, you will need the following components:

| Component                | Details                                                  |
|--------------------------|----------------------------------------------------------|
| **Web Server**           | Apache2                                                  |
| **Programming Language** | PHP                                                      |
| **Database**             | MariaDB                                                  |
| **Frontend**             | HTML, CSS                                                |

---

## Application Workflow

Here is an overview of how **Asir Connect** works:

```mermaid
graph LR
A[User Registers] --> B{Validates Password?}
B -- No --> C[Error Message]
B -- Yes --> D[Stores User in DB]
D --> E[User Logs In]
E --> F{Session Active?}
F -- No --> G[Redirect to Login]
F -- Yes --> H[Dashboard Access]
H --> I[Create Post]
H --> J[Edit Profile]
H --> K[Delete Account]
