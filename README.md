# Dragonsweeper Mobile

A mobile app version of [Dragonsweeper](https://danielben.itch.io/dragonsweeper) by Daniel Benmergui - a roguelike minesweeper adventure!

## About the Game

Dragonsweeper is a strategy game where you clear a dungeon of monsters and defeat the dragon at its center. Unlike traditional Minesweeper, the numbers indicate the total level of all monsters in adjacent tiles. You must carefully plan your moves, level up by defeating monsters, and gather enough hearts to face the dragon.

## Features

- Cross-platform mobile app built with Capacitor
- Optimized for touch controls
- Full offline support
- Same great gameplay as the web version

## Building

### Prerequisites

- Node.js 18+
- Android Studio (for Android builds)
- JDK 17

### Setup

```bash
# Install dependencies
npm install

# Sync Capacitor
npx cap sync

# Open in Android Studio
npx cap open android
```

### Build APK

```bash
# Debug build
cd android && ./gradlew assembleDebug

# Release build
cd android && ./gradlew assembleRelease
```

The APK files will be in `android/app/build/outputs/apk/`.

## CI/CD

This project uses GitHub Actions to automatically build APKs:

- **On push to main**: Builds debug and release APKs, uploads as artifacts
- **On tag push (v*)**: Creates a GitHub Release with the APKs

To create a release:
```bash
git tag v1.1.18
git push origin v1.1.18
```

## Credits

- **Game**: [Dragonsweeper](https://danielben.itch.io/dragonsweeper) by Daniel Benmergui
- **Mobile wrapper**: Built with [Capacitor](https://capacitorjs.com/)

## License

The game content is property of Daniel Benmergui. The mobile wrapper code is MIT licensed.
