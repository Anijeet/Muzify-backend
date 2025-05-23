# Muzify Backend

## Setup Instructions

Follow these steps to set up the backend for Muzify.

### Step 1: Clone the Frontend Repository
First, clone the frontend repository:
```sh
git clone https://github.com/Fahad-Dezloper/Muzify
```

### Step 2: Fork and Clone the Backend Repository
Fork the repository and then clone it to your local machine:
```sh
git clone https://github.com/anijeet/muzify-backend
```

### Step 3: Update Redis Configuration
Navigate to `index.ts` and modify the Redis configuration as follows:

1. Uncomment the following lines:
```ts
const redisClient = createClient({
    socket: {
        host: "localhost",
        port: 6379,
    },
});
```
2. Comment out the existing Railway Redis configuration:
```ts
// Redis configuration for Railway
// const redisClient = createClient({
//   url: process.env.REDIS_URL || "redis://localhost:6379"
// });
```

### Step 4: Run Redis in Docker
Run the following command to start a Redis container using Docker:
```sh
docker run --name redis-container -p 6379:6379 -d redis
```

### Step 5: Run PNPM
Run the following commands to start the backend:
```sh
pnpm install
```
```sh
pnpm run dev
```

Now, your backend should be properly configured and ready to run!
#   M u z i f y - b a c k e n d  
 