# Simple File Server

This project provides a simple file server with optional authentication, logging, and HTTPS support. It uses Python's built-in HTTP server and the `click` library for command-line interface options.

## Features

- Serve files from a specified directory.
- Bind to a specific host and port.
- Optional basic authentication.
- Optional logging to a file.
- Optional HTTPS support.

## Requirements

- Python 3.6 or later
- `click` library

## Installation

You have two choices for installation:

- Install from pip (Recommended)
  - `pip install fileserve`
- Install from git
    1. Clone the repository:
    ```sh
    git clone https://github.com/avycado13/fileserve
    ```
    2. Go into the dir
    ```sh
    cd fileserve
    ```

    3. Install the project:
    ```sh
    pip install [-e] fileserve
    ```

## Usage

Run the server using the following command:

```sh
fileserve
```

## Options

- `--bind`: Specify the host and port to bind to (default: localhost:8000).
- `--directory`: Specify the directory to serve files from (default: /).
- `--auth`: Enable basic authentication.
- `--log`: Enable logging to server.log.
- `--https`: Enable HTTPS (requires server.crt and server.key files).

## HTTPS

To use HTTPS, you need to have server.crt and server.key files in the root directory. You can create self-signed certificates for testing purposes using OpenSSL:

```sh
openssl req -new -x509 -keyout server.key -out server.crt -days 365 -nodes
```
