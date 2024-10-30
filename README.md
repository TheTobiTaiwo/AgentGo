## README

# Agent-Based Code Generator Using Groq API

This project automates the process of generating a Python script using a multi-agent approach and the Groq API. It uses the **Llama-3.2-3b-preview** model to handle tasks such as idea generation, requirements gathering, design architecture, and code writing. The code is divided into individual agents, each responsible for a specific stage of the software development lifecycle.

## Features
1. **Idea Generation**: Generates an initial concept or idea for an app or script based on a prompt provided by the user.
2. **Requirement Gathering**: Refines and lists the key requirements based on the generated idea.
3. **Design Architecture**: Produces a high-level design outline based on the collected requirements.
4. **Code Writing**: Converts the design into actual Python code and saves it to a file.

## How It Works (Chain of Thought Breakdown)

1. **Initialization**:  
   The `Groq` client is initialized using the provided API key, which is needed to access the Llama model for chat-based completions.

2. **Idea Generation**:  
   - The `agent_idea_generator` function takes a user prompt, sends it to the Llama model, and returns a concept or idea for an app.
   - Example Prompt: "Write a python script that can generate viral tweets and LinkedIn posts."

3. **Requirement Gathering**:  
   - The `agent_requirement_gatherer` function builds on the idea by prompting the Llama model to list key requirements for the app.
   - This structured approach helps refine the idea into concrete development goals.

4. **Design Architecture**:  
   - The `agent_design_architect` function takes the app requirements and generates a high-level design or outline. This helps in visualizing how the app will be structured.

5. **Code Writing**:  
   - The `agent_code_writer` function prompts the Llama model to generate Python code based on the design outline.
   - The generated code is saved to a file named `app.py` for later use or execution.

6. **Execution Flow**:  
   The `main` function orchestrates the workflow. Starting with the idea generation, it proceeds through requirement gathering, design, and finally, the code-writing stage.

## Getting Started

### Prerequisites
- Python 3.8 or higher
- Access to the Groq API with an API key

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/agent-code-generator.git
   cd agent-code-generator
   ```

2. Install dependencies:
   ```bash
   pip install groq
   ```

3. Add your Groq API key in the script:
   ```python
   client = Groq(api_key="your_groq_api_key")
   ```

### Running the Application

To run the code generator, simply execute the `main.py` file:

```bash
python main.py
```

The generated Python script will be saved as `app.py`.

### Example Use Case

If you want to generate an app that writes viral tweets and LinkedIn posts, you can modify the initial prompt in the `main()` function:

```python
initial_prompt = "Write a python script that has the ability to write viral Tweet and linkedin post of only 200 words"
```

Upon running the script, the agents will collaborate to generate the idea, gather requirements, design the app, and write the code.

## License
This project is licensed under the MIT License.

## License

This project is open-source and available under the [MIT License](https://opensource.org/licenses/MIT).

## Security Note

Please ensure that you keep your Groq API key confidential and do not share it publicly. It's recommended to use environment variables or a secure configuration file to store sensitive information.
```

This README provides an overview of the script, its requirements, how to install and use it, its features, and some basic configuration options. You may want to customize it further based on any additional details or specific use cases for your project.
