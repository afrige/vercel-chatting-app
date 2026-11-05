# Yap Platform (core)
Express + SQLite + Socket.IO + vanilla JS.
## Run
```
npm install
cp .env.example .env   # set OWNER_EMAIL, OWNER_SETUP_KEY (keep OWNER_USERNAME=jei)
npm start              # http://localhost:3000
```
## Become owner
Register with the exact OWNER_EMAIL, username `jei`, and the OWNER_SETUP_KEY (shown in the register form). Ownership is decided only on the server from env + DB (`users.is_owner`); owner gets permanent Plus and the Owner badge. Only one owner can exist.
## Implemented
Register/login/logout (bcrypt, HttpOnly session cookie, rate-limited), owner provisioning, servers, invites, channels, persistent real-time messages (Socket.IO, membership checked server-side), pagination API, badges (10 seeded, shown by usernames), bot creation with hashed one-time tokens.
## Not built yet
Google OAuth, password reset, avatars/uploads, roles/permissions, voice, DMs, replies/reactions/edit/delete/search, preset bots, bot runtime + sandbox + SDK, verified-bot review, Plus billing, Discover, admin dashboard, notifications, settings pages. Untested: dependencies could not be installed in the build environment.
