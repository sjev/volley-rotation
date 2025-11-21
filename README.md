# 🏐 Volleybal Rotatiebord

A digital volleyball rotation board for coaches to visualize player positions and detect rotation faults in real-time.

## 🎯 Features

- **Interactive Court**: Drag players around a half-court visualization with 6 zones
- **Rotation Controls**: Rotate players clockwise or counterclockwise with one tap
- **Fault Detection**: Automatic detection and highlighting of rotation rule violations
- **Touch-Friendly**: Optimized for tablets and touchscreens
- **Single File App**: No dependencies, no build process - just open and use

## 🚀 Usage

### Online
Visit the live demo: [GitHub Pages](https://sjev.github.io/volley-rotation/app/volleybal-rotatiebord.html)

### Local
Simply open `app/volleybal-rotatiebord.html` in your web browser. No installation required.

## 🎮 Controls

- **← Button**: Rotate players counterclockwise
- **→ Button**: Rotate players clockwise  
- **↺ Button**: Reset players to zone centers

## 👥 Player Roles

The app uses standard Dutch volleyball position abbreviations:

| Role | Dutch | English | Color |
|------|-------|---------|-------|
| **SV** | Spelverdeler | Setter | Blue |
| **PL1/PL2** | Passer-loper | Outside Hitter | Green |
| **M1/M2** | Middenblokeerder | Middle Blocker | Red |
| **D** | Diagonaal | Opposite | Yellow |

## 🚨 Fault Detection

The board automatically checks 7 rotation rules:
- Front row left-right positioning (zones 4-3, 3-2)
- Back row left-right positioning (zones 5-6, 6-1)
- Front-back alignment (zones 4-5, 3-6, 2-1)

Players violating rotation rules are highlighted with a red glow.

## 🛠️ Development

This is a single-file HTML application with embedded CSS and JavaScript. No build tools or package managers required.

To modify:
1. Clone this repository
2. Edit `app/volleybal-rotatiebord.html`
3. Open in a browser to test
4. Commit and push changes

See [DESIGN.md](DESIGN.md) for design principles and implementation details.

## 📄 License

MIT License - see [LICENSE](LICENSE) file for details

## 🤝 Contributing

Contributions welcome! Please feel free to submit issues or pull requests.
