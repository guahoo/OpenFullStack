sequenceDiagram
    participant browser
    participant server

    browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note
    note=test2
    activate server
    server-->>browser: 302, Accept
    deactivate server

    browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/data.json
    activate server
    server-->>browser: [{content: "hgjgh", date: "2025-02-26T03:47:57.408Z"}...]
    deactivate server
