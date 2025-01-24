# Live Report(24/01/2025)

**Date**: 24-01-2025

---

## Session 1

- **Start Time**: 8:41 AM
- **Task**: Complete the pending GitHub workshop
- **End Time**: 11:15 AM

---

## Session 2

- **Start Time**: 4:41 PM
- **Task**: Make a website and convert it into a PWA
- **Status**: I have made a PWA
- **Link**: [PWA Link](http://127.0.0.1:5500/index.html)
- **End Time**: 10:50 PM










# Progressive Web App (PWA):-

A **Progressive Web App (PWA)** is a web application that uses modern web technologies to deliver an app-like experience to users. PWAs work on any standards-compliant browser and provide features such as offline access, push notifications, and installability without requiring an app store.

## Key Features of PWAs

- **Progressive**: Compatible with any browser, providing enhanced features for supported browsers.
- **Responsive**: Adapts to different screen sizes and devices.
- **Offline Capabilities**: Functions without an internet connection using cached resources.
- **App-Like**: Mimics the look and feel of a native app.
- **Installable**: Can be added to the home screen without an app store.

---

## PWA Prerequisites

To build a PWA, ensure the following:

1. **Secure HTTPS Connection**: PWAs must be served over HTTPS for secure communication.
2. **Web Application**: A functioning website or web app forms the foundation of your PWA.
3. **Manifest File**: Defines metadata (name, icons, theme, etc.) and enables installation.
4. **Service Worker**: A JavaScript file that enables offline capabilities and caching.

---

## PWA Example

### HTML Code
```html
<!doctype html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <title>PWA</title>
    <link rel="manifest" href="manifest.json">
    <link rel="stylesheet" href="css/style.css">
  </head>
  <body>
    <header>
      <h1>Welcome to My Simple PWA</h1>
      <p>Hi, I'm Manvir Singh. Here's a little about me!</p>
    </header>
    <main>
      <section id="about">
        <h2>About Me</h2>
        <p>I am passionate about learning new things and creating fun projects.</p>
      </section>
      <section id="contact">
        <h2>Contact Me</h2>
        <form>
          <label for="name">Name:</label>
          <input type="text" id="name" name="name" required>
          <br>
          <label for="email">Email:</label>
          <input type="email" id="email" name="email" required>
          <br>
          <button type="submit">Submit</button>
        </form>
      </section>
    </main>
    <footer>
      <p>&copy; 2025 Manvir Singh</p>
    </footer>
    <!-- Register Service Worker -->
    <script>
      if ("serviceWorker" in navigator) {
        window.addEventListener("load", () => {
          navigator.serviceWorker
            .register("/sw.js")
            .then(() => console.log("Service Worker Registered"))
            .catch((error) => console.error("Service Worker Registration Failed:", error));
        });
      }
    </script>
  </body>
</html>
```
**Explanation:**
- The `<head>` section links the `manifest.json` and a CSS stylesheet.
- The `<header>` introduces the app.
- The `<main>` contains two sections: About Me and Contact Me.
- The `<footer>` adds copyright details.
- The `<script>` registers the service worker.

---

### CSS Code
```css
/* Reset default margin and padding */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

/* Body style */
body {
    font-family: 'Arial', sans-serif;
    background: #f0f0f0;
    padding: 20px;
    color: #333;
    text-align: center;
}

/* Header style */
header {
    margin-bottom: 20px;
    padding: 20px;
    background: #4CAF50;
    color: white;
    border-radius: 10px;
}

header h1 {
    font-size: 2.5rem;
}

/* Section style */
section {
    margin: 20px auto;
    padding: 20px;
    background: #fff;
    border-radius: 10px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
}

section h2 {
    font-size: 1.8rem;
}

/* Form styling */
form {
    margin-top: 10px;
    text-align: left;
}

label {
    font-size: 1rem;
    display: block;
    margin-bottom: 5px;
}

input {
    width: 100%;
    padding: 10px;
    margin-bottom: 15px;
    border: 1px solid #ddd;
    border-radius: 5px;
}

button {
    padding: 10px 20px;
    font-size: 1rem;
    border: none;
    border-radius: 5px;
    background-color: #4CAF50;
    color: white;
    cursor: pointer;
}

button:hover {
    background-color: #45a049;
}

/* Footer style */
footer {
    margin-top: 20px;
    padding: 10px;
    background: #4CAF50;
    color: white;
    border-radius: 10px;
}
```
**Explanation:**
- Resets margin and padding with `*` selector.
- Adds responsive and aesthetic styles to `body`, `header`, `section`, `form`, and `footer`.
- Buttons change color on hover for interactivity.

---

### JavaScript Code for Form Handling
```javascript
document.querySelector("form").addEventListener("submit", (event) => {
    event.preventDefault();
    alert("Thank you for contacting me! I'll get back to you soon.");
});
```
**Explanation:**
- Listens for form submission.
- Prevents default page reload and shows an alert message instead.

---

### Manifest File
```json
{
  "name": "My Simple PWA",
  "short_name": "SimplePWA",
  "start_url": "./index.html",  
  "display": "standalone", 
  "background_color": "#ffffff",
  "theme_color": "#4CAF50",
  "icons": [
    {
      "src": "icons/android-chrome-192x192.png",
      "sizes": "192x192",
      "type": "image/png"
    },
    {
      "src": "icons/android-chrome-512x512.png",
      "sizes": "512x512",
      "type": "image/png"
    }
  ]
}
```
**Explanation:**
- Defines app metadata like name, icons, theme color, and display mode.
- `start_url` specifies the app's entry point.

---

### Service Worker
```javascript
const CACHE_NAME = "v1";
const urlsToCache = [
  "/",
  "/index.html",
  "/css/style.css",
  "/javascript/script.js",
  "/icons/android-chrome-192x192.png", 
  "/icons/android-chrome-512x512.png" 
];

self.addEventListener("install", (event) => {
  event.waitUntil(
    caches.open(CACHE_NAME).then((cache) => {
      return cache.addAll(urlsToCache);
    })
  );
});

self.addEventListener("fetch", (event) => {
  event.respondWith(
    caches.match(event.request).then((cachedResponse) => {
      return cachedResponse || fetch(event.request);
    })
  );
});

self.addEventListener("activate", (event) => {
  const cacheWhitelist = [CACHE_NAME];
  event.waitUntil(
    caches.keys().then((cacheNames) => {
      return Promise.all(
        cacheNames.map((cacheName) => {
          if (!cacheWhitelist.includes(cacheName)) {
            return caches.delete(cacheName);
          }
        })
      );
    })
  );
});
```
**Explanation:**
- **Install**: Caches assets listed in `urlsToCache` during installation.
- **Fetch**: Serves cached assets if available, otherwise fetches from the network.
- **Activate**: Deletes old caches to manage storage.

---

This guide walks you through the creation of a fully functional PWA with detailed explanations for each part of the implementation. Happy coding!

