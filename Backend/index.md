# LangGraph-GUI

The core file that convert json to LangGraph is [/src/WorkFlow.py](https://github.com/LangGraph-GUI/LangGraph-GUI-backend/blob/main/src/WorkFlow.py)

[llm.py](https://github.com/LangGraph-GUI/LangGraph-GUI-backend/blob/main/src/llm.py) demo how to replace to different LLM services.

## Json Format

json node format like this:
you can extend ext to put your data, this is elastic design.
for example, the ext.info is a ext and able to parse in our backend.
```
{
  "nodes": [
    {
      "uniq_id": "1",
      "nexts": [
        "2"
      ],
      "type": "START",
      "name": "Node 1",
      "description": "",
      "tool": "",
      "true_next": null,
      "false_next": null,
      "ext": {
        "pos_x": 126,
        "pos_y": 146,
        "width": 200,
        "height": 200,
        "info": ""
      }
    },
```


This use FastAPI server to communicate with frontend.

Current implementation only runs graph.json.

## multi user support
if you use [nginx.conf](https://github.com/LangGraph-GUI/LangGraph-GUI/blob/main/nginx/nginx.conf)

that different user will working at each own sub folder

and each user will run it's own subprocess.


*For a beginner-friendly introduction to LangGraph, visit [LangGraph-learn](https://github.com/LangGraph-GUI/LangGraph-learn).*


