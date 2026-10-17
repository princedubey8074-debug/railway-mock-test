# Railway Mock Test — full-stack starter

## Run
1. Install Node.js 20+.
2. Unzip this folder and open terminal in it.
3. Run `npm install`.
4. Set secrets, then run `npm start`.
   - Linux/macOS:
     `export JWT_SECRET="$(node -e \"console.log(require('crypto').randomBytes(48).toString('hex'))\")"`
     `export ADMIN_USERNAME="owner"`
     `export ADMIN_PASSWORD="choose-a-unique-password-at-least-12-chars"`
   - Windows PowerShell:
     `$env:JWT_SECRET="replace-with-random-secret-at-least-32-characters"`
     `$env:ADMIN_USERNAME="owner"`
     `$env:ADMIN_PASSWORD="choose-your-own-strong-password"`
     `npm install; npm start`
5. Open http://localhost:3000.

## Included
Student username/password registration, bcrypt password hashes, JWT authentication, owner-only stats and question management API, SQLite persistence, question bank, separate Maths/GK/Reasoning/Science and mixed-test settings, result history and official-notice links.

## Important limitations
- Seed data contains only a few illustrative practice questions. The server deliberately refuses to launch a full 100-question test until there are at least 100 active questions for that test/category. Add verified questions through the owner API or a future admin UI before public launch.
- 100 marks / 90 minutes / 1/3 negative marking are practice settings, not a confirmed TTE/TC-specific official pattern.
- Mobile number is stored but NOT OTP-verified. Integrate an SMS provider before advertising phone verification.
- This is starter source code, not a hosted live website. You still need to deploy it to a Node-capable host, configure secrets and HTTPS, set up backups, privacy/terms and monitoring.
- Do not share the owner password. Set it only in your server environment variables; never put it in frontend code.
- Leaderboard usernames are visible to logged-in users. Add privacy controls/consent before public launch.

Official links:
- https://rrb.indianrailways.gov.in/
- https://www.rrbbbs.gov.in/notifications.php
