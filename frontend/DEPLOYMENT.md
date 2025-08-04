# Frontend Deployment Guide for Render

## Changes Made for Deployment

### 1. Environment Variables
- Created `.env` file with backend URL:
  ```
  VITE_BACKEND_URL=https://food-delivery-app-backend-sixo.onrender.com
  ```

### 2. Updated StoreContext.jsx
- Changed hardcoded localhost URL to use environment variable:
  ```jsx
  const url = import.meta.env.VITE_BACKEND_URL || "http://localhost:4000";
  ```

### 3. Updated vite.config.js
- Removed proxy configuration since we're using environment variables

## Deploy to Render

### Step 1: Push to GitHub
```bash
git add .
git commit -m "Updated frontend for deployment"
git push origin main
```

### Step 2: Create Render Web Service
1. Go to [Render Dashboard](https://dashboard.render.com/)
2. Click "New +" → "Static Site"
3. Connect your GitHub repository
4. Configure:
   - **Name:** food-delivery-frontend (or any name)
   - **Root Directory:** frontend
   - **Build Command:** `npm install && npm run build`
   - **Publish Directory:** `dist`
   - **Environment Variables:**
     - `VITE_BACKEND_URL`: `https://food-delivery-app-backend-sixo.onrender.com`

### Step 3: Deploy
- Click "Create Static Site"
- Render will build and deploy your frontend
- You'll get a URL like: `https://your-frontend.onrender.com`

## Important Notes

- The frontend will now use your deployed backend URL
- Local development will still work with the fallback localhost URL
- Make sure your backend is deployed and working before deploying frontend
- The environment variable will be used in production, localhost fallback for development

## Testing
After deployment, test:
1. User registration/login
2. Browsing food items
3. Adding items to cart
4. Placing orders
5. Payment integration 