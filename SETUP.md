# Setup Guide

This guide will walk you through the setup process for the project, including Firebase, Visual Crossing, TWILIO SendGrid, and Mapbox GL JS. Make sure to follow the steps carefully to configure both the backend and frontend environments.

---

## Firebase Setup

1. Go to [Firebase Console](https://console.firebase.google.com/).
2. **Create a new project** by entering a project name.
3. **Create the project** and go to **Project Settings** → **General Tab**.
4. **Add Firebase to your web app** and register the application.
5. Continue to the console and go back to **Project Settings** → **General Tab**.
6. Scroll down and **copy the `firebaseConfig` object**, save it for later use.
7. Go to **Project Settings** → **Service Accounts Tab**.
8. **Generate a new private key**, this will download a file. This is the `serviceAccount` file, save it for later.
9. Go to **Firestore Database** (under the **Build Tab**).
10. **Create database** in production mode and select the region.
11. Go to **Firestore Database** → **Rules Tab** and replace:
   ```javascript
   allow read, write: if false;
   ```
   with:
   ```javascript
   allow read, write: if true;
   ```
   Click **Publish** (for development purposes only).
12. Go to **Authentication** under the **Build Tab**.
13. Click **Get Started**, then go to **Sign-in Method** Tab.
14. Enable **Email/Password** under **Native Providers**, click **Save**.

---

## Visual Crossing Setup

1. Visual Crossing is used for fetching weather data.
2. Sign up on [Visual Crossing](https://www.visualcrossing.com/).
3. Save your **API Key** for later use.

---

## TWILIO SendGrid Setup

1. TWILIO SendGrid is used for sending emails.
2. Create an account on [SendGrid](https://sendgrid.com/).
3. Save your **API Key** and **verified sender email address**.

---

## Backend Setup

1. Install **Node.js v16.18.0** and **NPM v8.19.2**.
2. Navigate to the **backend's root directory**.
3. Copy the `firebaseConfig` object from Firebase to `./firebaseConfig.js` (from **Firebase Step 6**).
4. Copy the `serviceAccount` file from Firebase to `./serviceAccount.json` (from **Firebase Step 8**).
5. Set your **Visual Crossing API Key** in both `./env` and `./env.ts` files under the variable:
   ```bash
   APIKEY_VISUALCROSSING
   ```
6. Set your **TWILIO SendGrid API Key** in both `./env` and `./env.ts` files under the variable:
   ```bash
   APIKEY_SENDGRID
   ```
7. Set your **TWILIO SendGrid verified sender email address** in both `./env` and `./env.ts` files under the variable:
   ```bash
   SENDGRID_VERIFIEDSENDER
   ```
8. Run the following command in the terminal to install dependencies:
   ```bash
   npm install
   ```
9. Initialize the Cloud Firestore database:
   ```bash
   npm run init
   ```
10. Start the server:
    ```bash
    npm run start
    ```

---

## Mapbox GL JS Setup

1. Mapbox GL JS is used to render the map.
2. Create an account on [Mapbox](https://docs.mapbox.com/).
3. Go to [Mapbox Account](https://account.mapbox.com/).
4. Save your **default public token** (or create a new one).

---

## Frontend Setup

1. Install **Node.js v16.18.0** and **NPM v8.19.2**.
2. Navigate to the **frontend's root directory**.
3. Set your **Mapbox GL JS public token** in `./src/app/AppSettings.ts` under the variable:
   ```bash
   MapboxAccessToken
   ```
4. Install the frontend dependencies:
   ```bash
   npm install
   ```
5. Start the frontend (ensure the backend server is running):
   ```bash
   npm run start
   ```

---

## Final Notes

Make sure that both backend and frontend servers are running properly. For any issues or queries, consult the documentation provided with the project.
