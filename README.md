This is an Inventory app were Our app will enable users to add items to their inventory, monitor quantities, and remove items when they’re sold or used. 
We’ll leverage Next.js as our React framework, Material-UI for creating a sleek and responsive user interface, and Firebase Firestore as our backend database. 
This powerful combination of technologies will allow us to develop a real-time web application that’s both scalable and user-friendly.

Creating a Next.js project:
Open your terminal and navigate to the directory where you want to create your project. Then, run the following commands:

npx create-next-app inventory-management-app
cd inventory-management-app
This will create a new Next.js project and navigate into its directory. During the setup, you’ll be prompted with several configuration options. For this tutorial, you can select the following:

— Would you like to use TypeScript? No
— Would you like to use ESLint? Yes
— Would you like to use Tailwind CSS? No
— Would you like to use `src/` directory? No
— Would you like to use App Router? Yes
— Would you like to customize the default import alias? No

3. Installing additional dependencies:
We’ll need to install Material-UI and Firebase. Run the following command in your project directory:

npm install @mui/material @emotion/react @emotion/styled firebase
4. Setting up Firebase:
— Go to the Firebase Console and create a new project.
— Once your project is created, click on “Add app” and select the web platform (</>).
— Register your app with a nickname (e.g., “Inventory Management App”).
— Copy the Firebase configuration object. We’ll use this in the next step.

5. Creating a Firebase configuration file:
Create a new file in your project’s root directory called `firebase.js` and add the following code, replacing the placeholder values with your actual Firebase configuration:

import { initializeApp } from 'firebase/app';
import { getFirestore } from 'firebase/firestore';
const firebaseConfig = {
 apiKey: "YOUR_API_KEY",
 authDomain: "YOUR_PROJECT_ID.firebaseapp.com",
 projectId: "YOUR_PROJECT_ID",
 storageBucket: "YOUR_PROJECT_ID.appspot.com",
 messagingSenderId: "YOUR_MESSAGING_SENDER_ID",
 appId: "YOUR_APP_ID"
 };
const app = initializeApp(firebaseConfig);
const firestore = getFirestore(app);
export { firestore };
With these steps completed, we’ve successfully set up our development environment and project structure. 

