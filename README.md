# AI-Powered Voice-Based Cold Calling Agent

## Project Description
This AI-powered voice-based cold calling agent dynamically selects relevant responses based on user interactions in real-time. It supports various conversation scenarios, such as:
- Scheduling an ERP system demo.
- Conducting technical interviews.
- Sending polite yet firm payment reminders.

The agent integrates speech recognition (STT), text-to-speech (TTS), and Gemini AI to generate responses, providing a seamless interactive experience in Hinglish.

## Setup and Installation

### Prerequisites
Ensure you have the following installed:
- Python 3.8+
- Conda (optional but recommended)
- Required Python packages:
  - `speechrecognition`
  - `gtts`
  - `pygame`
  - `google-generativeai`
  - `python-dotenv`

### Steps to Set Up
1. Clone the repository:
   ```bash
   git clone https://github.com/your-repo/cold-call-agent.git
   cd cold-call-agent
   ```
2. Set up a virtual environment:
   ```bash
   conda create --name call_agent python=3.8 -y
   conda activate call_agent
   ```
3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
4. Set up the environment variables:
   - Create a `.env` file in the root directory.
   - Add the following line, replacing `your_api_key` with your actual API key:
     ```
     GEMINI_API_KEY=your_api_key
     ```
5. Run the AI agent:
   ```bash
   python cold_call_agent.py
   ```

## Models and Data Used
- **Speech Recognition**: Google Speech Recognition API (STT)
- **Text-to-Speech**: Google Text-to-Speech (`gTTS`)
- **AI Model**: Gemini AI (`gemini-1.5-pro`)
- **Data Sources**:
  - No predefined dataset; conversations are dynamically processed in real-time.
  
## Agent Architecture
The AI agent follows a modular architecture with:
1. **Speech Recognition (`recognize_speech`)**: Captures user input via microphone and converts it to text.
2. **Text-to-Speech (`speak`)**: Converts AI-generated responses to speech and plays them using `pygame`.
3. **Cold Call Agent (`ColdCallAgent`)**:
   - Selects a conversation scenario (`demo`, `interview`, `payment`).
   - Generates responses using Gemini AI based on the scenario.
   - Maintains conversation history for context-aware replies.
4. **Main Controller (`start_call`, `end_call`)**:
   - Manages call initiation, user input handling, and termination.

## Features Overview
| Feature | Status |
|---------|--------|
| Speech recognition | ✅ Completed |
| Text-to-speech | ✅ Completed |
| AI-generated responses | ✅ Completed |
| Dynamic conversation handling | ✅ Completed |
| Scenario-specific responses | ✅ Completed |
| Conversation history tracking | ✅ Completed |
| Real-time interactive conversation | ✅ Completed |
| Improved response delays | ⏳ Partially implemented |
| Multi-lingual support | ❌ Not implemented |

## Demonstration Video
Watch the agent in action: [Loom Video Link](#)

## Future Improvements
- Enhancing response delay handling to ensure smoother conversation flow.
- Expanding language support beyond Hinglish.
- Improving response coherence through advanced context tracking.
- Adding GUI for easier scenario selection.

## License
This project is licensed under the MIT License.

---
For questions or contributions, feel free to open an issue or submit a pull request!

