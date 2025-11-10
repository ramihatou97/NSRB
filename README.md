# NeuroScribe

**AI-Powered Clinical Documentation System with Built-in Quality Validation**

NeuroScribe is a single-file, zero-dependency clinical documentation tool that combines advanced AI generation with a 6-layer industrial-grade validation pipeline. Designed specifically for neurosurgical practice, it ensures every generated note meets the highest standards of accuracy and completeness.

## Key Features

### Core Capabilities
- **Pre-Consultation Briefing**: Research pathologies across 8 categories with 3 depth levels
- **Voice Recording**: Real-time transcription using Web Speech API (Chrome/Edge)
- **SOAP Quick-Entry**: Both simple AI parsing and advanced structured input modes
- **Clinical Scales**: 6 embedded scales (mJOA, Nurick, NDI, ODI, VAS, GCS)
- **Document Upload**: Multi-file support (PDF, DOC, DOCX, TXT)
- **Interactive Review**: AI-powered suggestion parsing with dependency tracking
- **Multiple Export Formats**: DOAP, ULTRATHINK, Telegram compression modes

### V8 Validation Engine
NeuroScribe includes a comprehensive 6-layer validation system:

1. **Source Grounding**: Verifies quotes match source text with coverage tracking
2. **Fabrication Detection**: AI-powered hallucination detection with semantic analysis
3. **Completeness Check**: Bidirectional validation ensures nothing is missed
4. **Consistency Validation**: Medical logic checks including functional scores and anatomical rules
5. **Proportionality Check**: Output/input ratio analysis for appropriate detail level
6. **Confidence Calibration**: Multi-source adjustment with over-confidence detection

### Professional UI
- Real-time quality score display with color-coded badges (🟢/🟡/🔴)
- Animated progress bars for each validation layer
- Detailed error and warning reporting
- Auto-generated validation reports after each note generation

## Quick Start

### 1. Open the Application
```bash
open neuroscribe.html
# or
open src/neuroscribe-V8-MITIGATIONS.html
```

### 2. Configure API Key
- Click "⚙️ Settings" in the interface
- Paste your Google Gemini API key
- Key is stored securely in browser localStorage

### 3. Generate Your First Note
- Enter clinical transcript or use voice recording
- Click "✨ Generate Clinical Note"
- Wait 15-30 seconds for generation + validation
- Review quality report in the "🔍 Quality Report" tab

## Technical Specifications

### Architecture
- **Type**: Single HTML file (self-contained)
- **Dependencies**: Zero - truly portable
- **Size**: 586 KB
- **Lines of Code**: 11,458
- **API**: Google Gemini 2.0 Flash
- **Storage**: localStorage for settings and data
- **Execution**: Browser-only (no Node.js, no build process)

### Browser Compatibility
- ✅ Chrome/Edge (recommended) - Full support including voice
- ✅ Firefox - All features except voice recording
- ✅ Safari - All features except voice recording
- ⚠️ Voice recording requires Chrome/Edge (Web Speech API)

### Code Statistics
```
Total Lines: 11,458
├── HTML/CSS: 1,104 lines (9.6%)
├── Clinical Scales DB: 881 lines (7.7%)
├── Validation Engine: 3,752 lines (32.8%)
└── V7 Application + UI: 5,721 lines (49.9%)

Total Classes: 7 (validation)
Total Functions: 107
Total Features: 15 (9 core + 6 validation layers)
```

## Project Structure

```
neuroscribe/
├── neuroscribe.html                    # Symlink to current version
├── README.md                           # This file
├── QUICK_START.md                      # Quick reference guide
├── src/
│   └── neuroscribe-V8-MITIGATIONS.html # Current production version
├── archive/
│   ├── versions/                       # Previous working versions
│   ├── backups/                        # Compressed backups
│   └── standalone/                     # Standalone components
├── docs/
│   ├── development/                    # Development progress docs
│   ├── testing/                        # Testing plans and guides
│   └── guides/                         # User guides
└── tests/
    └── test-validation-tab.html        # Test files
```

## Documentation

### Getting Started
- [QUICK_START.md](QUICK_START.md) - Fast-track guide for immediate use

