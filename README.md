# Project Build and Start Scripts

This document explains how to use the provided npm scripts to build and start the project in different environments. These scripts ensure that the appropriate environment variables are loaded from specific `.env` files.

## Prerequisites

- **Node.js** and **npm** installed on your system.
- **cross-env** and **dotenv** packages are used to manage environment variables.
- `.env` files for each environment: `.env.local`, `.env.development`, `.env.uat`, `.env.production`.

## Scripts Overview

### 1. **Starting the Project**

You can start the project in different environments using the following commands:

- **Local Environment:**  
  ```bash
  npm run start:local
  ```
  Loads environment variables from `.env.local`.

- **Development Environment:**  
  ```bash
  npm run start:development
  ```
  Loads environment variables from `.env.development`.

- **UAT (User Acceptance Testing) Environment:**  
  ```bash
  npm run start:uat
  ```
  Loads environment variables from `.env.uat`.

- **Production Environment:**  
  ```bash
  npm run start:production
  ```
  Loads environment variables from `.env.production`.

### 2. **Building the Project**

To create an optimized production build for different environments:

- **Local Build:**  
  ```bash
  npm run build:local
  ```
  Uses `.env.local` for environment variables.

- **Development Build:**  
  ```bash
  npm run build:development
  ```
  Uses `.env.development` for environment variables.

- **UAT Build:**  
  ```bash
  npm run build:uat
  ```
  Uses `.env.uat` for environment variables.

- **Production Build:**  
  ```bash
  npm run build:production
  ```
  Uses `.env.production` for environment variables.

### 3. **Running Tests**

To run the tests:

```bash
npm run test
```

### 4. **Ejecting the Project**

To eject the project and have full control over the configuration:

```bash
npm run eject
```

> ⚠️ **Caution:** This action is irreversible.

## How It Works

- **cross-env:** Ensures environment variables work correctly across different operating systems.
- **dotenv:** Loads environment variables from the specified `.env` file.
- **react-scripts:** Handles starting, building, testing, and ejecting the React app.

### Example of `.env` File:

```env
REACT_APP_API_URL=https://api.example.com
REACT_APP_ENV=development
```

Make sure to create and maintain the respective `.env` files for each environment to ensure the correct configuration is loaded.

## Troubleshooting

1. **Missing `.env` File:** Ensure the required `.env` file exists in the root directory.
2. **Dependencies Issue:** Run `npm install` if you encounter missing packages.
3. **Cross-Environment Issues:** Ensure `cross-env` and `dotenv` are correctly installed:
   ```bash
   npm install cross-env dotenv
   ```

## Conclusion

This setup ensures that the app runs smoothly in various environments with minimal configuration changes. Future developers should update the `.env` files and scripts as needed to reflect any new environments or changes.

