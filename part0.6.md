```mermaid
sequenceDiagram
participant server
participant browser
browser-->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa
note left to browser At this point the browser reloads just the json with content refreshed, not doing more GET requests.
activate server
server-->>browser: {"message":"note created"}
deactivate server
```
