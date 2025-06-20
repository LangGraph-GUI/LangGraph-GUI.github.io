---
layout: page/note/basic
---

# LangGraph GUI Setup on Windows 

This guide will help you set up and run the LangGraph-GUI, both backend and frontend, on a Windows environment, using environment variables for backend port and Ollama URL.

### Prerequisites

Before you begin, ensure you have the following installed on your system:

- **Codebase**
- **Python or Conda**
- **npm**
- **Ollama**

## Download repos
    ```bash
    git clone --recursive https://github.com/LangGraph-GUI/LangGraph-GUI
    ```

## Ollama Setup

1. Download Ollama from official

    https://ollama.com/download

2. **Open Another PowerShell Terminal**  
    Open another PowerShell terminal window.

3. **Start Ollama**  
    Run the Ollama service:
    ```bash
       ollama serve
    ```

## Backend Setup

1. **Open a PowerShell Terminal**
    Open another PowerShell terminal window to start the setup process.

2. **Create a Conda Environment (Optional)**
    Create a new Conda environment for the LangGraph backend:
    ```bash
    conda create --name langgraph-backend python=3.11
    ```
    Activate your new environment:
    ```bash
    conda activate langgraph-backend
    ```

3. **Clone the Backend Repository**
    Clone the LangGraph backend repository from GitHub:
    ```bash
    git clone https://github.com/LangGraph-GUI/LangGraph-GUI-backend
    ```

4. **Navigate to the Backend Directory**
    Change directory to the backend project folder:
    ```bash
    cd LangGraph-GUI-backend
    ```

5. **Install Python Dependencies**
    Install the required Python packages using `pip`:
    ```bash
    pip install -r requirements.txt
    ```
6. **Start the Backend Server**  

    **Set Environment Variables**
    Before starting the backend, you need to set the following environment variables. If you skip this, the default values will be used:

    *   **BACKEND_PORT:** The port number for the backend server. (Default: 5000)
    *   **OLLAMA_BASE_URL:** The base URL for your Ollama service. (Default: `http://localhost:11434`)

    To set these variables for your PowerShell session, use:

    ```powershell
        $env:BACKEND_PORT=5000
        $env:OLLAMA_BASE_URL="http://localhost:11434"
    ```

    Run the backend server:
    ```bash
        mkdir src/workspace
    cd src/workspace
    python ../server.py
    ```

## Frontend Setup

1. **Open Another PowerShell Terminal**  
    Open a new PowerShell terminal window.

2. **Clone the Frontend Repository**  
    **frontend need dep**
    Clone the LangGraph frontend repository from GitHub:
    ```bash
        -frontend
    ```

3. **Navigate to the Frontend Directory**  
    Change directory to the frontend project folder:
    ```bash
        cd LangGraph-GUI-frontend
    ```

4. **Install Node.js Dependencies**  
    Use `npm` to install the required packages:
    ```bash
    npm install
    ```

5. **Start the Frontend Server**  
    Launch the frontend server:
    ```bash
    npm start
    ```


## Conclusion

After completing the steps above, you should have the backend and frontend servers running along with the Ollama service. You can now access the LangGraph GUI through your web browser at `http://localhost:3000`.

### Note
- Ensure all terminal windows remain open while running the servers.

