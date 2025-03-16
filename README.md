# **REST API Form Interaction**

A web application that demonstrates CRUD operations (Create, Read, Update, Delete) using a form-based interface and integrates with the **Secrets API**. This project allows users to interact with an external API by performing different HTTP requests via a user-friendly form.

---

## **Features**
- **CRUD Operations**:
  - **GET**: Retrieve a secret using its ID.
  - **POST**: Create a new secret with an ID, score, and content.
  - **PUT**: Replace an existing secret entirely.
  - **PATCH**: Update specific fields of an existing secret (e.g., score).
  - **DELETE**: Remove a secret using its ID.
- **Dynamic Feedback**:
  - Displays API responses directly in the interface for user clarity.
- **Responsive Interface**:
  - Simplistic and clean design for a seamless user experience.
- **Integrated with the Secrets API**:
  - Demonstrates how to authenticate and interact with an external API using a bearer token.

---

## **Technologies Used**
- **Node.js**: Backend runtime for server-side execution.
- **Express.js**: Framework for handling routing and middleware.
- **Axios**: For making HTTP requests to the Secrets API.
- **EJS (Embedded JavaScript Templates)**: For rendering dynamic content in the front-end.
- **CSS**: For styling the front-end interface.
- **body-parser**: Middleware for parsing form data.

---

## **Getting Started**

### **Prerequisites**
- **Node.js**: Ensure Node.js is installed on your system.

---

### **Installation**
1. Clone the repository:
   ```bash
   git clone https://github.com/Ayu1404/REST-API-Form-Interaction.git
   cd REST-API-Form-Interaction
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Add your **Bearer Token**:
   - Replace the placeholder value in `server.js`:
     ```javascript
     const yourBearerToken = "your-bearer-token";
     ```

4. Start the server:
   ```bash
   node server.js
   ```

5. Open your browser and navigate to:
   ```plaintext
   http://localhost:3000
   ```

---

## **How to Use**
1. **Access the Form**:
   - Open the web app in your browser at `http://localhost:3000`.
2. **Perform Operations**:
   - Use the form to interact with the Secrets API:
     - Enter an ID, secret, and score as required for each operation.
     - Select one of the buttons (`GET`, `POST`, `PUT`, `PATCH`, `DELETE`) to perform the corresponding HTTP request.
3. **View Results**:
   - The API response will be displayed dynamically in the "Response Area" section of the page.

---

## **Routes**
### **Server Routes**
| HTTP Method | Path             | Description                          |
|-------------|------------------|--------------------------------------|
| **GET**     | `/`              | Renders the form interface.          |
| **POST**    | `/get-secret`    | Sends a GET request to retrieve a secret by ID. |
| **POST**    | `/post-secret`   | Sends a POST request to create a new secret. |
| **POST**    | `/put-secret`    | Sends a PUT request to update a secret entirely. |
| **POST**    | `/patch-secret`  | Sends a PATCH request to update part of a secret. |
| **POST**    | `/delete-secret` | Sends a DELETE request to remove a secret by ID. |

---

## **Project Structure**
### **Back-End (server.js)**:
- **Integration**:
  - Communicates with the **Secrets API** using Axios.
  - Authenticates each request using a bearer token.
- **Form Handling**:
  - Parses form data using `body-parser` middleware.
  - Processes user input and sends corresponding requests to the Secrets API.
- **Dynamic Rendering**:
  - Uses EJS to display API responses on the web interface.

### **Front-End (index.ejs)**:
- **Form**:
  - Provides input fields for ID, secret, and score, along with buttons for each HTTP method.
- **Response Display**:
  - Dynamically displays the API's response in the "Response Area."

---

## **Example API Interactions**
### **GET a Secret**
- **Input**:
  - Enter the ID of the secret you want to retrieve.
- **Output**:
  - Displays the retrieved secret's details (e.g., ID, secret, score).

### **POST a Secret**
- **Input**:
  - Enter an ID, secret content, and score.
- **Output**:
  - Displays the confirmation response from the API.

### **PUT a Secret**
- **Input**:
  - Enter an ID, new secret content, and score to replace an existing secret.
- **Output**:
  - Displays the updated secret details.

### **PATCH a Secret**
- **Input**:
  - Enter an ID and only the fields you want to update (e.g., score).
- **Output**:
  - Displays the partially updated secret.

### **DELETE a Secret**
- **Input**:
  - Enter the ID of the secret to delete.
- **Output**:
  - Displays a confirmation message from the API.

---

## **Contributing**
Contributions are welcome! To contribute:
1. Fork this repository.
2. Create a new branch:
   ```bash
   git checkout -b feature/your-feature-name
   ```
3. Commit your changes:
   ```bash
   git commit -m "Add your feature"
   ```
4. Push to your branch:
   ```bash
   git push origin feature/your-feature-name
   ```
5. Open a pull request.

---

## **License**
This project is licensed under the MIT License, allowing you to modify and distribute the project with proper attribution.

---

## **Acknowledgments**
- Thanks to the open-source Secrets API for providing the backend functionality.
- Inspired by the goal of simplifying API interactions for learning and demonstration purposes.
