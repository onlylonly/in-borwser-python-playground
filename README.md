# Python Playground - In-Browser Python IDE

A simple, in-browser Python 3 IDE built using Pyodide and CodeMirror.  Write, run, and experiment with Python code directly in your web browser!  Includes the ability to install packages and get AI help.

## Features

*   **Code Editor:**  Powered by CodeMirror for syntax highlighting, line numbers, and bracket matching.
*   **Python 3 Execution:** Runs Python code using Pyodide, a WebAssembly port of CPython.
*   **Package Installation:** Install popular Python packages directly in the browser using `micropip`.
*   **Output Display:**  Displays the output of your Python code in a dedicated output window.
*   **AI Assistant:**  Ask an AI for help with your code, errors, and understanding Python concepts.  Uses streaming responses for a more interactive experience.
*   **Package Management:** Install and manage Python packages easily using a text input area.
*   **Clean UI:**  A user-friendly interface with collapsible panels for package management.
*   **Examples:** The editor starts with a basic "Hello, Python World!" example.

## How it Works

This project leverages the following technologies:

*   **Pyodide:**  A Python distribution for the browser, built on WebAssembly.  Allows running Python code within a web worker.
*   **CodeMirror:** A versatile text editor implemented in JavaScript for in-browser code editing with syntax highlighting.
*   **Web Workers:**  Offload Python execution to a background thread, preventing the UI from freezing during long-running processes.
*   **HTML, CSS, JavaScript:** The core technologies for building the user interface and handling interactions.
*   **OpenAI (optional):**  Provides AI assistance via an API.  Requires an API key to be configured.  The code is designed to be compatible with other OpenAI-compatible API endpoints.

## Getting Started

Simply open the `index.html` file in your web browser. No server or installation is required!

## Usage

1.  **Code Editing:** Write your Python 3 code in the editor.
2.  **Package Installation (Optional):** In the "Python Packages" panel, enter the names of the packages you want to install (one package per line) and click "Install Packages".
3.  **Run Code:** Click the "Run Code" button to execute your code. The output will be displayed in the "Output" window.
4.  **Stop Execution:**  Click the "Stop Execution" button to halt a running script.  Note: This restarts the Pyodide worker.
5.  **Clear Output:** Click the "Clear Output" button to clear the output window.
6.  **AI Assistant (Optional):**
    *   Click "Ask AI for Help" to get assistance with your code.
    *   **API Key Required:**  You'll need to provide a valid OpenAI-compatible API key (e.g., from OpenAI, Azure OpenAI) in the settings panel.  This is stored locally in your browser's local storage.
    *   Ask follow-up questions in the chat input area.
7.  **Packages Panel:** The packages panel can be collapsed and expanded using the arrow icon in the panel header.

## Author

Liew (From PulseSecure)

## License

This project is open source and available under the [AGPL 3.0 License](LICENSE).

## Contributing

Contributions are welcome! Please feel free to submit pull requests or open issues.


## Notes

*   This is a client-side application, so all code execution and package installation happens within the browser.
*   The performance of the IDE may be limited by the browser's capabilities and the speed of WebAssembly execution.
*   The AI assistant relies on an external API and requires an API key.  Usage may incur costs depending on the API provider.
*   API Key is saved in localStorage.
