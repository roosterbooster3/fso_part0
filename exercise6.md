```mermaid
sequenceDiagram
    participant browser
    participant server

    Note over browser: User writes a note in the text field

    Note over browser: clicks the "Save" button



    Note over browser: The JS code adds new note to the internal notes list and on the page

    browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa
    activate server

    server-->>browser: HTTP status code 201 (Created)
    deactivate server

    Note over browser: The JS code receives the confirmation (or handles an error)
