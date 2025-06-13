 
```markdown
![Node.js Blog REST API Banner](https://raw.githubusercontent.com/JeremyG11/gatwech-nguth-assets/main/blog-api-banner.png)
# 📝 Node.js Blog REST API

A modular and production-ready REST API for blogging platforms, built using **Node.js**, **TypeScript**, **Express**, and **MongoDB**. This backend empowers users with features like registration, secure login, blog post creation, commenting, liking, and more – all secured with JWT authentication and featuring cloud image support via Cloudinary.

---

## 🚀 Tech Stack

This project leverages a robust and modern tech stack:

* **Node.js** & **Express**: The core backend runtime and web framework for efficient routing and API development.
* **TypeScript**: Ensures strong typing, leading to more robust, maintainable, and scalable code.
* **MongoDB + Mongoose**: A flexible NoSQL database solution with Mongoose for elegant ODM (Object Data Modeling).
* **🔑 JWT (JSON Web Tokens)**: For secure, stateless authentication and authorization.
* **☁️ Cloudinary**: Integrated for seamless and efficient cloud-based image uploads and management.
* **🪵 Winston**: A powerful logging library for comprehensive application monitoring and debugging.
* **🚦 Rate Limiting**: Implemented to protect the API from abuse and ensure stability.

---

## 📁 Project Structure

The project follows a clear and organized modular structure for better maintainability and scalability:

```

src/
├── config/           \# ⚙️ Application-wide configurations
│ └── index.ts
├── controllers/v1/   \# 💡 Route logic, grouped by resource for API version 1
│ ├── auth/
│ ├── blog/
│ ├── comment/
│ ├── like/
│ └── user/
├── lib/              \# 🛠️ Core libraries and utility modules
│ ├── cloudinary.ts
│ ├── express\_rate\_limit.ts
│ ├── jwt.ts
│ ├── mongoose.ts
│ └── winston.ts
├── middlewares/      \# 🛡️ Custom Express middleware functions
│ ├── authenticate.ts
│ ├── authorize.ts
│ ├── uploadBlogBanner.ts
│ └── validationError.ts
├── models/           \# 📚 Mongoose schemas and models
│ ├── blog.ts
│ ├── comment.ts
│ ├── like.ts
│ ├── token.ts
│ └── user.ts
├── routes/v1/        \# ➡️ Express API routes for version 1
│ ├── auth.ts
│ ├── blog.ts
│ ├── comment.ts
│ ├── like.ts
│ ├── user.ts
│ └── index.ts
├── @types/           \# 🏷️ Custom TypeScript type definitions
│ └── express/
│ └── index.d.ts
├── utils/            \# ✨ General utility functions
│ └── index.ts
└── server.ts         \# 🚀 Application entry point

````

---

## ✨ Features

This API comes packed with powerful features:

* ✅ **JWT-based Authentication**: Secure user login and protected routes.
* ✅ **Cloudinary Image Upload**: Effortless handling of image uploads for blog banners, avatars, etc.
* ✅ **Robust Rate Limiting**: Prevents API abuse and maintains service availability.
* ✅ **Role-Based Access Control (RBAC)**: Fine-grained permissions for different user roles.
* ✅ **Comprehensive Blog Management**: Create, read, update, and delete blog posts with interactive likes and comments.
* ✅ **Modular & Versioned API**: Structured for easy scaling and future enhancements (`v1`).
* ✅ **Clean Error Handling & Validation**: Provides clear, consistent error responses for API consumers.

---

## 📦 Installation

To get started with the project, follow these steps:

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/JeremyG11/TS-node-blog-RESTAPI.git](https://github.com/JeremyG11/TS-node-blog-RESTAPI.git)
    cd TS-node-blog-RESTAPI
    ```
2.  **Install dependencies** (using pnpm is recommended):
    ```bash
    pnpm install
    ```

---

### 🧪 Running the App

Choose your desired environment to run the API:

**Development Mode (with hot-reloading)**

```bash
pnpm dev
````

**Production Mode (build and start)**

```bash
pnpm build && pnpm start
```

-----

### 📬 API Endpoints (v1)

Here's a list of the available API endpoints and their authentication requirements:

| Method | Endpoint                     | Description                    | Authentication |
| :----- | :--------------------------- | :----------------------------- | :-------------: |
| `POST` | `/api/v1/auth/register`      | Register a new user            |       ❌       |
| `POST` | `/api/v1/auth/login`         | Login and obtain a JWT token   |       ❌       |
| `GET`  | `/api/v1/blog`               | Retrieve a list of all blog posts |       ❌       |
| `GET`  | `/api/v1/blog/:id`           | Get a single blog post by ID   |       ❌       |
| `POST` | `/api/v1/blog`               | Create a new blog post         |       ✅       |
| `PUT`  | `/api/v1/blog/:id`           | Update an existing blog post   |       ✅       |
| `DELETE`| `/api/v1/blog/:id`           | Delete a blog post             |       ✅       |
| `POST` | `/api/v1/blog/:id/comment`   | Add a comment to a specific post |       ✅       |
| `POST` | `/api/v1/blog/:id/like`      | Like a specific post           |       ✅       |

-----

### 🧰 Scripts

Useful `pnpm` scripts for development and build processes:

| Script     | Description                                |
| :--------- | :----------------------------------------- |
| `pnpm dev`   | Starts the development server with hot-reloading |
| `pnpm build` | Transpiles TypeScript code to JavaScript   |
| `pnpm start` | Runs the compiled production build         |
| `pnpm lint`  | Executes ESLint for code quality checks    |

-----

### 🪪 License

This project is licensed under the [MIT License](https://opensource.org/licenses/MIT).

Copyright (c) 2025 Gatwech Tap Nguth

-----

### 👨‍💻 Author

**Gatwech Tap Nguth**

  * GitHub: [@JeremyG11](https://www.google.com/search?q=https://github.com/JeremyG11)
  * Email: [gatwech3211@gmail.com](mailto:gatwech3211@gmail.com)

🔗 **Repository:** [https://github.com/JeremyG11/TS-node-blog-RESTAPI](https://github.com/JeremyG11/TS-node-blog-RESTAPI)

```
```