### Development
- [CURRENT_STATUS.md](docs/development/CURRENT_STATUS.md) - Current project status
- [PHASE_8_COMPLETE.md](docs/development/PHASE_8_COMPLETE.md) - Latest implementation details
- [INTEGRATION_COMPLETE_STATUS.md](docs/development/INTEGRATION_COMPLETE_STATUS.md) - Integration documentation

### Testing
- [V8-TEST-PLAN.md](docs/testing/V8-TEST-PLAN.md) - Comprehensive testing plan
- [PHASE_9_TESTING_PLAN.md](docs/testing/PHASE_9_TESTING_PLAN.md) - End-to-end testing guide

### User Guides
- [SAFE_WORKING_VERSION_README.md](docs/guides/SAFE_WORKING_VERSION_README.md) - Detailed usage guide

## Features in Detail

### 1. Pre-Consultation Briefing
Research any pathology before seeing the patient:
- **8 Categories**: Degenerative, Tumor, Vascular, Trauma, Infection, Congenital, Functional, Other
- **3 Depth Levels**: Quick (2 min), Standard (5 min), Deep (10 min)
- **Smart Integration**: Briefing data enhances note generation

### 2. Voice Recording (Chrome/Edge only)
- Real-time speech-to-text transcription
- Start/Stop controls with visual feedback
- Instant integration with note generation

### 3. SOAP Quick-Entry
**Simple Mode**: AI automatically parses freeform text into SOAP format
**Advanced Mode**: Separate fields for S/O/A/P with enhancement toggles

### 4. Clinical Scales
Embedded calculators for:
- **mJOA**: Modified Japanese Orthopedic Association
- **Nurick**: Cervical Myelopathy Grading
- **NDI**: Neck Disability Index
- **ODI**: Oswestry Disability Index
- **VAS**: Visual Analog Scale (Pain)
- **GCS**: Glasgow Coma Scale

### 5. Validation Quality Report
After each generation, view:
- Overall quality score (0-100)
- Individual layer scores with detailed breakdowns
- Specific errors and warnings
- Recommendations for improvement

## Development Status

**Current Version**: V8 (with mitigations)
**Status**: Production Ready
**Last Updated**: 2025-11-08

### Completed Phases
- ✅ Phase 1-6: Validation engine porting and integration
- ✅ Phase 7: Validation workflow integration
- ✅ Phase 8: Validation UI implementation
- ✅ Phase 9: End-to-end testing

### Version History
- **V8**: Current production version with mitigations
- **V7**: Full feature set with 6-layer validation
- **V6**: Interactive review implementation
- **V1-5**: Core feature development

## Requirements

### Mandatory
- Modern web browser (Chrome, Firefox, Safari, Edge)
- Google Gemini API key ([Get one here](https://makersuite.google.com/app/apikey))

### Optional
- Chrome/Edge for voice recording feature
- Internet connection for API calls

## Security & Privacy

- **API Key**: Stored locally in browser (localStorage), never transmitted except to Google Gemini
- **Data**: All processing local except AI generation calls
- **No Tracking**: No analytics, no data collection, no external dependencies
- **HIPAA Consideration**: Use appropriate safeguards for patient data

## Troubleshooting

### Validation Not Running
1. Check browser console (F12) for errors
2. Verify API key is configured
3. Ensure sufficient API quota

### Voice Recording Not Working
- Voice recording requires Chrome or Edge browser
- Check microphone permissions in browser settings

### Generation Fails
- Verify API key is valid
- Check internet connection
- Review console for detailed error messages

## Contributing

This is currently a single-developer project. For questions or issues:
1. Review documentation in `docs/` directory
2. Check console for error messages
3. Refer to testing plans in `docs/testing/`

## License

[Specify your license here]

## Acknowledgments

Built with:
- Google Gemini 2.0 Flash API
- Web Speech API (Chrome/Edge)
- Pure JavaScript (no frameworks)
- Love for neurosurgery and quality documentation

---

**Version**: V8 with Mitigations
**File Size**: 586 KB
**Lines of Code**: 11,458
**Last Updated**: 2025-11-08
