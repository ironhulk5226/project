# ShareBox

ShareBox is a React application for authenticated image uploads and expiring
share links.

## Technology

- React and Vite
- Firebase Authentication
- Cloud Firestore for user, file, and share-link metadata
- Cloudinary for JPG, JPEG, and PNG media

There is no custom Node.js server or Firebase Storage dependency. The browser
communicates with Firebase and Cloudinary directly.

## Run locally

From PowerShell:

```powershell
cd "D:\Final Year\sem VII\LAB\CC lab\project\sharebox\client"
npm install
npm run dev
```

Open the URL printed by Vite, normally `http://localhost:5173`.

To create a production build:

```powershell
npm run build
```

To preview that build:

```powershell
npm run preview
```

## Upload restrictions

- Supported formats: `.jpg`, `.jpeg`, and `.png`
- Maximum file size: 10 MB
- PDF and other file types are rejected

## Firebase setup

The Firebase project configuration is in
`client/src/services/firebase.js`. Publish the rules in `firestore.rules` to
Cloud Firestore before using a new Firebase project.

## Cloudinary setup

The upload configuration is in `client/src/services/cloudinary.js`. The
unsigned upload preset must allow image uploads and use the folder configured
there.
