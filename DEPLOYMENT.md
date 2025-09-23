# 🚀 Vercel Deployment Guide

Complete guide for deploying your 3D Human Anatomy Explorer to Vercel.

## 📋 Prerequisites

- [ ] GitHub account
- [ ] Vercel account (free)
- [ ] Your project files ready
- [ ] GLB model files (heart.glb, lung.glb, liver.glb)

## 🎯 Quick Deployment (5 minutes)

### **Step 1: Prepare Your Repository**
```bash
# Initialize git repository (if not already done)
git init

# Add all files
git add .

# Commit your changes
git commit -m "Initial commit: 3D Human Anatomy Explorer"

# Create GitHub repository and push
git remote add origin https://github.com/yourusername/3d-human-anatomy-explorer.git
git branch -M main
git push -u origin main
```

### **Step 2: Deploy to Vercel**

#### **Option A: GitHub Integration (Recommended)**
1. Go to [vercel.com](https://vercel.com)
2. Click "New Project"
3. Import your GitHub repository
4. Vercel will auto-detect it's a static site
5. Click "Deploy"
6. Your app will be live in ~2 minutes!

#### **Option B: Vercel CLI**
```bash
# Install Vercel CLI
npm install -g vercel

# Login to Vercel
vercel login

# Deploy from your project directory
vercel

# Follow the prompts:
# - Set up and deploy? Y
# - Which scope? (your account)
# - Link to existing project? N
# - Project name? 3d-human-anatomy-explorer
# - Directory? ./
# - Override settings? N
```

## 🔧 Configuration Files

### **vercel.json** ✅
```json
{
  "version": 2,
  "name": "3d-human-anatomy-explorer",
  "builds": [
    {
      "src": "index.html",
      "use": "@vercel/static"
    }
  ],
  "routes": [
    {
      "src": "/(.*)",
      "dest": "/index.html"
    }
  ]
}
```

### **package.json** ✅
```json
{
  "name": "3d-human-anatomy-explorer",
  "version": "1.0.0",
  "description": "Interactive 3D Human Anatomy Explorer",
  "main": "index.html",
  "scripts": {
    "dev": "python -m http.server 8000",
    "build": "echo 'No build step required'",
    "deploy": "vercel --prod"
  }
}
```

## 🌐 Post-Deployment

### **Your App is Live!**
- **URL**: `https://your-project-name.vercel.app`
- **Custom Domain**: Available in Vercel dashboard
- **HTTPS**: Automatically enabled
- **CDN**: Global content delivery

### **Automatic Deployments**
- Every push to `main` branch = automatic deployment
- Preview deployments for pull requests
- Instant rollbacks available

## 🎨 Customization

### **Custom Domain**
1. Go to Vercel Dashboard → Your Project
2. Settings → Domains
3. Add your domain (e.g., `anatomy.yourdomain.com`)
4. Update DNS records as instructed

### **Environment Variables**
```bash
# No environment variables needed for this static site
# But you can add them in Vercel dashboard if needed
```

### **Build Settings**
- **Framework Preset**: Other
- **Build Command**: (leave empty)
- **Output Directory**: (leave empty)
- **Install Command**: (leave empty)

## 🔍 Troubleshooting

### **Common Issues**

#### **GLB Files Not Loading**
- ✅ Ensure GLB files are in root directory
- ✅ Check file names match exactly: `heart.glb`, `lung.glb`, `liver.glb`
- ✅ Verify file sizes are reasonable (< 50MB each)

#### **Sketchfab Not Loading**
- ✅ Check Content Security Policy in `index.html`
- ✅ Ensure `https://sketchfab.com` is allowed in CSP
- ✅ Test in different browsers

#### **Performance Issues**
- ✅ Enable Vercel's Edge Functions
- ✅ Optimize GLB file sizes
- ✅ Use Vercel's Analytics for monitoring

### **Debug Steps**
1. Check Vercel deployment logs
2. Test locally with `python -m http.server 8000`
3. Verify all files are committed to git
4. Check browser console for errors

## 📊 Performance Optimization

### **Vercel Features**
- ✅ **Edge Network**: Global CDN
- ✅ **Automatic HTTPS**: SSL certificates
- ✅ **Compression**: Gzip/Brotli compression
- ✅ **Caching**: Smart caching headers

### **GLB Optimization**
```bash
# Optimize GLB files (optional)
# Use tools like gltf-pipeline for compression
npx gltf-pipeline -i heart.glb -o heart-optimized.glb --draco
```

## 🚀 Advanced Features

### **Preview Deployments**
- Every branch gets a preview URL
- Perfect for testing before merging
- Share preview links with team

### **Analytics**
- Enable Vercel Analytics in dashboard
- Monitor performance and usage
- Track Core Web Vitals

### **Edge Functions**
```javascript
// api/hello.js - Example edge function
export default function handler(req, res) {
  res.json({ message: 'Hello from Vercel!' })
}
```

## 📱 Mobile Optimization

### **Responsive Design**
- ✅ Touch controls for mobile
- ✅ Optimized viewport settings
- ✅ Mobile-friendly UI controls

### **Performance**
- ✅ Lazy loading for 3D models
- ✅ Optimized textures
- ✅ Efficient animations

## 🔒 Security

### **Content Security Policy**
```html
<meta http-equiv="Content-Security-Policy" 
      content="default-src 'self' 'unsafe-inline' 'unsafe-eval' 
               https://cdn.jsdelivr.net https://sketchfab.com blob:; 
               script-src 'self' 'unsafe-inline' 'unsafe-eval' 
               https://cdn.jsdelivr.net; 
               connect-src 'self' https://cdn.jsdelivr.net 
               https://sketchfab.com blob:; 
               frame-src 'self' https://sketchfab.com;" />
```

### **Headers**
- ✅ X-Content-Type-Options: nosniff
- ✅ X-Frame-Options: DENY
- ✅ X-XSS-Protection: 1; mode=block

## 📈 Monitoring

### **Vercel Dashboard**
- Deployment status
- Performance metrics
- Error tracking
- Usage analytics

### **Custom Monitoring**
```javascript
// Add to your HTML for custom analytics
<script>
  // Track organ selections
  function trackOrganSelection(organ) {
    // Your analytics code here
  }
</script>
```

## 🎉 Success!

Your 3D Human Anatomy Explorer is now live on Vercel! 

**Next Steps:**
1. ✅ Share your live URL
2. ✅ Test all organ models
3. ✅ Verify Sketchfab integration
4. ✅ Set up custom domain (optional)
5. ✅ Monitor performance

---

**🫀 Your interactive anatomy learning platform is ready for the world!**
