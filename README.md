# Adopt a Pet - Pet Adoption Website

## Project Description

Adopt a Pet is a pet adoption website built using React and React Router. The website allows users to view all adoptable pets, filter pets by species, view detailed profiles of individual pets, search for pets by name, and handle scenarios where pet details are unavailable.

## Features

- **Home Page**: Displays all adoptable pets with the ability to filter by species (dogs, cats, rabbits, birds).
- **Pet Details Page**: Displays detailed information about a specific pet based on the pet ID in the URL.
- **Search Page**: Allows users to search for pets by name using a query parameter.
- **Pet Not Found Page**: Redirects users to this page if the pet details are unavailable.
- **Navigation Bar**: Allows users to navigate between different species and search for pets.

## Setup Instructions

1. **Clone the repository**:
   ```bash
   git clone https://github.com/your-username/Adopt_a_pet.git
   cd Adopt_a_pet
   ```

2. **Install dependencies**:
   ```bash
   npm install
   ```

3. **Start the application**:
   ```bash
   npm start
   ```

4. **Open the application in your browser**:
   Navigate to `http://localhost:3000`


## Implementation Details

### Routing Setup

1. **Installed React Router**:
   ```bash
   npm install --save react-router-dom@6
   ```

2. **Provided React Router at the root level** in `src/App.js`:
   - Imported `RouterProvider` and used it to wrap the application routes.

3. **Created the initial route**:
   - Defined the `appRouter` constant with a route to the `Root` component.

4. **Nested Routes and Index Route**:
   - Added a nested route for `HomePage` in the `Root` route.

5. **Dynamic Paths and URL Parameters**:
   - Created dynamic routes for filtering pets by species and viewing pet details.

6. **Implemented Search Feature**:
   - Added a search bar to update the URL with query parameters and render the `SearchPage`.

7. **Pet Details Not Found Handling**:
   - Redirected to `PetDetailsNotFound` page if the pet details are unavailable and added a button to navigate back to the home page.

### Component Updates

1. **Navigation Component**:
   - Replaced `<a>` tags with `NavLink` for client-side navigation.
   - Added visual indication for the active link.

2. **HomePage Component**:
   - Used `Link` component for pet details links to prevent page reloads.

3. **PetDetailsPage Component**:
   - Used `useParams` hook to fetch pet details based on URL parameters.
   - Redirected to `PetDetailsNotFound` page if pet details are not found.

4. **SearchPage Component**:
   - Used `useSearchParams` hook to filter pets by name based on query parameters.

## Usage

- Navigate through different species using the navigation bar.
- Click on a pet to view its detailed profile.
- Use the search bar to find pets by name.
- If a pet's details are unavailable, you will be redirected to a not found page with an option to return to the home page.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Acknowledgements

- The project uses Mock Service Worker (MSW) to simulate API responses.
- Developed as part of a learning exercise on Codecademy.
