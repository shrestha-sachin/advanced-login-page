# Advanced Login Page

A modern and beautiful login page built with React, Tailwind CSS, and Firebase Authentication with **real** social login support!

## Features

- ✨ Modern and responsive design
- 🔐 Real authentication with Firebase
- 📧 Email/Password registration and login
- � Social authentication with:
  - Google
  - Facebook
  - GitHub
- �🎨 Beautiful gradient backgrounds with animated floating elements
- � Toggle between Login and Sign Up forms
- 👁️ Show/Hide password functionality
- � Password reset functionality
- �📱 Fully responsive (mobile, tablet, desktop)
- ✅ Form validation
- 💫 Smooth animations and transitions
- 🎯 Protected dashboard after login
- 🚪 Logout functionality

## Getting Started

### Prerequisites

- Node.js installed
- Firebase account (free tier works!)

### Installation

1. **Install Dependencies**

```bash
npm install
```

2. **Set Up Firebase**

Follow the detailed instructions in [FIREBASE_SETUP.md](./FIREBASE_SETUP.md) to:
- Create a Firebase project
- Enable authentication methods (Email, Google, Facebook, GitHub)
- Get your Firebase configuration
- Update `src/firebase/config.js` with your credentials

### Run Development Server

```bash
npm run dev
```

Open [http://localhost:5173](http://localhost:5173) in your browser.

### Build for Production

```bash
npm run build
```

### Preview Production Build

```bash
npm run preview
```

## Project Structure

```
/login
├── src/
│   ├── components/
│   │   ├── LoginPage.jsx      # Login/Signup form
│   │   └── Dashboard.jsx      # Protected dashboard
│   ├── context/
│   │   └── AuthContext.jsx    # Authentication context
│   ├── firebase/
│   │   ├── config.js          # Firebase configuration
│   │   └── auth.js            # Authentication functions
│   ├── App.jsx
│   ├── main.jsx
│   └── index.css
├── FIREBASE_SETUP.md           # Detailed Firebase setup guide
├── tailwind.config.js
├── vite.config.js
└── package.json
```

## How It Works

### Authentication Flow

1. **Email/Password**: Users can sign up with email and password or log in
2. **Social Login**: Users click a provider button (Google/Facebook/GitHub)
3. **Firebase handles the OAuth flow** with a popup
4. **User is authenticated** and redirected to dashboard
5. **Protected routes** check authentication state
6. **Logout** clears the session

### Key Components

- **LoginPage**: Handles all authentication forms and social login buttons
- **Dashboard**: Shows user info after successful login
- **AuthContext**: Manages authentication state across the app
- **Firebase Auth Functions**: Wrapper functions for Firebase authentication

## Authentication Methods

### Email/Password
- Sign up with email and password
- Login with existing credentials
- Password reset via email

### Google
- One-click authentication
- Automatic account creation
- Profile photo and name imported

### Facebook
- Seamless Facebook integration
- Access to basic profile info
- Requires Facebook Developer app setup

### GitHub
- Developer-friendly authentication
- Access to GitHub profile
- Requires GitHub OAuth app setup

## Customization

### Colors
Modify colors in `tailwind.config.js` to match your brand.

### Animations
Custom animations are defined in `tailwind.config.js` under `keyframes`.

### Firebase Rules
Set up Firestore security rules for additional data storage.

## Security Notes

⚠️ **Important:**
- Never commit your Firebase config with real credentials to public repos
- Use environment variables for production
- Enable Firebase App Check for additional security
- Set up proper security rules in Firebase Console

## Technologies Used

- React 18
- Vite
- Tailwind CSS
- Firebase Authentication
- PostCSS
- Autoprefixer

## Troubleshooting

### Authentication not working?
- Check Firebase Console for errors
- Verify authentication methods are enabled
- Check browser console for error messages
- See [FIREBASE_SETUP.md](./FIREBASE_SETUP.md) for common issues

### Social login popup blocked?
- Allow popups in your browser
- Check Firebase authorized domains

### "Unauthorized domain" error?
- Add your domain to Firebase authorized domains
- For localhost, add `localhost` and `127.0.0.1`

## Next Steps

Consider adding:
- Email verification
- User profiles in Firestore
- Two-factor authentication
- OAuth for more providers (Twitter, Microsoft, Apple)
- Session persistence options
- Custom claims and user roles

## License

MIT

## Support

For Firebase setup help, see [FIREBASE_SETUP.md](./FIREBASE_SETUP.md)

For Firebase docs, visit [Firebase Authentication Documentation](https://firebase.google.com/docs/auth)

