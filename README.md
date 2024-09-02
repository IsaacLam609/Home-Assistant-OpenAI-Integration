# Home Assistant Integration with OpenAI

## Introduction
This project focuses on developing a smart home platform (Home Assistant) for a smart elderly home. The goal is to help users manage their smart home devices through the UI and voice commands while maintaining a natural conversation flow. The project uses OpenAI services for natural language processing.

## Features
- Natural language processing for conversational interactions and smart device control
- Generating and publishing a response automatically when a message is received
- Smart home device management through UI
- Fetching news from the Internet
- Communicating with other devices using protocols like MQTT
- Developers' dashboard for future development

## Usage
**Automations**
- Choose the 'edit in YAML' option after creating an automation.
- Paste the yaml code.

**Configurations**
- Install Studio Code Server add-on.
- Edit the configuration.yaml file.

**Prompts**
- Install the Extended OpenAI Conversation integration.
- Create a new service.
- Press the 'configure' button of the service and edit the prompt template.

## Architecture
- **Components:**
  - **Humanoid Robot** (or other devices): The humanoid robot which recognizes and sends users' speech.
  - **Home Assistant**: The platform for managing smart home devices.
 
- **Flow:** *text_generation* automation
  1. The humanoid publishes the recognized user message to an MQTT topic.
  2. Home Assistant processes the received message using OpenAI services.
  3. Home Assistant controls the corresponding smart home devices (if necessary).
  4. Home Assistant publishes the response to an MQTT topic.

## Acknowledgements
- [Home Assistant documentation](https://www.home-assistant.io/docs/)
- [Extended OpenAI Conversation integration](https://github.com/jekalmin/extended_openai_conversation/tree/main/examples/function)
