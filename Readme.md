# EstateFinder – Real Estate Listing Platform

EstateFinder is a real estate listing and discovery platform where builders and property owners can showcase flats, villas, and plots for sale, rent, or lease. Users can explore listings, view property details, upload their own listings, and interact with individual properties through dedicated comments and reviews.

## Key Features

- **Property Listings:** Create and manage property listings with images, descriptions, pricing, and location details.
- **Property Discovery:** Browse available properties and explore their details.
- **Image Management:** Upload and store property images using Cloudinary.
- **Location Services:** Integrate Mapbox geocoding to convert property addresses into geographic coordinates.
- **User Accounts:** Support user registration, authentication, and account-related pages.
- **Property-Specific Reviews:** Allow users to post reviews and interact with individual property listings.
- **Review Management:** Associate reviews with their respective properties and manage related reviews when listings are removed.
- **Error Handling:** Centralized error handling and asynchronous request management through reusable middleware.

## Architecture

EstateFinder follows an **MVC (Model-View-Controller) architecture** with a modular Express.js application structure.

### 1. Application Layer
- `app.js` – Main Express application entry point.
- Registers application routes and middleware.
- Handles incoming visitor requests.

### 2. Routing and Middleware Layer
- `listing.js` – Handles property listing routes.
- `user.js` – Handles user-related routes.
- `review.js` – Handles property review routes.
- `middleware.js` – Manages authentication and request validation.
- `wrapAsync.js` – Provides reusable asynchronous error handling.
- `error.ejs` – Renders application error pages.

### 3. Controllers and Services
- `listings.js` – Handles property listing operations and listing-related logic.
- `users.js` – Manages user account operations.
- `reviews.js` – Handles property-specific review operations.
- `cloudConfig.js` – Configures Cloudinary for property image storage.
- `map.js` – Handles map-related client functionality.
- Mapbox Geocoding – Processes property location data.

### 4. Data Models
- `Listing` – Stores property information and listing details.
- `User` – Manages user account data.
- `Review` – Stores reviews associated with individual property listings.
- MongoDB – Provides persistent data storage.

## Technology Stack

| Category | Technologies |
|---|---|
| Backend | Node.js, Express.js |
| Frontend | EJS, JavaScript, HTML, CSS |
| Database | MongoDB |
| Authentication | Passport.js |
| Image Storage | Cloudinary |
| Maps & Geocoding | Mapbox |
| Architecture | MVC |

## Project Highlights

- Modular backend architecture with separated routes, controllers, and models.
- Property-specific user interactions through an associated review system.
- Third-party integrations for cloud image storage and location geocoding.
- Reusable middleware for authentication, validation, and error handling.
- Structured MongoDB relationships between users, listings, and reviews.
## System Architecture

The following diagram illustrates EstateFinder's application structure, request flow, MVC components, middleware, and database interactions.

![EstateFinder System Architecture](Temp_images/architecture.png)