# Interactive-ELIZA
Step back to 1966 with this interactive ELIZA web app, simulating Joseph Weizenbaum’s historic AI psychotherapist. Built with pure JavaScript, it transforms user input into Rogerian reflective questions using classic pattern matching and pronoun reflection. Features a retro CRT green-screen mode, a real-time logic inspector, and voice tools.
ELIZA — Rogerian Psychotherapist (1966 Simulation)
An interactive, single-file web application simulating ELIZA, the pioneering Natural Language Processing (NLP) computer program created by Joseph Weizenbaum at the MIT Artificial Intelligence Laboratory between 1964 and 1966.
This implementation emulates the famous DOCTOR script, which mimics a Rogerian psychotherapist by reflecting patient statements back as open-ended questions without applying genuine intelligence or understanding.
🌟 Key Features
🧠 Pattern Matching & NLP Logic Engine
Keyword Decomposition: Uses regular expressions to match user statements against a prioritized hierarchy of emotional, relational, and contextual triggers (e.g., family, mother, father, feel, sad, depressed, remember, dream, think, computer).
Pronoun Reflection Mapping: Transforms point-of-view pronouns safely on tokenized inputs (e.g., "my mother" \rightarrow "your mother", "I am" \rightarrow "you are", "me" \rightarrow "you").
Rogerian Response Synthesis: Combines reflected fragments with classic non-directive response templates.
Memory Buffer: Caches significant user topics and periodically weaves them back into conversation when no pattern matches occur.
Fallback Pool: Handles unrecognized inputs with open-ended conversational prompts.
💻 UI & User Experience
Live Logic Inspector: A real-time sidebar breaking down the internal state of ELIZA for every turn—showing raw text, detected keywords, extracted regex groups, pronoun transformations, and chosen template strategies.
Dual Visual Themes:
Modern Theme: Clean, clinical, and responsive design built with Tailwind CSS.
CRT Terminal Mode: Retro 1960s green-phosphor display complete with scanlines, CRT glow, and monospace styling.
Voice Capabilities: Integrated Web Speech API for optional Text-to-Speech (reading responses aloud) and Speech-to-Text (voice input).
Session Tools: Quick prompt suggestion chips, live message counters, chat reset options, and raw text session transcript export.
🚀 Getting Started
Because ELIZA is built as a self-contained, single-file web application (index.html), no setup, installation, or build tools are required.
Quick Run
Download or clone the repository.
Double-click index.html or open it directly in any modern web browser (Chrome, Firefox, Safari, Edge).
🛠️ Tech Stack
HTML5: Semantic markup structure.
CSS3 / Tailwind CSS: Utility-first styling with custom CSS variables for CRT scanlines and glowing animations.
Vanilla JavaScript (ES6+): Complete logic engine with zero external framework dependencies.
FontAwesome & Google Fonts: Visual icons (Inter and Fira Code typography).
📐 How the Logic Engine Works
The core interaction follows a 4-step pipeline for every user input:
[ User Input ] 
      │
      ▼
[ 1. Pattern Matching ] ───► Evaluates input against Regex keyword matrix
      │
      ▼
[ 2. Key Extraction ]  ───► Extracts captured segment $1 from regex match
      │
      ▼
[ 3. Pronoun Swap ]    ───► Map pronouns (I -> you, my -> your, etc.)
      │
      ▼
[ 4. Template Substitute ] ► Inserts reflected phrase into selected template
Example Transformation:
Input: "I feel sad when I think about my mother."
Matched Trigger: family / mother
Extracted Fragment: "my mother"
Pronoun Reflection: "your mother"
Template Applied: "Tell me more about {ref}."
Output: "Tell me more about your mother."
📜 License & Historical Context
This project is an educational recreation inspired by Joseph Weizenbaum's original 1966 paper:
"ELIZA—A Computer Program For the Study of Natural Language Communication Between Man and Machine."
