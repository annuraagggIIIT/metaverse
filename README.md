# Save this script as setup.sh

# Clone the repository
git clone https://github.com/your-username/nestjs-contacts-app.git

# Navigate to the project directory
cd nestjs-contacts-app

# Install dependencies
npm install

# Create a .env file
echo "MONGO_URI=your_mongo_db_uri" > .env
echo "REDIS_HOST=your_redis_host" >> .env
echo "REDIS_PORT=your_redis_port" >> .env

# Start MongoDB and Redis servers (assumes they are installed and configured)
# You may need to adjust these commands based on your specific setup
# For example, you might use different commands to start MongoDB and Redis
# Or you might have them set up as services that start automatically

# Start MongoDB (replace with your actual MongoDB start command)
mongod --dbpath=./data &

# Start Redis (replace with your actual Redis start command)
redis-server &

# Run the NestJS application
npm run start
