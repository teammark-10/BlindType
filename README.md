# Accessible Typing Tutor

An accessible, speech-enabled typing tutor designed specifically for blind and visually impaired users, inspired by Monkeytype. The application provides real-time audio feedback and complete keyboard-only navigation.

## 🎯 Features

### Core Functionality
- **Audio-First Design**: Uses Web Speech API (speechSynthesis) for real-time voice feedback
- **Keyboard-Only Navigation**: Fully accessible without mouse interaction
- **Smart Directional Guidance**: QWERTY layout-based directional instructions when incorrect keys are pressed
- **Progress Tracking**: Saves your progress in localStorage between sessions
- **Adaptive Keyboard Support**: Supports both full-size and compact keyboards

### Accessibility Features
- **Screen Reader Compatible**: Proper ARIA roles and live regions
- **High Contrast Design**: Dark theme optimized for low vision users
- **Focus Management**: Clear focus indicators and logical tab order
- **Audio Announcements**: All interactions provide immediate audio feedback

### User Experience
- **Real-time Feedback**: Instant audio response for correct/incorrect keystrokes
- **Word Repetition**: Press 'R' to repeat the current word
- **Session Management**: Pause with 'Escape' key
- **Visual Indicators**: Color-coded letters for users with some vision (green=correct, red=incorrect)

## 🛠 Technology Stack

- **React 18** with TypeScript
- **TailwindCSS** for styling
- **Vite** for fast development and building
- **Web Speech API** for text-to-speech functionality
- **localStorage** for progress persistence

## 🚀 Getting Started

### Prerequisites
- Node.js (version 16 or higher)
- NPM or Yarn package manager
- Modern web browser with Web Speech API support

### Installation

1. **Install dependencies:**
   ```bash
   npm install
   ```

2. **Start the development server:**
   ```bash
   npm run dev
   ```

3. **Open in browser:**
   - Navigate to `http://localhost:5173`
   - Ensure your browser supports Web Speech API (Chrome, Edge, Safari recommended)

### Building for Production

```bash
npm run build
npm run preview
```

## 🎮 How to Use

### Initial Setup
1. **Keyboard Selection**: Choose between full-size or compact keyboard layout
2. **Start Session**: Press Space or click "Start Typing Session"

### During Typing
- **Listen**: Each word is announced via speech synthesis
- **Type**: Type the word using your keyboard
- **Feedback**: Receive instant audio feedback for each keystroke
  - Correct key: "Good job!"
  - Incorrect key: Detailed guidance with directional instructions

### Keyboard Commands
- **R**: Repeat current word
- **Escape**: Pause session
- **Space**: Start/continue session
- **Letters**: Type the current word

### Audio Feedback Examples
- ✅ Correct keystroke: "Good job!"
- ❌ Incorrect keystroke: "Wrong key. You pressed 'd'. The correct letter is 's'. Move one key to the left."
- 🎉 Word completed: "Excellent! Moving to next word."

## 📊 Features in Detail

### Directional Guidance System
The app provides intelligent keyboard navigation guidance based on QWERTY layout:
- Identifies the position of pressed vs. expected keys
- Gives specific directional instructions (up/down/left/right)
- Counts key distances for precise guidance

### Word List
Includes 20 carefully selected words of varying difficulty:
`apple`, `banana`, `cherry`, `dog`, `elephant`, `flower`, `guitar`, `house`, `island`, `jungle`, `keyboard`, `lemon`, `monkey`, `notebook`, `ocean`, `piano`, `queen`, `rainbow`, `star`, `tiger`

### Progress Tracking
- Counts correctly completed words
- Saves progress in browser localStorage
- Displays current score during sessions
- Persists between browser sessions

## ♿ Accessibility Standards

This application follows WCAG 2.1 AA guidelines:
- **Keyboard Navigation**: All functionality accessible via keyboard
- **Screen Reader Support**: Proper semantic HTML and ARIA labels
- **Focus Management**: Clear visual and programmatic focus indicators
- **Color Independence**: Audio feedback doesn't rely on color alone
- **User Control**: Users can pause, repeat, and control speech

## 🔧 Technical Architecture

### Component Structure
```
src/
├── components/
│   └── TypingTrainer.tsx     # Main typing interface
├── hooks/
│   └── useSpokenFeedback.ts  # Speech synthesis hook
├── utils/
│   └── keyboardUtils.ts      # QWERTY layout and guidance
├── types.ts                  # TypeScript definitions
├── App.tsx                   # Root component
└── main.tsx                  # Entry point
```

### Key Technologies Used
- **React Hooks**: State management and lifecycle
- **Web Speech API**: Text-to-speech functionality
- **TailwindCSS**: Utility-first styling
- **TypeScript**: Type safety and better development experience
- **Vite**: Fast build tool and development server

## 🎨 Design Philosophy

### Audio-First Approach
- Every interaction provides immediate audio feedback
- Visual elements support but don't replace audio cues
- Speech synthesis parameters optimized for clarity

### Inclusive Design
- Designed for blind users but usable by everyone
- Multiple input modalities (keyboard, some visual cues)
- Flexible and forgiving interaction patterns

### Performance Optimized
- Minimal dependencies
- Fast load times
- Efficient speech synthesis management

## 🐛 Browser Compatibility

### Fully Supported
- Chrome 33+
- Edge 14+
- Safari 7+

### Limited Support
- Firefox: Web Speech API support varies
- Mobile browsers: May have limited speech synthesis

### Recommendations
- Use Chrome or Edge for best experience
- Enable JavaScript and Web Speech API
- Use headphones for better audio clarity

## 🤝 Contributing

This is an educational project demonstrating accessible web development practices. Key areas for potential enhancement:

1. **Additional Languages**: Multi-language word lists and speech
2. **Advanced Metrics**: WPM tracking, accuracy statistics
3. **Custom Word Lists**: User-defined practice words
4. **Difficulty Levels**: Progressive difficulty system
5. **Voice Selection**: Multiple speech synthesis voices

## 📝 License

This project is open source and available under the MIT License.

## 🙏 Acknowledgments

- Inspired by Monkeytype's clean design
- Built with accessibility-first principles
- Designed for the blind and visually impaired community 