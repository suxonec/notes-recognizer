# Piano Note Recognizer

A web application that listens to audio input or MIDI and displays detected notes on a musical staff in real time.

## Version 2 Features

### New in v2:
1. **MIDI Input Support** - Connect MIDI devices (keyboards, controllers) and detect notes directly
2. **Dual Input Sources** - Switch between microphone and MIDI input
3. **Note Naming Systems** - Choose between English (C, D, E, F, G, A, B) or Russian (До, Ре, Ми, Фа, Соль, Ля, Си) note names
4. **Improved History** - Notes now appear chronologically with the latest note at the end and highlighted
5. **MIDI Device Selection** - Select from available MIDI devices when multiple are connected

## Tech Stack

- **Vanilla HTML/CSS/JS** - Single file, no build step required
- **VexFlow 4.2.2** - Sheet music rendering via CDN
- **Web Audio API** - Microphone capture and pitch detection
- **Web MIDI API** - MIDI device support
- **No backend** - Runs entirely in the browser

## Features

### Core Functionality
- Real-time microphone capture with pitch detection
- MIDI device input support
- Autocorrelation algorithm (YIN) for frequency detection
- Frequency-to-note conversion for piano range (C3-C6)
- 180ms debounce to prevent duplicate notes
- Sequential note display on treble clef staff
- Scrollable note history (last 15 notes)
- Volume and clarity/confidence meters (microphone mode)
- Clear staff button
- Multiple note naming systems

### Technical Details
- **Piano Range**: C3–C6 (frequencies ~130 Hz to ~1050 Hz)
- **Buffer Size**: 2048 samples for audio analysis
- **Debounce Time**: 180ms for stable note detection
- **History Limit**: 15 notes maximum
- **Staff Capacity**: 12 notes visible simultaneously

## Browser Support

- **Chrome/Edge**: Full support (microphone + MIDI)
- **Firefox**: Full support (microphone + MIDI)
- **Safari**: Microphone support, limited MIDI support

## How to Use

### Microphone Mode
1. Open `index.html` in a browser
2. Select "Microphone" as input source
3. Click "Start" and allow microphone access
4. Play piano notes or sing/whistle in the C3-C6 range
5. Watch notes appear on the staff after holding them for ~180ms
6. Monitor volume and clarity meters for signal quality

### MIDI Mode
1. Connect a MIDI keyboard or controller to your computer
2. Open `index.html` in a browser
3. Select "MIDI" as input source
4. Choose your MIDI device from the dropdown
5. Click "Start"
6. Play notes on your MIDI device
7. Notes appear instantly on the staff

### Note Naming
- Use the "Note Naming" selector to switch between English and Russian note names
- The history updates automatically to reflect your choice
- The staff always uses standard musical notation

## Files

- `index.html` - Version 2 (current)
- `index_V1.html` - Version 1 (microphone only)
- `README.md` - This file

## Version History

### Version 2
- Added MIDI input support
- Added input source selection (microphone/MIDI)
- Added note naming system selection (English/Russian)
- Improved history display (chronological, latest highlighted)
- Added MIDI device selection

### Version 1
- Initial release
- Microphone input only
- Autocorrelation pitch detection
- VexFlow staff rendering
- Note history
- Volume and clarity meters

## License

MIT License - Feel free to use and modify!
