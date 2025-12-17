# AI Chess Agent

An interactive chess game where two AI agents powered by OpenAI's GPT-4o-mini play against each other using the AutoGen framework. Built with Streamlit for an intuitive web interface.

## Features

- **AI vs AI Chess Gameplay**: Watch two intelligent agents compete in a full chess match
- **Real-time Board Visualization**: SVG-based chess board with move highlighting and animations
- **Configurable Game Length**: Set maximum turns to control game duration and API usage
- **Move Validation**: Automatic validation of legal moves using the python-chess library
- **Game State Tracking**: Complete move history with visual board states
- **Web-based Interface**: Easy-to-use Streamlit application
- **Secure API Key Management**: Password-protected OpenAI API key input
__________________________________________________________________________________________________________________________________
![WhatsApp Image 2025-12-17 at 18 42 12_c4c0205a](https://github.com/user-attachments/assets/c580fed5-44db-4337-a433-07bbc020d6bf)

___________________________________________________________________________________________________________________________________

## Architecture

The application uses a multi-agent system:

- **Agent White**: GPT-4o-mini powered chess player controlling white pieces
- **Agent Black**: GPT-4o-mini powered chess player controlling black pieces
- **Game Master**: Stateless agent that validates moves and manages game state

## Prerequisites

- Python 3.8 or higher
- OpenAI API key with access to GPT-4o-mini

## Installation

1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/ai-chess-agent.git
   cd ai-chess-agent
   ```

2. Create a virtual environment:
   ```bash
   python -m venv .venv
   ```

3. Activate the virtual environment:
   - Windows: `.venv\Scripts\activate`
   - macOS/Linux: `source .venv/bin/activate`

4. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

## Usage

1. Run the Streamlit application:
   ```bash
   streamlit run ai_chess_agent.py
   ```

2. Open your browser to `http://localhost:8501`

3. Enter your OpenAI API key in the sidebar

4. Configure the maximum number of turns (recommended: 5-10 for demo purposes)

5. Click "Start Game" to begin the AI vs AI chess match

6. Watch the agents play and view the complete move history

## Configuration

- **Max Turns**: Controls the maximum number of moves in the game. Higher values allow for longer games but consume more API credits.
- **API Key**: Your OpenAI API key is required. It's stored securely in the session and not persisted.

## Dependencies

- `streamlit`: Web application framework
- `chess==1.11.1`: Chess board representation and move validation
- `autogen==0.6.1`: Multi-agent conversation framework
- `cairosvg`: SVG rendering for chess board visualization
- `pillow`: Image processing for board display

## How It Works

1. **Initialization**: Agents are configured with GPT-4o-mini and registered functions for move execution and legal move queries.

2. **Game Loop**: Agents take turns making moves through nested conversations:
   - Agent requests available legal moves
   - Agent analyzes position and selects a move
   - Game Master validates and executes the move
   - Board state is updated and visualized

3. **Termination**: Game ends when max turns are reached, checkmate occurs, or other end conditions are met.

## API Usage Warning

Playing full chess games can consume significant OpenAI API credits. The default max_turns of 5 is recommended for testing. A complete game might require 200+ turns.

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

## License

This project is open source. Please check the license file for details.

## Disclaimer

This is a demonstration of AI agents playing chess. The agents may not play perfectly and are for entertainment/educational purposes only.</content>
<parameter name="filePath">c:\Users\lucif\OneDrive\Desktop\Projects\Chess Game\README.md
