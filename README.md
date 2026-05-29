# Sports Roster Manager 🎾

A simple event roster management system built with Firebase. Create sports events and manage team rosters with WhatsApp notification support.

## Features

### For Event Creators
- 🔐 Simple password authentication
- 📅 Set event date and time period
- 🏸 Add single or multiple courts
- 👥 Configure player capacity (4, 6, 8, 10, 12, or 16 players)
- 🔗 Generate shareable event links
- 📱 Share directly to WhatsApp

### For Players (Roster Candidates)
- 🔐 Team password authentication (shared in advance)
- ✋ Add your name to the roster
- ✏️ Edit your name if needed
- 🗑️ Remove yourself from the roster
- 📱 Share current roster status to WhatsApp

## Configuration

Edit the passwords in `public/index.html`:

```javascript
const CONFIG = {
  CREATOR_PASSWORD: 'a*******',     // Password for event creators
  USER_PASSWORD: 't**********',        // Password shared with team members
};
```

## Setup

1. Make sure you have Firebase CLI installed:
   ```bash
   npm install -g firebase-tools
   ```

2. Login to Firebase:
   ```bash
   firebase login
   ```

3. Enable Firestore in your Firebase project (Firebase Console → Firestore Database → Create Database)

4. Deploy to Firebase:
   ```bash
   firebase deploy
   ```

## Local Development

Run the Firebase emulator:
```bash
firebase emulators:start
```

Then open http://localhost:5000 in your browser.

## Usage

### Creating an Event
1. Click "Create New Event"
2. Enter the creator password
3. Fill in the event details:
   - Select date
   - Set time period (from - to)
   - Add court names
   - Choose max number of players
4. Click "Create Event"
5. Share the generated link with your team

### Joining an Event
1. Open the shared event link OR click "Join Event as Player"
2. Enter the event ID (if not from link) and team password
3. Add your name to the roster
4. Use edit/delete buttons to modify your entry

### WhatsApp Notifications
- After creating an event, click "Share to WhatsApp" to send event details
- On the roster page, click "Share Roster to WhatsApp" to share current roster status

## Tech Stack
- Firebase Hosting
- Firebase Firestore (real-time database)
- Vanilla JavaScript (no frameworks)
- Mobile-responsive CSS
