# LangGraph-GUI

The core file that convert json to LangGraph is [/src/WorkFlow.py](https://github.com/LangGraph-GUI/LangGraph-GUI-backend/blob/main/src/WorkFlow.py)

[llm.py](https://github.com/LangGraph-GUI/LangGraph-GUI-backend/blob/main/src/llm.py) demo how to replace to different LLM services.

## Json Format

It will be subgraphs.

for each subgraph, contain graph_name, graph_nodes, graph_serial_number

you can put anything at ext

```
[
  {
    "name": "root",
    "nodes": [
      {
        "uniq_id": "1",
        "type": "STEP",
        "name": "Node 1",
        "description": "",
        "tool": "",
        "nexts": [],
        "true_next": null,
        "false_next": null,
        "ext": {
          "pos_x": 420,
          "pos_y": 60,
          "width": 150,
          "height": 200,
          "info": null
        }
      }
    ],
    "serial_number": 2
  }
]
```


This use FastAPI server to communicate with frontend.

Current implementation only runs graph.json.

## multi user support
if you use [nginx.conf](https://github.com/LangGraph-GUI/LangGraph-GUI/blob/main/nginx/nginx.conf)

that different user will working at each own sub folder

and each user will run it's own subprocess.


*For a beginner-friendly introduction to LangGraph, visit [LangGraph-learn](https://github.com/LangGraph-GUI/LangGraph-learn).*


