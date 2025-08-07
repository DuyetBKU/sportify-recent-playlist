# 🎵 Spotify Recently Played — README Generator

<p align="center">
  <img src="https://github.com/DuyetBKU/sportify-recent-playlist/assets/spotify-preview.gif" width="420" alt="Spotify Preview GIF"/>
</p>

A simple web app that lets you display your recently played Spotify tracks in your GitHub README — beautifully and automatically.

> 📌 Created by **[@DuyetBKU](https://github.com/DuyetBKU)**. Inspired by [JeffreyCA](https://github.com/JeffreyCA)'s [spotify-recently-played-readme](https://github.com/JeffreyCA/spotify-recently-played-readme.git).

---

## 🚀 Features

-   🟢 OAuth2 login with Spotify
-   📊 Show your recently played tracks
-   🔁 Auto-refreshes every 5 minutes via Firebase
-   🧾 Generates GitHub-friendly Markdown snippet
-   ☁️ Hosted with Firebase Functions

---

## 📦 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/DuyetBKU/sportify-recent-playlist.git
cd sportify-recent-playlist
```

### 2. Install dependencies

```bash
npm install
```

### 3. Create your `.env.local` file

Create a `.env.local`or `.env.example` or some else name file in the root and add the following:

```env
NEXT_PUBLIC_REDIRECT_URI=http://127.0.0.1:3000/
NEXT_PUBLIC_BASE_URL=http://127.0.0.1:3000
NEXT_PUBLIC_CLIENT_ID=your_spotify_client_id
CLIENT_SECRET=your_spotify_client_secret
FIREBASE_PROJECT_ID=your_firebase_project_id
FIREBASE_PRIVATE_KEY_B64=your_firebase_private_key_base64
FIREBASE_CLIENT_EMAIL=your_firebase_client_email
FIREBASE_DATABASE_URL=https://your_project.firebaseio.com
WARMUP_KEY=your_custom_warmup_key
```

> ⚠️ **NOTE:** Use `127.0.0.1` instead of `localhost` in Spotify Redirect URI settings.

### 4. Run the app

```bash
npm run dev
```

---

## 🛠 Setup Spotify App

1. Go to [Spotify Developer Dashboard](https://developer.spotify.com/dashboard)
2. Create a new app
3. Set the **Redirect URI** to:  
   `http://127.0.0.1:3000/`
4. Get your **Client ID** and **Client Secret**
5. Update `.env.local` accordingly

---

## 🔐 Firebase Setup (Optional for Hosting)

If you want to deploy it on Firebase:

-   Create a Firebase project
-   Enable Realtime Database
-   Create a Firebase Service Account and encode the private key in Base64
-   Update your `.env.local`

To deploy:

```bash
npm run deploy
```

---

## 📋 Example Markdown Snippet

Once logged in, you’ll get a markdown snippet like:

```md
[![Spotify Recently Played](https://spotify-recent-playlist.web.app/api/spotify-recently-played?user=your_spotify_user)](https://open.spotify.com/user/your_spotify_user)
```

Paste that in your GitHub README.md file!

---

## 🙌 Credits

-   Inspired by: [JeffreyCA](https://github.com/JeffreyCA)'s [spotify-recently-played-readme](https://github.com/JeffreyCA/spotify-recently-played-readme)
-   Built with: Next.js, Firebase, Spotify API, Ant Design

---

## 📜 License

MIT © DuyetBKU
