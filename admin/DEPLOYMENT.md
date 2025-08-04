# Admin App Deployment Guide for Render

## Changes Made for Deployment

### 1. Environment Variables
- Created `.env` file with backend URL:
  ```
  VITE_BACKEND_URL=https://food-delivery-app-backend-sixo.onrender.com
  ```

### 2. Updated assets.js
- Changed hardcoded localhost URL to use environment variable:
  ```js
  export const url = import.meta.env.VITE_BACKEND_URL || 'http://localhost:4000'
  ```

### 3. Updated App.jsx
- Changed hardcoded localhost URL to use environment variable:
  ```jsx
  const url = import.meta.env.VITE_BACKEND_URL || 'http://localhost:4000';
  ```

## Deploy to Render

### Step 1: Push to GitHub
```bash
git add .
git commit -m "Updated admin app for deployment"
git push origin main
```

### Step 2: Create Render Static Site
1. Go to [Render Dashboard](https://dashboard.render.com/)
2. Click "New +" → "Static Site"
3. Connect your GitHub repository
4. Configure:
   - **Name:** food-delivery-admin (or any name)
   - **Root Directory:** admin
   - **Build Command:** `npm install && npm run build`
   - **Publish Directory:** `dist`
   - **Environment Variables:**
     - `VITE_BACKEND_URL`: `https://food-delivery-app-backend-sixo.onrender.com`

### Step 3: Deploy
- Click "Create Static Site"
- Render will build and deploy your admin app
- You'll get a URL like: `https://your-admin.onrender.com`

## Important Notes

- The admin app will now use your deployed backend URL
- Local development will still work with the fallback localhost URL
- Make sure your backend is deployed and working before deploying admin
- The environment variable will be used in production, localhost fallback for development

## Admin Features
After deployment, you can:
1. Add new food items
2. View and manage food list
3. View and update order status
4. Upload food images

## Testing
After deployment, test:
1. Adding new food items
2. Uploading images
3. Viewing food list
4. Managing orders
5. Updating order status 