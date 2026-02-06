# Pirate Context-Aware Chatbot

A stateful, persona-driven chatbot that speaks exclusively in 17th-century pirate slang using the OpenAI API.

## Project Overview

This project implements a context-aware chatbot with a pirate persona that:
- Maintains a consistent pirate character throughout conversations
- Remembers user details across conversation turns
- Manages conversation history to prevent token overflow
- Handles API errors gracefully

## Features

- **Pirate Persona**: The chatbot speaks exclusively in authentic 17th-century pirate slang and maintains its character regardless of user input
- **State Management**: Conversation history is stored in a Python list to maintain context across turns
- **Context Window Management**: Automatically removes older messages when the history gets too long, while preserving the system message
- **Error Handling**: Gracefully handles API errors with pirate-themed messages

## Requirements

- Python 3.6+
- OpenAI API key
- `openai` Python package


### Jupyter Notebook

You can also use the Jupyter notebook version:
1. Open `pirate_chatbot.ipynb` in Jupyter or Google Colab
2. Run the cells in order
3. Enter your OpenAI API key when prompted
4. Interact with the pirate chatbot in the final cell

## How It Works

1. The system initializes with a pirate persona defined in the system message
2. User inputs are added to the conversation history
3. The full conversation history is sent to the OpenAI API
4. The API response is displayed and added to the conversation history
5. If the conversation history exceeds 10 messages, the oldest user and assistant messages are removed to prevent token overflow

## Example Conversation

```
Ahoy! Ye be chattin' with a fearsome pirate! (Type 'exit' to end)
You: Hello, what's your name?
Pirate: Arr! The name be Captain Blackbeard, the most feared pirate to ever sail the seven seas! Me real name ain't for the likes of landlubbers to be knowin'. What be yer name, ye scurvy dog? Be ye friend or foe of me fearsome crew?

You: My name is Alex
Pirate: Ahoy there, Alex! Welcome aboard me mighty vessel! 'Tis a pleasure to make yer acquaintance on these treacherous waters. Any friend o' the sea be a friend o' Captain Blackbeard, unless ye be after me treasure! *spits and adjusts eye patch* What brings ye to these parts, young Alex? Be ye searchin' for adventure or runnin' from the King's Navy?
```

## License

MIT License

## Acknowledgments

- OpenAI for providing the API
- The Golden Age of Piracy for the colorful language inspiration

---
