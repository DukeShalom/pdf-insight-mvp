# Solace Voice Features — User Documentation

## 🎤 Voice Interaction Overview

Solace now empowers users with **full voice-to-text and text-to-speech capabilities**, creating an accessible, hands-free journaling experience. Users can choose to write or speak their feelings naturally.

---

## ✨ Key Voice Features

### 1. **Input Mode Toggle**
- Users see two clear options on the journal page:
  - **✏️ Type** — Traditional text input
  - **🎤 Voice** — Speech-to-text input
- Toggle seamlessly between modes with a single tap
- Selected mode is highlighted with gradient background

### 2. **Speech-to-Text (Voice Recording)**

#### Starting a Recording
- Tap **"🎤 Start Recording"** button
- Red pulsing animation indicates active recording
- Animated waveform visualization plays during recording
- Real-time status: "🎤 Listening..."

#### Live Transcription
- **Real-time interim results** appear as you speak
- Interim text appears in italic, slightly transparent (shows it's being processed)
- Final transcription becomes solid text when Solace recognizes sentence breaks
- Character-accurate speech recognition via Web Speech API

#### Stopping Recording
- Red **"⏹️ Stop"** button replaces the start button while recording
- Tap to end recording anytime
- Status updates: "✓ Transcription complete"
- Full transcribed text appears in the transcript box

#### Visual Feedback
- **Waveform animation** — Five bars animated to simulate sound waves
- **Interim transcript styling** — Lighter/italicized text shows real-time speech
- **Status messages** — Clear feedback at every step
- **Error handling** — User-friendly error messages if recognition fails

### 3. **Text-to-Speech (AI Response Playback)**

#### Playing AI Responses
- After receiving an AI response in **voice mode**, a **"🔊 Play Response"** button appears
- Click to hear Solace's response spoken naturally
- Button changes to **"⏹️ Stop Playing"** while audio is playing
- Response is spoken at a comfortable pace (0.95x speed)

#### Natural Voice
- Smooth, clear voice synthesis
- Balanced pitch and volume for emotional resonance
- Mimics the warm, compassionate tone of Solace

### 4. **Input Method Memory**
- Each journal entry records whether it was created via **text** or **voice**
- History page can show this metadata (future enhancement)
- Enables personalized user insights

---

## 🎯 User Experience Flow

### Voice Journaling Workflow

1. **Select Voice Mode**
   - Tap "🎤 Voice" button on journal page

2. **Record Your Thoughts**
   - Tap "🎤 Start Recording"
   - Speak freely about how you're feeling
   - Watch waveform animate and see live transcription

3. **Review Transcription**
   - Tap "⏹️ Stop" when finished
   - Review the transcribed text
   - Edit directly in the transcript box if needed

4. **Submit Entry**
   - Tap "Send to Solace ♥"
   - Solace processes your entry and generates a response

5. **Hear Solace's Response**
   - "🔊 Play Response" button appears
   - Tap to hear Solace's warm, caring response read aloud
   - Tap "⏹️ Stop Playing" to stop playback

---

## 🛠️ Technical Implementation

### Browser Compatibility
- **Speech Recognition**: Chrome, Edge, Safari (iOS 14.5+), Firefox
- **Text-to-Speech**: All modern browsers (Chrome, Firefox, Safari, Edge)
- Graceful degradation: Voice buttons disabled if not supported

### APIs Used
1. **Web Speech API** (SpeechRecognition)
   - Real-time speech-to-text conversion
   - Continuous listening with interim results
   - Error handling for network/permission issues

2. **Speech Synthesis API** (SpeechSynthesis)
   - Text-to-speech for AI responses
   - Configurable rate, pitch, and volume
   - Play/pause/stop controls

### Data Privacy
- Speech data is processed locally in the browser
- No server-side speech processing (MVP)
- Transcribed text stored only in browser localStorage
- Users maintain full privacy and control

---

## 📱 Mobile-First Design

### Touch Optimization
- Large, easy-to-tap buttons (min 44px height)
- Full-screen waveform visualization
- Scrollable transcript area
- Bottom navigation remains accessible

### Responsive Behavior
- Buttons stack vertically on narrow screens
- Flexible grid layout adapts to all devices
- Touch-friendly spacing throughout

---

## ♿ Accessibility Features

### Voice as Accessibility Tool
- **Hands-free journaling** for users with mobility limitations
- **Audio playback** for users with visual impairments
- **Real-time transcription** helps users with hearing aid compatibility

### Keyboard Support
- All buttons accessible via keyboard
- Tab navigation between input modes
- Enter key to submit (with Shift for multiline textarea)

---

## 🔐 Safety & Privacy

### Crisis Detection
- Crisis keywords detection works for both text AND voice input
- Same emergency resources displayed regardless of input method
- Crisis Text Line info: "Text HOME to 741741"

### Permission Handling
- Browser requests microphone permission on first use
- User can revoke permissions in browser settings
- Clear messaging about permission requirements

---

## 🚀 Future Enhancements

1. **Multi-language Support** — Spanish, French, German voice recognition
2. **Voice Profiles** — Train AI to recognize user's emotional tone
3. **Mood Emoji from Voice Tone** — Auto-detect mood from voice intonation
4. **Transcription Editing** — Click words to correct misheard phrases
5. **Voice Diary Sharing** — Share audio journals with trusted friends/therapists
6. **Custom Voice Options** — Choose Solace's voice personality (soothing, energetic, etc.)
7. **Server-side Processing** — Upgrade to enterprise-grade speech APIs (Google Cloud, Azure)
8. **Ambient Sounds** — Optional background sounds during recording (rain, forest, café ambience)

---

## ✅ What's Enabled Right Now

✓ Full speech-to-text with live transcription
✓ Animated waveform visualization
✓ Text-to-speech AI response playback
✓ Seamless text/voice mode switching
✓ Crisis detection for voice entries
✓ Mobile-optimized voice interface
✓ localStorage persistence
✓ Browser-native implementation (no backend needed)

---

## 🎤 Example Interaction

**User:** *taps Voice mode, starts recording*

"I've been really overwhelmed at work today. My team keeps asking me to do more, but I'm already stretched thin. I feel like I'm not good enough, and it's eating me up."

*System transcribes in real-time, shows waveform*

**After submission, Solace responds:**

"It sounds like you're carrying a lot of weight at work, and that's completely understandable. Feeling stretched thin while doubting yourself is a heavy combination. What strikes me is how deeply you care about doing well — that's a strength. Today, remind yourself that you're already enough. Take one small break just for yourself. You've earned it. ♥"

**User:** *taps Play Response button*

*Solace's warm voice reads the response aloud*

---

## 📞 Support & Troubleshooting

### Microphone not working?
1. Check browser microphone permissions
2. Reload page and try again
3. Verify browser supports Web Speech API

### Speech recognition not accurate?
1. Speak slowly and clearly
2. Minimize background noise
3. Use English language setting (currently optimized for en-US)

### Can't hear Solace's response?
1. Check device volume
2. Ensure browser has speaker access
3. Try different browser if issue persists

---

**Solace Voice is designed to meet users where they are — whether they're typing, speaking, or switching between both. Every interaction is warm, accessible, and deeply human.**