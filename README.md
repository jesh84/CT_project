# Tee Bridge

This is a simple Python program that connects two data streams — like input and output — and lets you send and receive messages through them. It can be used for connecting things like serial ports, network sockets, or other types of communication interfaces.

## What It Does

The script sets up a **tee bridge**, which:
- Reads data from one input.
- Sends it to multiple outputs (like a tee pipe in plumbing).
- Also works in the opposite direction if needed.

This can be useful for logging, debugging, or controlling devices.

## Features

- Handles input and output in real time.
- Works with threads to keep everything running smoothly.
- Can stop safely using signals like Ctrl+C.

## Requirements

- Python 3.x

You don't need to install any extra libraries — it only uses built-in Python modules.

## How to Use

Run the script with:

```bash
python main.py
