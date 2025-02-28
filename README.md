# Intellibot

Intellibot is a terminal-based client for interacting with the ViewMo cloud platform. It allows users to connect to the platform using their credentials and chat with the bot through a command-line interface. And also this package let users to initialize there own RAG Agents and run them on ViewMo platform.

## Installation

To install Intellibot, run:

```sh
pip install intellibot
```

## Usage

### Connect to Intellibot

To connect to Intellibot, use the `connect` command with your username and password:

```sh 
intellibot connect --username <your-username> --password <your-password>
```

Example:

```sh 
intellibot connect --username jane@gmail.com --password pass
```

This command logs in to Intellibot and saves credentials to `credentials.json`.

### Chat with Intellibot

Once connected, you can start a chat session with the bot using the `chat` command:

```sh 
intellibot chat
```

Example:

```sh 
intellibot chat
```

This starts an interactive chat session where you can type messages and receive responses until you type "exit" or "quit".

### Initialize AI Agents

To initialize the AI agent system with a JSON configuration file, use the `initialize` command:

```sh 
intellibot initialize path/to/your/config.json
```

Example:

```sh 
intellibot initialize C:/intellihack_4.0/cli/ViewMo/config.json
```

### Check Available Projects

To list all available projects for the authenticated user, use the `projects` command:

```sh 
intellibot projects
```

Example:

```sh 
intellibot projects
```

### Execute a Project

To execute a specified project, use the `execute` command:

```sh 
intellibot execute project_name
```

Example:

```sh 
intellibot execute "Mental health chatbot researcher"
```

### View Active User Details

To display details of the authenticated user, use the `user_details` command:

```sh 
intellibot user_details
```

Example:

```sh 
intellibot user_details
```

## Development

To install the package locally for development, navigate to the root directory (where `setup.py` is located) and run:

```sh
pip install .
```

You can then use the `intellibot` CLI commands as described above to test the functionality.

## Project Structure

```sh
Intellibot/
├── intellibot/
│   ├── __init__.py
│   ├── cli.py
│   └── api.py
├── setup.py
├── README.md
├── requirements.txt
└── MANIFEST.in
```

### API Module (`api.py`)

The `api.py` module contains the `IntelliBotAPI` class, which handles connection, chat, project management, and user details functionalities.

### CLI Module (`cli.py`)

The `cli.py` module defines the command-line interface using `click`. It includes commands for connecting to the backend, chatting with the bot, initializing agents, viewing projects, executing projects, and viewing user details.

## License

This project is licensed under the Apache 2.0 License.

