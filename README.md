# OpenAI CHATGPT API Experiments

## Introduction
This repository contains a Jupyter notebook designed to experiment with OpenAI's CHATGPT API. The notebook explores different ways to structure and prompt the model to achieve specific tasks, such as classifying customer service queries into primary and secondary categories.

## Requirements

### Prerequisites
1. **Python Environment**: The code is written in Python and requires a Python 3.x environment.
2. **Python Libraries**: Ensure you have the following libraries installed in your system:
   - `os`
   - `openai`
   - `tiktoken`
   - `dotenv`
3. **OpenAI API Key**: You'll need an API key from OpenAI to interact with the service. Store it securely in an `.env` file or another secure location and make sure it's accessible to the notebook.

## Code Explanation

### Setup and Initialization
- **Library Imports**: The necessary Python libraries for the code's operation are imported.
- **Environment Variable Loading**: The code uses `dotenv` to load essential environment variables, particularly the OpenAI API key.

### Function Definitions
1. `get_completion_from_messages(messages, model="gpt-3.5-turbo", temperature=0, max_tokens=500)`: This function is designed to send a series of messages to the OpenAI model and receive a structured response. It takes into account:
    - `messages`:  A list of message objects containing a role (either "system" or "user") and content (the actual message).
    - `model`:  The OpenAI model to use (default is "gpt-3.5-turbo").
    - `temperature`: Adjusts the randomness of the model's output.
    - `max_tokens`: Limits the length of the model's response.
### Experiment with structured Prompts
- The notebook demonstrates how to use a structured system message to guide the model's behavior. In this case, the system message instructs the model to classify customer service queries into primary and secondary categories.
- Two examples are provided:
  1.1 A user query about deleting a profile, which the model should classify.
  1.2 A user query seeking information about flat screen TVs, which the model should also classify.
By using a consistent system message and structuring user queries with a specific delimiter, the notebook aims to obtain consistent and accurate classifications from the model.

## Usage Tips
- The `system_message` provides the model with context and instructions. Adjusting this message can lead to different model behaviors.
- The `delimiter` is used to clearly indicate the beginning and end of a user query. Ensure that user messages are properly delimited for accurate model responses.
- Feel free to experiment with different user queries and observe how the model classifies them based on the provided system message.
