# Orbitchat

A real-time, school-focused multi-room chat app with a space theme, built with React, Vite, Express, and Socket.IO.

## Run locally

Install Node.js 18 or newer, then run:

```bash
npm install
npm run dev
```

Open the Vite URL printed in the terminal (usually `http://localhost:5173`). The development server starts the chat server alongside it.

For a production build, run `npm run build`, then `npm start`. The server serves the built website and hosts the Socket.IO connection on the same port.

## Names and chatrooms

The starter rooms are Main Chat, Chatroom 1, and Chatroom 2. Active display names are unique without regard to capitalization and are reserved across every room. Names must be 2–24 characters and use letters, spaces, apostrophes, or hyphens. Profanity and common placeholder names are blocked. The server validates names, room names, and messages; clients cannot bypass those checks. People can switch rooms or create new ones.

The app does not set an arbitrary connection limit. Real capacity depends on the machine and hosting environment. Rooms and message history are held in server memory, so they reset when the server restarts; use a shared database and Socket.IO adapter before scaling to multiple server instances.