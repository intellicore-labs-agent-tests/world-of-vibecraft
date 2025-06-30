# 🎮 World of Vibecraft

> A browser-based multiplayer pixel art game development platform with AI integration

[![Live Demo](https://img.shields.io/badge/Live-Demo-4CAF50?style=for-the-badge)](https://your-demo-url.netlify.app)
[![React](https://img.shields.io/badge/React-18.3.1-61DAFB?style=for-the-badge&logo=react)](https://reactjs.org/)
[![Supabase](https://img.shields.io/badge/Supabase-Backend-3ECF8E?style=for-the-badge&logo=supabase)](https://supabase.com/)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind-CSS-38B2AC?style=for-the-badge&logo=tailwind-css)](https://tailwindcss.com/)

## 🌟 Overview

World of Vibecraft is a comprehensive pixel art game development platform that runs entirely in your browser. Create, animate, and share pixel art games with integrated AI tools, real-time collaboration, and a powerful asset management system.

### ✨ Key Features

- 🎭 **Advanced Sprite Animation System** - 60fps animations with directional support
- 🗺️ **Tile-Based Level Editor** - Create worlds with collision layers and multi-resolution tiles
- 🗃️ **Asset Management** - Upload, organize, and share sprites, tilesets, and audio
- 🤖 **AI Integration** - OpenAI and ElevenLabs support for dynamic content
- 👥 **Multiplayer Ready** - Real-time collaboration and server selection
- 🛠️ **Development Tools** - Integrated debugging and state inspection

## 🚀 Quick Start

### Prerequisites

- Node.js 18+ 
- npm or yarn
- Supabase account (for backend features)

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/world-of-vibecraft.git
   cd world-of-vibecraft
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Set up environment variables**
   ```bash
   cp .env.example .env
   ```
   
   Add your Supabase credentials:
   ```env
   VITE_SUPABASE_URL=your_supabase_url
   VITE_SUPABASE_ANON_KEY=your_supabase_anon_key
   ```

4. **Start the development server**
   ```bash
   npm run dev
   ```

5. **Open your browser**
   Navigate to `http://localhost:5173`

## 🏗️ Architecture

### Tech Stack

- **Frontend**: React 18.3.1, Tailwind CSS, Lucide React
- **Backend**: Supabase (PostgreSQL, Auth, Storage)
- **State Management**: Custom reactive StateManager
- **Build Tool**: Vite
- **Deployment**: Netlify

### Project Structure

```
src/
├── components/           # React components
│   ├── auth/            # Authentication components
│   ├── dev/             # Development tools
│   ├── game/            # Game interface components
│   ├── layout/          # Layout components
│   └── assets/          # Asset management
├── hooks/               # Custom React hooks
├── core/                # Core systems (StateManager)
├── lib/                 # External service integrations
└── main.tsx            # Application entry point
```

## 🎮 Features Deep Dive

### Sprite Animation System

Create smooth 60fps character animations with our advanced sprite system:

- **8×8 Grid Support**: Optimized for 512×512px sprite sheets
- **Directional Animations**: Idle, walk, run, jump in all directions
- **Frame Management**: Configurable timing and frame sequences
- **Real-time Preview**: Test animations instantly

```javascript
// Example: Character movement with animation
const character = {
  position: { x: 300, y: 200 },
  direction: 'right',
  state: 'walking',
  speed: 2.5
};
```

### Level Editor

Build worlds with our tile-based editor:

- **Multi-Resolution Tiles**: 8×8 to 64×64 pixel support
- **Collision Layers**: Visual collision editing with transparency
- **Import/Export**: Save and share level data
- **Paint Tools**: Brush, erase, and special object placement

### Asset Management

Organize your game assets efficiently:

- **File Upload**: Drag-and-drop sprite sheets, tilesets, audio
- **Tagging System**: Organize assets with custom tags
- **Permission Control**: Public/private asset sharing
- **Version Control**: Track asset changes and updates

### AI Integration Framework

Enhance your games with AI:

- **OpenAI Integration**: Dynamic NPC dialogue generation
- **ElevenLabs Voice**: Text-to-speech for character voices
- **Smart Suggestions**: AI-assisted content creation
- **API Management**: Secure key storage and validation

## 🔧 Development

### Available Scripts

```bash
npm run dev          # Start development server
npm run build        # Build for production
npm run preview      # Preview production build
npm run lint         # Run ESLint
```

### Development Mode

Access advanced development tools:

1. **Login** with Developer or Master role
2. **Toggle Dev Mode** in the game hub
3. **Access Tools**: Sprite tester, level editor, asset manager

### Database Setup

The project uses Supabase with the following tables:

- `user_profiles` - User information and roles
- `game_assets` - Asset metadata and storage references

Row Level Security (RLS) is enabled for data protection.

## 🎯 User Roles

### User
- Basic game access
- Asset viewing
- Community features

### Developer  
- Development tools access
- Asset upload and management
- Debug capabilities

### Master
- Full administrative access
- User management
- Production asset promotion

## 🌐 Deployment

### Netlify Deployment

1. **Build the project**
   ```bash
   npm run build
   ```

2. **Deploy to Netlify**
   - Connect your GitHub repository
   - Set build command: `npm run build`
   - Set publish directory: `dist`
   - Add environment variables

### Environment Variables

Required for production:

```env
VITE_SUPABASE_URL=your_production_supabase_url
VITE_SUPABASE_ANON_KEY=your_production_anon_key
```

## 🤝 Contributing

We welcome contributions! Please see our [Contributing Guide](CONTRIBUTING.md) for details.

### Development Workflow

1. Fork the repository
2. Create a feature branch: `git checkout -b feature/amazing-feature`
3. Commit changes: `git commit -m 'Add amazing feature'`
4. Push to branch: `git push origin feature/amazing-feature`
5. Open a Pull Request

### Code Style

- Use TypeScript for new components
- Follow React hooks patterns
- Maintain pixel-perfect styling
- Add JSDoc comments for complex functions

## 📚 Documentation

- [Project Structure](docs/PROJECT_STRUCTURE.md)
- [State Management](docs/STATE_MANAGEMENT.md)
- [Development Tools](docs/DEV_PANEL.md)
- [Sprite Animation Guide](docs/SPRITE_ANIMATION_TESTER.md)
- [Level Editor Guide](docs/TILESET_LEVEL_EDITOR.md)

## 🐛 Troubleshooting

### Common Issues

**Development server won't start**
- Check Node.js version (18+ required)
- Clear node_modules: `rm -rf node_modules && npm install`

**Supabase connection errors**
- Verify environment variables
- Check Supabase project status
- Ensure RLS policies are configured

**Asset upload failures**
- Check file size limits
- Verify user permissions
- Ensure storage buckets exist

## 🔮 Roadmap

### Phase 1: Core Platform ✅
- [x] Sprite animation system
- [x] Level editor
- [x] Asset management
- [x] User authentication

### Phase 2: AI Integration 🚧
- [ ] OpenAI dialogue system
- [ ] ElevenLabs voice synthesis
- [ ] AI-assisted content creation
- [ ] Smart recommendations

### Phase 3: Multiplayer 📋
- [ ] Real-time collaboration
- [ ] Server infrastructure
- [ ] Guild system
- [ ] Community features

### Phase 4: Platform Expansion 🔮
- [ ] Mobile support
- [ ] Game export
- [ ] Marketplace
- [ ] Educational tools

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- **React Team** - For the amazing framework
- **Supabase** - For the backend infrastructure
- **Tailwind CSS** - For the utility-first styling
- **Lucide** - For the beautiful icons
- **Community** - For feedback and contributions

## 📞 Support

- 📧 Email: support@worldofvibecraft.com
- 💬 Discord: [Join our community](https://discord.gg/vibecraft)
- 🐛 Issues: [GitHub Issues](https://github.com/yourusername/world-of-vibecraft/issues)
- 📖 Docs: [Documentation Site](https://docs.worldofvibecraft.com)

---

<div align="center">

**[🎮 Try the Demo](https://your-demo-url.netlify.app)** • **[📚 Read the Docs](docs/)** • **[🤝 Contribute](CONTRIBUTING.md)**

Made with ❤️ by the World of Vibecraft team

</div>
