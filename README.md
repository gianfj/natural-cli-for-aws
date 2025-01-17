# AWS CLI via OpenAI

## Overview
This project integrates OpenAI’s GPT capabilities with AWS CLI, enabling users to interact with AWS services using natural language prompts. The tool translates user-friendly prompts into actionable AWS CLI commands and executes them seamlessly.

## Features
- **Natural Language Processing**: Leverage OpenAI’s GPT model to interpret user commands.
- **AWS CLI Integration**: Automatically execute AWS CLI commands based on generated outputs.
- **Error Handling**: Includes checks to ensure environment variables and dependencies are properly configured.

## Prerequisites

Before running the script, ensure the following dependencies and environment variables are set up:

### Dependencies
1. Python 3.8 or newer
2. `openai` Python package
3. AWS CLI configured with valid credentials
4. `pyenv` for managing Python versions (optional but recommended)

### Environment Variables
- **OPENAI_API_KEY**: Your OpenAI API key.
- **AWS credentials**: Ensure `~/.aws/credentials` is configured correctly.

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/<your-username>/<repo-name>.git
   cd <repo-name>
   ```

2. Set up a virtual environment (optional but recommended):
   ```bash
   python3 -m venv venv
   source venv/bin/activate
   ```

3. Install required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

4. Set the necessary environment variables:
   ```bash
   export OPENAI_API_KEY="your-openai-api-key"
   ```

## Usage

1. Run the script:
   ```bash
   python aaws.py
   ```

2. Enter natural language prompts to interact with AWS services. For example:
   ```
   Create an S3 bucket named "my-bucket"
   ```

3. The tool will:
   - Interpret your prompt using OpenAI’s GPT model.
   - Translate it into an AWS CLI command.
   - Execute the command and display the results.

## Example

**Input**:
```
List all EC2 instances in the us-east-1 region.
```

**Output**:
```bash
aws ec2 describe-instances --region us-east-1
```

**Result**:
Displays the list of EC2 instances.

## Troubleshooting

1. **Missing API Key**:
   Ensure the `OPENAI_API_KEY` environment variable is set correctly.

2. **AWS CLI Errors**:
   Verify AWS credentials and CLI configuration using:
   ```bash
   aws configure
   ```

3. **Dependency Issues**:
   Reinstall dependencies using:
   ```bash
   pip install -r requirements.txt
   ```

## Contributing

Contributions are welcome! Please follow these steps:
1. Fork the repository.
2. Create a new branch:
   ```bash
   git checkout -b feature-branch-name
   ```
3. Make your changes and test them thoroughly.
4. Submit a pull request with a detailed description of your changes.

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.

## Acknowledgments

- [OpenAI](https://openai.com) for the GPT model
- [AWS](https://aws.amazon.com) for the CLI tools


