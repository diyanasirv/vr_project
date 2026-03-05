# RAKSHA - Fire Safety Training Simulation

> **RAKSHA for Suraksha** (Protection for Safety)

A 3D fire safety training simulation built with **Three.js** to educate users on identifying fire hazards and responding appropriately in emergency situations. The application provides an interactive first-person experience with VR support for enhanced immersion.


## 🎯 Overview

RAKSHA is an educational simulation that guides users through a fire safety scenario. Players must:
1. **Identify the hazard** - Locate the fire source in the room
2. **Respond appropriately** - Use available safety equipment
3. **Extinguish the fire** - Apply the fire extinguisher
4. **Evacuate safely** - Reach the designated safe zone

The application uses WebGL 3D graphics to create a realistic indoor environment with interactive objects, dynamic lighting, and particle effects.

---

## ✨ Features

### Core Gameplay
- **First-Person Perspective**: Navigate the 3D environment from a first-person viewpoint
- **Interactive Objects**: 
  - Fire source (burning barrel)
  - Fire alarm box on the wall
  - Fire extinguisher
  - Safe evacuation zone
- **Step-Based Progression**: Multi-step objectives guide the player through the safety procedure
- **Progress Tracking**: Visual progress bar for each objective

### Graphics & Visuals
- **3D Environment**: Detailed room with walls, ceiling, floor, and pillars
- **Advanced Lighting**:
  - Ambient room lighting
  - Emergency red alarm lights (triggered on fire detection)
  - Dynamic fire light with flickering effect
  - Exit sign illumination
- **Particle Systems**:
  - Fire particle effects
  - Smoke simulation
- **Shadow Rendering**: Realistic shadow mapping with PCF soft shadows
- **Canvas-based Labels**: Text labels for interactive objects

### Controls
- **Mouse Look**: Free mouse movement to look around (Pointer Lock)
- **WASD Movement**: W (Forward), A (Left), S (Backward), D (Right)
- **Interaction**: Left click to interact with nearby objects
- **Pause**: ESC key to pause the simulation
- **VR Support**: Enter VR button for immersive headset experiences (WebXR)

### Audio
- Fire alarm sound loop when hazard is detected
- Fire extinguisher spray sound effect

---

## 🎮 How to Use

### Quick Start
1. Open `vr.html` in a modern web browser
2. Click "Start Simulation" button
3. Allow pointer lock when prompted (click to lock mouse)
4. Follow the on-screen instructions

### Gameplay Flow
1. **Step 1**: Identify and inspect the fire source
   - Look around and locate the burning barrel
   - Get close to inspect it
   
2. **Step 2** (Implied): Locate and acquire the fire alarm
   - Find the red alarm box on the right wall
   - Interact with it

3. **Step 3** (Implied): Find and use the fire extinguisher
   - Locate the red extinguisher on the left wall
   - Pick it up and apply it to the fire

4. **Step 4** (Implied): Evacuate to safety
   - Move to the green-marked safe zone
   - Complete the simulation

---

## 🛠️ Technical Details

### Technology Stack
- **Rendering Engine**: Three.js r128
- **3D Graphics**: WebGL
- **Controls Library**: PointerLockControls (Three.js)
- **Physics**: Basic collision detection via raycasting
- **Audio**: HTML5 Audio API
- **VR Support**: WebXR API (if available)

### Browser Requirements
- Modern browser with WebGL support
- JavaScript enabled
- For VR: Compatible VR headset and WebXR-enabled browser (Mozilla Firefox, Chrome with flag, etc.)

### Project Structure
```
vr_project/
├── index.html          # Main application file
├── README.md        # This file
└── vr_project/      # Subdirectory (for future expansion)
```

---

## 🔧 Development Notes

### Key Game Objects
- `camera`: First-person perspective (eye level at 1.6 units)
- `scene`: Main 3D environment
- `renderer`: WebGL renderer with shadow mapping enabled
- `controls`: PointerLockControls for first-person navigation

### Game State Machine
```javascript
state = {
  step: 0,              // Current objective step
  hasAlarm: false,      // Whether alarm was triggered
  hasExtinguisher: false, // Whether player has extinguisher
  fireOut: false,       // Whether fire is extinguished
  evacuated: false      // Whether player reached safe zone
}
```

### Interactive Objects
- **Fire Zone**: Burning barrel at position (-8, 0, -10)
- **Alarm**: Red box on right wall at (14.9, 1.5, 0)
- **Extinguisher**: Red cylinder on left wall at (5, 1.2, -14.8)
- **Safe Zone**: Green wall at z=15 (evacuation area)

### Visual Elements
- Room dimensions: 30×30 units with 4-unit ceiling
- Floor color: Light grey (#e0e0e0)
- Walls: Off-white (#f5f5f5) with one green safe zone wall
- Lighting: Bright indoor environment with dynamic effects

---

## 🚀 Future Enhancements

Potential improvements and features:
- [ ] Additional fire scenarios (multiple hazard types)
- [ ] Performance metrics and scoring system
- [ ] Difficulty levels
- [ ] Multiplayer support
- [ ] Mobile device support with gyro controls
- [ ] Additional interactive realistic elements
- [ ] Sound localization in VR mode
- [ ] More detailed 3D models and textures

---

## 📝 License

This project is designed for educational purposes.

---

## 🤝 Contributing

Feel free to extend this project with:
- New scenarios and hazards
- Improved graphics and models
- Additional educational content
- Performance optimizations

---

## 📧 Support

For issues or questions about the simulation, please review the inline code comments in `vr.html` for implementation details.
