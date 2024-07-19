# About LangGraph-GUI

[LangGraph-GUI](https://github.com/LangGraph-GUI/LangGraph-GUI) is a user-friendly interface designed for editing Node-Edge workflow graphs using LangGraph. This tool supports creating, editing, and running workflows with local language models such Ollama. It can be easily deployed using Docker Compose.

![LangGraph-GUI](/cover.webp)

## Components

LangGraph-GUI comprises the following main components:

- [**Frontend**](https://github.com/LangGraph-GUI/LangGraph-GUI-frontend): The default frontend is built with ReactFlow, providing an intuitive interface for graph editing.
  - for more info, please view [Frontend](/Frontend)
- [**Backend**](https://github.com/LangGraph-GUI/LangGraph-GUI-backend): The backend is implemented using Flask, offering a robust and scalable server-side solution.
  - for more info, please view [Backend](/Backend)
- AI-end
  - For running local language models with Ollama AI service, we recommend using NVIDIA Docker. 


## Docker COmpose
To run LangGraph-GUI using Docker Compose, refer to the detailed instructions available in the [LangGraph-GUI repository](https://github.com/LangGraph-GUI/LangGraph-GUI).

## Electron wrapper

For those who prefer a desktop application, we also provide an [Electron wrapper](https://github.com/LangGraph-GUI/LangGraph-GUI?tab=readme-ov-file#electron-wrapper).


We hope you find LangGraph-GUI useful for your workflow management needs. For more information, visit our [GitHub Discussions](https://github.com/orgs/LangGraph-GUI/discussions) page to leave any questions or feedback.
