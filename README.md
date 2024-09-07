# CLI-based-Chat-tool
# CLI Chatbot

This project is a simple Command-Line Interface (CLI) chatbot designed using Python. It processes user input, matches it against predefined responses stored in a JSON file, and returns the appropriate response. If no matching response is found, the bot will return a random response.

## Features
- **Natural language processing**: The chatbot uses regular expressions to process and understand user input.
- **Customizable responses**: The bot responses are stored in a JSON file, making it easy to customize and add more responses.
- **Random fallback**: When no response matches the user input, the bot provides a random response from a predefined set of phrases.
- **CLI Interface**: Users can interact with the bot through the command-line interface.

## How it works
1. The chatbot loads a JSON file (`bot.json`) containing possible user inputs, required words, and corresponding bot responses.
2. The user input is split into words using regular expressions.
3. The bot checks if the input contains any required words (if defined).
4. It calculates a score based on the number of matching words in the input.
5. The bot responds with the answer that has the highest score. If no good response is found, it returns a random response.

## Prerequisites
- Python 3.x
- A JSON file containing chatbot responses in the following format:

```json
[
    {
        "user_input": ["hi", "hello", "hey"],
        "bot_response": "Hello! How can I help you today?",
        "required_words": []
    },
    {
        "user_input": ["bye", "goodbye"],
        "bot_response": "Bye, See you later!",
        "required_words": []
    }
]
## Customizing Responses
To add or modify the bot's responses, follow these steps:

1. Open the `bot.json` file.
2. Add new `user_input` phrases, `bot_response`, and optionally, `required_words` that must appear in the user's input for a valid match.

### Example of a JSON entry:
```json
{
    "user_input": ["what", "your", "name"],
    "bot_response": "I'm a simple chatbot created to respond to your queries.",
    "required_words": ["name"]
}

