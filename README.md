# ShoreAgents Schedulers

This repository contains only the scheduler services for ShoreAgents, designed to run on Railway.

## 🚀 Schedulers Included

- **break-reminder-scheduler** - Sends break notifications every 30 seconds
- **task-notification-scheduler** - Handles task notifications every 5 minutes
- **meeting-scheduler** - Manages meeting notifications
- **event-reminder-scheduler** - Handles event reminders
- **announcement-scheduler** - Manages announcements

## 🐳 Deployment

This repository is configured to deploy directly to Railway using the included Dockerfile.

### Railway Deployment

1. **Connect this repository to Railway**
2. **Railway will automatically detect the Dockerfile**
3. **Set environment variables**:
   - `DATABASE_URL` - Your PostgreSQL connection string
   - `NODE_ENV=production`
4. **Deploy** - Railway will build and run all schedulers

## 📁 Files

- `Dockerfile` - Docker configuration for Railway
- `package.json` - Dependencies for schedulers
- `ecosystem.railway.schedulers.config.js` - PM2 configuration
- `scripts/` - Scheduler scripts
- `railway.json` - Railway configuration

## 🔧 Environment Variables

Required environment variables:
- `DATABASE_URL` - PostgreSQL connection string
- `NODE_ENV=production`

Optional environment variables:
- `REDIS_URL` - Redis connection string (if using Redis)

## 📊 Monitoring

After deployment, you can monitor the schedulers through Railway dashboard:
- View logs in real-time
- Monitor CPU/Memory usage
- Check scheduler status
- Restart individual schedulers

## 🎯 Usage

Once deployed, the schedulers will run automatically 24/7 on Railway, handling all notification tasks for the ShoreAgents application.
