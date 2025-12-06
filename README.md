**how to run Node.js server** 
step by step using the `server.js` file.  

---

## 🛠 Step 1: Install Node.js
- Download and install Node.js from [nodejs.org](https://nodejs.org).  
- Verify installation:
  ```bash
  node -v
  npm -v
  ```
  This should print the installed versions.

---

## 📂 Step 2: Project Setup
1. Create a new folder for your project, e.g. `mysimplesite`.
2. Inside it, create:
   - `server.js` → paste the code you shared.
   - `index.html` → a simple homepage (e.g. `<h1>Hello Node.js Server</h1>`).
   - Optionally `404.html` → for custom error page.

Your folder might look like:
```
myserver/
│
├── server.js
├── index.html
└── 404.html
```

---

## ▶️ Step 3: Run the Server
Open a terminal in the project folder and run:

```bash
node server.js
```

If successful, you’ll see:
```
Server running on port 2060
```

---

## 🌐 Step 4: Access the Server
- Open a browser and go to:
  ```
  http://localhost:2060
  ```
- You should see your `index.html` page.  
- If you request a non-existent file (e.g. `/abc.html`), the server will serve `404.html`.

---

## ⚙️ Step 5: Change Port (Optional)
- The server uses:
  ```js
  const PORT = process.env.PORT || 2060;
  ```
- To run on a different port, set the environment variable:
  ```bash
  PORT=3000 node server.js   # Linux/Mac
  set PORT=3000 && node server.js   # Windows (cmd)
  ```
- Then visit `http://localhost:3000`.

---

## 🔎 How It Works (Quick Breakdown)
- **`http.createServer`** → creates the server.  
- **`req.url`** → determines which file to serve.  
- **`fs.readFile`** → reads the file from disk.  
- **MIME map** → ensures correct content type (HTML, CSS, JS, images, etc.).  
- **Error handling** → serves `404.html` if file not found, or `500` if server error.  

---

Sam, since you’re teaching, would you like me to also prepare a **student-friendly lab exercise** where they modify this server to serve CSS/JS files and see live changes? That way they can connect Django’s static file concept with Node’s file serving.
