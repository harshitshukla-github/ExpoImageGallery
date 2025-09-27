# 📱 Image Gallery App

A beautiful and intuitive image gallery app built with React Native and Expo. Browse your photos in a responsive grid layout, view them full-screen, and add new photos directly from your camera or photo library.

## ✨ Features

- **📸 Photo Grid Display**: View your photos in a clean, responsive 3-column grid layout
- **🔍 Full-Screen Viewer**: Tap any photo to view it in full-screen mode with smooth animations
- **📷 Camera Integration**: Take new photos directly from the app
- **🖼️ Photo Library Access**: Select and import photos from your device's photo library
- **🔐 Permission Management**: Smart permission handling with user-friendly prompts
- **⚡ Performance Optimized**: Efficient image loading and rendering for smooth scrolling
- **🎨 Modern UI**: Clean, modern interface with intuitive navigation
- **📱 Cross-Platform**: Works seamlessly on both iOS and Android

## 📋 Prerequisites

Before you begin, ensure you have the following installed:

- [Node.js](https://nodejs.org/) (version 16 or higher)
- [Expo CLI](https://docs.expo.dev/get-started/installation/)
- [Git](https://git-scm.com/)
- A physical device or emulator for testing

## 🚀 Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/image-gallery-app.git
cd image-gallery-app
```

### 2. Install Dependencies

```bash
npm install
```

### 3. Start the Development Server

```bash
npx expo start
```

### 4. Run on Your Device

- **iOS**: Scan the QR code with your iPhone's camera or use the Expo Go app
- **Android**: Scan the QR code with the Expo Go app
- **Simulator**: Press `i` for iOS simulator or `a` for Android emulator

## 📦 Dependencies

### Core Dependencies
- **React Native**: Mobile app framework
- **Expo**: Development platform and tools
- **expo-image-picker**: Camera and photo library access
- **expo-media-library**: Device media library integration
- **@expo/vector-icons**: Icon library

### Development Dependencies
- **@babel/core**: JavaScript compiler

## 🛠️ Project Structure

```
image-gallery-app/
├── App.js                 # Main application component
├── package.json          # Project dependencies and scripts
├── app.json              # Expo configuration
├── .gitignore            # Git ignore rules
├── README.md             # Project documentation
├── assets/               # App icons and splash screens
│   ├── icon.png
│   └── splash.png
└── node_modules/         # Installed dependencies
```

## 🔧 Configuration

### App Configuration (app.json)

Make sure your `app.json` includes the necessary permissions:

```json
{
  "expo": {
    "name": "Image Gallery",
    "slug": "image-gallery-app",
    "platforms": ["ios", "android"],
    "ios": {
      "infoPlist": {
        "NSCameraUsageDescription": "This app needs access to the camera to take photos.",
        "NSPhotoLibraryUsageDescription": "This app needs access to the photo library to display and select images."
      }
    },
    "android": {
      "permissions": [
        "CAMERA",
        "READ_EXTERNAL_STORAGE",
        "WRITE_EXTERNAL_STORAGE"
      ]
    }
  }
}
```

## 🎯 Usage

### Viewing Photos
1. Launch the app
2. Grant necessary permissions when prompted
3. Browse your photos in the grid layout
4. Tap any photo to view it full-screen
5. Tap outside the image or use the close button to return to the grid

### Adding Photos
1. Tap the "+" button in the header
2. Choose from two options:
   - **Camera**: Take a new photo
   - **Photo Library**: Select an existing photo
3. The new photo will appear in your gallery

## 🔒 Permissions

The app requires the following permissions:

- **Camera**: To take new photos
- **Media Library**: To access and display existing photos
- **Photo Library**: To select photos from your device

All permissions are requested with clear explanations of why they're needed.

## 🎨 Customization

### Styling
The app uses React Native's StyleSheet for styling. You can customize:

- **Grid Layout**: Modify `numColumns` to change the number of columns
- **Image Size**: Adjust `imageSize` calculation for different photo dimensions
- **Colors**: Update the color scheme in the styles object
- **Animations**: Customize modal transitions and touch feedback

### Grid Configuration
```javascript
const numColumns = 3; // Change to 2, 4, etc.
const imageSize = (width - 40) / numColumns;
```

## 🚀 Building for Production

### Android APK
```bash
npx expo build:android
```

### iOS IPA
```bash
npx expo build:ios
```

### Using EAS Build (Recommended)
```bash
npm install -g @expo/eas-cli
eas build --platform android
eas build --platform ios
```

## 🐛 Troubleshooting

### Common Issues

**Permission Denied Error**
- Ensure you've granted camera and media library permissions
- Try restarting the app after granting permissions

**Images Not Loading**
- Check device storage permissions
- Verify that photos exist in the device's media library

**App Crashes on Startup**
- Clear Expo cache: `npx expo start -c`
- Reinstall dependencies: `rm -rf node_modules && npm install`

## 📱 Testing

### Manual Testing Checklist
- [ ] App launches successfully
- [ ] Permissions are requested and handled properly
- [ ] Photo grid displays correctly
- [ ] Full-screen view works
- [ ] Camera functionality works
- [ ] Photo library selection works
- [ ] App handles empty photo library gracefully

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- [Expo Team](https://expo.dev/) for the excellent development platform
- [React Native Community](https://reactnative.dev/) for the robust framework
- [Ionicons](https://ionic.io/ionicons) for the beautiful icon set

## 📞 Support

If you encounter any issues or have questions:

1. Check the [troubleshooting section](#🐛-troubleshooting)
2. Open an issue on GitHub
3. Contact the development team

## 🔄 Version History

- **v1.0.0** - Initial release
  - Basic photo gallery functionality
  - Camera and photo library integration
  - Full-screen photo viewer
  - Permission management

---

Made with ❤️ using React Native and Expo
