# 🫀 3D Human Anatomy Explorer

An interactive 3D web application for exploring human organs with realistic models and animations.

## 🌟 Features

### 🎯 **Interactive 3D Models**
- **❤️ Heart** - Realistic heartbeat animation with chambers and vessels
- **🫁 Lungs** - Breathing animation with left and right lung lobes  
- **🫀 Liver** - Subtle pulsing animation with liver tissue

### 🎮 **Controls**
- **Mouse/Touch** - Drag to rotate, scroll to zoom
- **Double-click** - Reset camera view
- **Organ Selector** - Switch between heart, lung, and liver
- **Animation Controls** - Pause, wireframe, labels, auto-rotate

### ✨ **Technical Features**
- **High-resolution 3D models** in GLB format
- **Realistic materials** with subsurface scattering
- **Dynamic lighting** with shadows and reflections
- **Organ-specific animations** (heartbeat, breathing, pulsing)
- **Responsive design** for desktop and mobile

## 🚀 Quick Start

### **Option 1: Local Server (Recommended)**
```bash
# Navigate to project directory
cd your-project-folder

# Start local server
python -m http.server 8000

# Open in browser
http://localhost:8000
```

### **Option 2: Live Server (VS Code)**
1. Install "Live Server" extension in VS Code
2. Right-click on `index.html`
3. Select "Open with Live Server"

### **Option 3: Node.js Server**
```bash
# Install http-server globally
npm install -g http-server

# Start server
http-server -p 8000

# Open in browser
http://localhost:8000
```

## 📁 File Structure

```
3d-anatomy-explorer/
├── index.html          # Main application
├── heart.glb           # Heart 3D model
├── lung.glb            # Lung 3D model  
├── liver.glb           # Liver 3D model
└── README.md           # This file
```

## 🎮 How to Use

### **Navigation**
- **🖱️ Mouse/Touch** - Drag to rotate the organ
- **🔄 Scroll** - Zoom in/out
- **🔄 Double-click** - Reset to default view

### **Organ Selection**
- **🔬 Select Organ** dropdown - Choose between Heart, Lung, or Liver
- **Instant switching** - No page reload required
- **Dynamic UI** - Interface updates for each organ

### **Controls**
- **⏸️ Pause Animation** - Stop/start organ animation
- **🔄 Reset View** - Return to default camera position
- **🔲 Wireframe** - Toggle wireframe/solid view
- **🏷️ Show Labels** - Display anatomical labels
- **🔄 Auto Rotate** - Enable automatic rotation

## 🧬 Organ Details

### **❤️ Heart**
- **Animation**: Heartbeat rhythm (60-100 BPM)
- **Features**: 4 chambers, blood vessels, realistic tissue
- **Materials**: Red-pink cardiac tissue with subsurface scattering

### **🫁 Lungs**  
- **Animation**: Breathing rhythm (12-20 breaths/min)
- **Features**: Left & right lungs, bronchi, pulmonary vessels
- **Materials**: Pink-beige lung tissue with organic texture

### **🫀 Liver**
- **Animation**: Subtle pulsing (liver function)
- **Features**: Liver lobes, hepatic vessels, bile ducts
- **Materials**: Brown liver tissue with realistic surface

## 🛠️ Technical Requirements

- **Modern Browser** - Chrome, Firefox, Safari, Edge
- **WebGL Support** - Required for 3D rendering
- **Local Server** - Required for loading GLB files (CORS policy)
- **Internet Connection** - For Three.js CDN resources

## 🔧 Troubleshooting

### **Model Not Loading**
- Ensure you're using a local server (not opening file directly)
- Check browser console for CORS errors
- Verify GLB files are in the same directory

### **Performance Issues**
- Close other browser tabs
- Reduce browser zoom level
- Disable browser extensions

### **Mobile Issues**
- Use touch gestures for rotation/zoom
- Ensure stable internet connection
- Try landscape orientation

## 📱 Browser Compatibility

- ✅ **Chrome** 80+ (Recommended)
- ✅ **Firefox** 75+
- ✅ **Safari** 13+
- ✅ **Edge** 80+
- ⚠️ **Mobile browsers** - Limited performance

## 🎨 Customization

### **Adding New Organs**
1. Add GLB file to project directory
2. Update `organData` object in JavaScript
3. Add new option to organ selector
4. Create animation function for new organ

### **Modifying Animations**
- Edit `updateOrganAnimation()` function
- Adjust frequency, amplitude, and movement patterns
- Add new animation types for different organs

## 📄 License

This project is open source and available under the MIT License.

## 🤝 Contributing

Contributions are welcome! Please feel free to submit issues and enhancement requests.

---

**🫀 Explore the human body in 3D!** - Interactive anatomy learning made simple.
