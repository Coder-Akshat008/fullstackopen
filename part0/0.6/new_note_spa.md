# 0.6: New note in Single Page App

```mermaid
sequenceDiagram
    participant browser
    participant server

    Note right of browser: User writes a note and clicks Save

    Note right of browser: JavaScript prevents normal form submission

    browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa
    activate server
    server-->>browser: JSON response confirming saved note
    deactivate server

    Note right of browser: JavaScript adds the new note to the page
