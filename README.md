# 📝 LLM Text-to-Text Service

> ‼️This project is deprecated due to advancement of LLM eco system. To see more advancement based on current project, check our latest repo here: https://github.com/AierLab/MultiverseNote .

The **LLM Text-to-Text Service** is a wrapper that integrates third-party open-source Large Language Models (LLM) services for modular purposes. This service leverages **OLLAMA** for local deployment and provides APIs for interacting with models like **ChatGPT**, **ChatGLM**, and **JAIS** for fine-tuning and delivering text-to-text services.

## 📋 Table of Contents

- [📝 LLM Text-to-Text Service](#-llm-text-to-text-service)
  - [📋 Table of Contents](#-table-of-contents)
  - [✨ Features](#-features)
  - [📂 Directory Structure](#-directory-structure)
  - [⚙️ Installation](#️-installation)
  - [🚀 Usage](#-usage)
  - [🔗 Integration](#-integration)
  - [🔧 Configuration](#-configuration)
  - [🧪 Running Tests](#-running-tests)
  - [🤝 Contributing](#-contributing)
  - [📄 License](#-license)

## ✨ Features

- **Multiple LLM Integrations**: Supports multiple LLMs, including **OLLAMA**, **ChatGPT**, **ChatGLM**, and **JAIS**.
- **Local and Remote Deployment**: Utilizes **OLLAMA** for local deployment and various APIs for accessing and fine-tuning models remotely.
- **Modular Structure**: Designed to be easily extendable and configurable for different LLM service providers.
- **Configuration Flexibility**: YAML-based configuration allows easy customization and management of service parameters.

## 📂 Directory Structure

The repository is organized as follows:

```plaintext
llm-text2text-service/
├── src/
│   ├── control/               # Contains controllers for handling LLM-specific logic
│   ├── dao/                   # Data Access Objects for handling data interactions
│   ├── model/                 # Data models for managing LLM responses
│   ├── utils/                 # Utility functions for common operations
│   └── view/                  # Views for rendering outputs (e.g., APIs or CLI)
├── storage/
│   ├── config/                # Configuration files
│   │   └── main_config.yaml   # Main configuration file
│   └── log/                   # Log files
│       └── .gitkeep           # Keeps log directory in version control
├── tests/
│   ├── __init__.py            # Initializer for the tests package
│   └── ...                    # Test modules for various components
├── .gitignore                 # Specifies files and directories to ignore in version control
├── LICENSE                    # License file
├── main.py                    # Entry point for running the service
├── README.md                  # Project description and instructions
└── setup.py                   # Setup script for packaging and distribution
```

## ⚙️ Installation

To install the **LLM Text-to-Text Service**, follow these steps:

1. **Clone the Repository**:

   ```bash
   git clone https://github.com/your-repo/llm-text2text-service.git
   cd llm-text2text-service
   ```

2. **Install Dependencies**:

   Use `pip` to install the required dependencies:

   ```bash
   pip install -e .
   ```

## 🚀 Usage

To start the service, run:

```bash
python main.py
```

This will launch the LLM Text-to-Text Service, enabling you to interact with multiple LLMs through defined APIs or the CLI.

## 🔗 Integration

To integrate the **LLM Text-to-Text Service** into your existing project:

1. **Install the Module**:

   Install the service as a package:

   ```bash
   pip install -e /path/to/llm-text2text-service
   ```

2. **Import and Use Functions in Your Code**:

   Import the necessary bot classes or functions from the `control` module:

   ```python
   from llm_text2text_service.src.control import openaiBot, petalsBot, wenxinBot

   # Example usage with OpenAI's ChatGPT
   chatgpt_bot = openaiBot.ChatGPT()
   response = chatgpt_bot.get_response("Hello, how are you?")
   print(response)
   ```

   Replace `ChatGPT` with the specific LLM integration you wish to use, such as `PetalsAI` or `Wenxin`.

## 🔧 Configuration

The service uses a YAML configuration file located at `storage/config/main_config.yaml`. You can modify this file to configure API keys, model parameters, logging levels, and other settings.

Example configuration in `main_config.yaml`:

```yaml
openai:
  api_key: "your-openai-api-key"
wenxin:
  api_key: "your-wenxin-api-key"
logging:
  level: "INFO"
```

## 🧪 Running Tests

To run the test suite, use:

```bash
pytest tests/
```

This command will execute all test cases in the `tests` directory and provide a report of the test results.

## 🤝 Contributing

We welcome contributions from the community. Please follow these steps to contribute:

1. Fork the repository.
2. Create a new branch for your feature or bugfix.
3. Commit your changes with descriptive commit messages.
4. Push your changes to your forked repository.
5. Create a pull request with a detailed description of your changes.

## 📄 License

This project is licensed under Apache License 2.0 - see the [LICENSE](LICENSE) file for more details.

---

Thank you for your interest in the LLM Text-to-Text Service! If you have any questions or need further assistance, feel free to open an issue or contact us.
