# Liore 🤖

<div align="center">
  <img src="./docs/static/img/liore_banner.jpg" alt="Liore Banner" width="100%" />
</div>

## Overview
**Liore** is a conversational AI framework inspired by the classic Eliza framework. Liore allows you to create custom characters that can engage in personalized dialogues, tailored to specific personalities and behaviors. This project extends the original Eliza model by enabling developers to define custom characters and feed them specific data to improve their responses.
## Key Features

- **Custom Character Creation**: Create characters with unique personalities and conversational patterns.
- **Data Feeding**: Feed characters with external or predefined data to make conversations more intelligent and contextually aware.
- **Extensible and Flexible**: Liore is built to be easily extendable, allowing you to add more characters, features, and integrations as needed.

## How It Works

### 1. Create a Custom Character

To create a custom character, you can define its:
- **Personality**: This includes the greetings, default responses, and any specific behaviors that make the character unique.
- **Behavioral Data**: You can feed your character with specific topics, behaviors, or knowledge that guide its responses.

Example of a custom character:

```javascript
const LioreCharacter = new LioreCharacter({
  name: 'Techie',
  personality: {
    greetings: ['Hello, fellow coder!', 'Greetings, developer!'],
    responses: {
      "What is JavaScript?": "JavaScript is a programming language used for web development.",
      "Tell me about coding": "Coding is like solving puzzles. It's an art and a science!"
    }
  },
  data: {
    interests: ['technology', 'programming', 'web development']
  }
});
```

### 2. Feeding the Character with Data

Feeding data into Liore characters allows you to enhance their conversational abilities. You can add information such as favorite topics, recurring phrases, and more.

```javascript
LioreCharacter.feedData({
  techUpdates: [
    "Did you hear about the new version of Node.js?",
    "JavaScript has evolved a lot. ES6 is my favorite!"
  ],
  mood: "excited"
});
```

### 3. Interaction with the Character

Once you've created and fed your character data, you can start interacting with it. The character will use the personality and data you've defined to respond intelligently.

```javascript
// Start a conversation with the custom character
LioreCharacter.say("What is JavaScript?");
```

Output:
```
Techie: JavaScript is a programming language used for web development.
```

### 4. Extending the Framework

Liore is built to be flexible and easy to extend. You can add new characters, new features, or even integrate with machine learning models and external APIs. Want to create a more complex character? No problem! Liore provides you with all the tools you need to build powerful conversational agents.

## Installation

To get started, clone this repository and install the required dependencies:

```bash
git clone https://github.com/liore-ai/liore.git
cd liore
npm install
```

## Usage

Once you've installed Liore, you can begin creating and interacting with characters in your own projects:

```javascript
const { LioreCharacter } = require('liore-framework');

const character = new LioreCharacter({
  name: 'MysteryBot',
  personality: {
    greetings: ['Welcome, traveler...', 'Ah, a new face. Welcome.'],
    responses: {
      "Who are you?": "I am the keeper of mysteries.",
      "Tell me something strange": "I once saw a cat speak in riddles."
    }
  },
  data: {
    interests: ['mysteries', 'cryptic tales']
  }
});

character.say("Who are you?");
```

## Contributing

We welcome contributions to this project! If you have ideas for new features, character templates, or improvements, please open an issue or submit a pull request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Follow Us

Stay updated on the latest development and news!

- Twitter: [@lioreai_](https://x.com/lioreai_)