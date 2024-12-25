# Uber_Clone


## Overview
The **Uber Clone App** is a ride-hailing application built using the MERN stack (MongoDB, Express.js, React.js, Node.js). The app replicates the core functionality of Uber, including user authentication, real-time ride booking, map integration, and ride history tracking.

## Features

- **User Authentication**: Sign up and log in using email and password.
- **Real-Time Map Integration**: Integrated Google Maps for live location tracking.
- **Ride Booking**: Book rides by selecting pickup and drop-off locations.
- **Ride History**: View past rides with detailed information.
- **Driver Dashboard**: A separate dashboard for drivers to manage ride requests.
- **Payment Integration**: Simulated payment functionality.

## Tech Stack

- **Frontend**: React.js, Redux (for state management)
- **Backend**: Node.js, Express.js
- **Database**: MongoDB
- **APIs**: Google Maps API, Payment Gateway (e.g., Stripe/PayPal)
- **Authentication**: JWT (JSON Web Token)

## Installation

### Prerequisites
Ensure you have the following installed on your system:
- Node.js (v14 or higher)
- MongoDB (local or cloud-based, e.g., MongoDB Atlas)

### Steps

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/yourusername/uber-clone.git
   cd uber-clone
   ```

2. **Install Dependencies**:
   Navigate to both the `client` and `server` directories to install dependencies:
   ```bash
   cd client
   npm install
   cd ../server
   npm install
   ```

3. **Set Up Environment Variables**:
   Create a `.env` file in the `server` directory with the following keys:
   ```env
   PORT=5000
   MONGO_URI=your-mongodb-connection-string
   JWT_SECRET=your-jwt-secret
   GOOGLE_MAPS_API_KEY=your-google-maps-api-key
   PAYMENT_GATEWAY_KEY=your-payment-gateway-key
   ```

4. **Run the Application**:
   - Start the backend server:
     ```bash
     cd server
     npm start
     ```
   - Start the frontend client:
     ```bash
     cd client
     npm start
     ```

5. **Access the App**:
   Open your browser and navigate to `http://localhost:3000`.

## Folder Structure

```
uber-clone/
│
├── client/                # Frontend code
│   ├── public/            # Static files
│   ├── src/               # React app source code
│   │   ├── components/    # Reusable components
│   │   ├── pages/         # Pages for the app
│   │   ├── redux/         # Redux setup
│   │   └── App.js         # Root component
│
├── server/                # Backend code
│   ├── models/            # MongoDB models
│   ├── routes/            # API routes
│   ├── controllers/       # Route handlers
│   └── server.js          # Entry point
│
└── README.md              # Documentation
```

## API Endpoints

### User Authentication
- **POST /api/auth/register**: Register a new user
- **POST /api/auth/login**: Log in an existing user

### Ride Management
- **POST /api/rides/book**: Book a ride
- **GET /api/rides/history**: Fetch ride history

### Driver Management
- **GET /api/drivers/requests**: Fetch ride requests
- **POST /api/drivers/accept**: Accept a ride request

## Contributing
Contributions are welcome! Please follow these steps:
1. Fork the repository.
2. Create a new branch (`feature/your-feature-name`).
3. Commit your changes.
4. Push to the branch.
5. Submit a pull request.

## License
This project is licensed under the [MIT License](LICENSE).

## Acknowledgements
- Google Maps API for location services.
- Open-source libraries and tools that made this project possible.
