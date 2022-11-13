sequenceDiagram
Title: Loading page containing JS
browser->>server: HTTP GET request for notes
server-->>browser: sends HTML code
browser->>server: HTTP GET request for CSS
server-->>browser: sends main.css
browser->>server: HTTP GET request for JS
server-->>browser: sends main.js

    Note right of browser: browser executes js code that request JSON data from server.
    browser->>server: HTTP GET request for data.json
    server-->>browser: sends [note's data]

    Note right of browser: browser executes event handler to display note

sequenceDiagram
Title: Loading page containing JS single page application
browser->>server: HTTP POST request for notes
server-->>browser: sends JSON string

    Note right of browser: browser executes event handler to display note
