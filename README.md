# Code Reviewer

A full-stack application for reviewing code, built with a Vite + React frontend and a Node.js/Express backend. This guide covers setup, development, and API integration for both frontend and backend.

---

## Features

- Modern React frontend (Vite)
- RESTful API backend (Node.js/Express)
- Easy local development and API integration

---

## Prerequisites

- [Node.js](https://nodejs.org/) v18 or higher
- [npm](https://www.npmjs.com/) (comes with Node.js)
- (Optional) [Git](https://git-scm.com/)

---

## Getting Started

### 1. Clone the Repository

```sh
git clone https://github.com/your-username/code-reviewer.git
cd code-reviewer
```

### 2. Install Dependencies

#### Frontend

```sh
cd frontend
npm install
```

#### Backend

```sh
cd ../backend
npm install
```

---

## Running the Project Locally

### 1. Start the Backend Server

```sh
cd backend
npm run dev
```
- The backend will typically run on [http://localhost:5000](http://localhost:5000) (check your backend config).

### 2. Start the Frontend Dev Server

Open a new terminal:

```sh
cd frontend
npm run dev
```
- The frontend will run on [http://localhost:5173](http://localhost:5173) (default Vite port).

---

## API Integration

- The frontend communicates with the backend via RESTful APIs.
- Update API endpoints in your frontend code (e.g., in `src/api.js` or similar) to match your backend URL if needed.

Example API call in React:
```js
fetch('http://localhost:5000/api/review', {
  method: 'POST',
  body: JSON.stringify({ code: '...' }),
  headers: { 'Content-Type': 'application/json' }
})
```

---

## Project Structure

```
code-reviewer/
│
├── frontend/      # React + Vite app
│   ├── src/
│   ├── public/
│   └── ...
│
├── backend/       # Node.js/Express API
│   ├── src/
│   └── ...
│
└── README.md
```

---

## Deployment

- Build the frontend for production:
  ```sh
  cd frontend
  npm run build
  ```
- Deploy the backend and serve the built frontend as needed (see backend docs).

---

## Contributing

1. Fork the repo
2. Create your feature branch (`git checkout -b feature/YourFeature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin feature/YourFeature`)
5. Open a pull request

---

## License

MIT

---

## Troubleshooting

- Ensure Node.js version is 18 or higher.
- If you encounter dependency issues, try deleting `node_modules` and `package-lock.json`, then run `npm install` again.
- For API errors, check backend server logs and ensure ports are not blocked.

---

**Happy
