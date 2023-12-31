# Wallet App Keycloak Configuration

## Part 1: Keycloak Configuration

Follow these steps to configure Keycloak using the reference video [here](https://www.youtube.com/watch?v=vNKVm2vTL2Q).

### 1. Download and Start Keycloak 19

- Download Keycloak version 19 from [this link](https://www.keycloak.org/downloads).
- Start Keycloak following the instructions for your operating system.

### 2. Create an Admin Account

- Access the admin interface (default at http://localhost:8080/admin).
- Create an admin account to manage Keycloak.
  
![](./screenshots/sc-1.png)

### 3. Create a Realm

- Add a new "Realm" in the admin interface.
- This "Realm" will group clients, users, and roles related to your application.
  
![](./screenshots/sc-2.png)

### 4. Create a Client to Secure

- Within the created "Realm," add a new "Client" representing your application.
- Configure client settings and note the "Client ID" and "Client Secret."
  
![](./screenshots/sc-3.png)

### 5. Create Users and Roles

- Add users to the "Realm."
- Create specific roles for your application.
  
![](./screenshots/sc-4.png)
![](./screenshots/sc-5.png)
![](./screenshots/sc-6.png)

### 6. Assign Roles to Users

- Assign created roles to corresponding users in the "Realm."
  
![](./screenshots/sc-7.png)
![](./screenshots/sc-8.png)

### 7. Use Postman

- Utilize Postman to test authentication and explore tokens.

  - **Test Authentication with Password**
    - Authenticate using Postman with a password.
      
  ![](./screenshots/sc-9.png)

  - **Analyze JWT Access Token and Refresh Token Contents**
    - Analyze the contents of generated access and refresh tokens.
      
  ![](./screenshots/sc-10.png)
  ![](./screenshots/sc-11.png)

  - **Test Authentication with Refresh Token**
    - Authenticate using the refresh token.
      
  ![](./screenshots/sc-12.png)
  ![](./screenshots/sc-13.png)
  ![](./screenshots/sc-14.png)

  - **Test Authentication with Client ID and Client Secret**
    - Authenticate using "Client ID" and "Client Secret."
      
  ![](./screenshots/sc-15.png)
  ![](./screenshots/sc-16.png)

  - **Modify Token Parameters**
    - Experiment with modifying parameters of Access Token and Refresh Token.

## Part 2: Secure Wallet App with Keycloak

- Integrate Keycloak into your Wallet App using the configuration obtained earlier.

---

*Note: Refer to the official Keycloak documentation for specific details and advanced information: [Keycloak Documentation](https://www.keycloak.org/documentation.html).*
