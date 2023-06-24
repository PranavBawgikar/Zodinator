<p align="center"><img align="center" src="https://github.com/PranavBawgikar/Zodinator/assets/102728016/9224ce43-c618-439b-b519-a931a3dfa50b" height="110" width="127">
<img align="center" src="https://github.com/PranavBawgikar/Zodinator/assets/102728016/f33f65e8-9003-4898-bbc8-62e9b5231ee4" height="110"></p>
<h1 align="center">Zodinator</h1>

<a href="">Zod</a> is indeed a powerful library for schema validation in TypeScript.

This repo is a User Registration Form implemented using React, TypeScript, and the Zod library for schema validation. It allows users to fill out a registration form with various fields, such as name, email, password, and confirmPassword, and validates the input data based on the defined schema.

## Step-by-Step Guide
Visit the Zod documentation to learn more about the available validation methods and how to define schemas using Zod.<br />
Follow these steps to set up and develop the User Registration Form with Validation project:

1. Set up a new React project:
   - Create a new directory for your project.
   - Initialize a new React project using `npm create vite --template typescript` (provide a name to your local repo when prompted).
   - Change into the project directory: `cd my-app`.
   - Install the necessary dependencies: `npm install zod`.

2. Create a new file, let's say `RegistrationForm.tsx`, and import the required modules:
   ```tsx
   import { useState } from 'react';
   import { z } from 'zod';
   ```

3. Define the schema for user registration using Zod:
   ```tsx
   const registrationSchema = z.object({
     name: z.string().min(2),
     email: z.string().email(),
     password: z.string().min(8),
     confirmPassword: z.string().min(8),
   });
   ```

4. Implement the registration form logic:
   - Create a functional component that represents the registration form.
   - Use React's `useState` hook to manage form input values and validation errors.
   - Handle form submission and validate the input values against the defined schema using `registrationSchema.safeParse()`.

5. Implement the UI and Error Handling:
   - Create the necessary form fields and components using JSX.
   - Add event handlers to capture user input and update the form data state.
   - Display validation errors to the user based on the `validationErrors` state.
   - Customize the error display based on your UI/UX preferences.

6. Style the User Interface:
   - Enhance the user experience by applying CSS styles to the registration form components.
   - Use CSS frameworks or custom styles to create an aesthetically pleasing and responsive user interface.
