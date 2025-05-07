# 📄 Design Analysis – TeeBridge

## What Is It?

`TeeBridge` is a Python class that lets you send printed output to two places at once:
1. The screen (like normal)
2. A file (to save what was printed)

It works like the `tee` command in Linux.

---

## How Does It Work?

- You create a `TeeBridge` object and pass in:
  - The original output stream (`sys.stdout` or `sys.stderr`)
  - A file or any other writable stream

- Then, you replace `sys.stdout` with your `TeeBridge` object.
- After that, everything you `print()` goes to both the screen and the file.

---

## What’s In the Code?

### `__init__(self, original_stream, additional_stream)`
- Sets up the two places where the output should go.

### `write(self, data)`
- Sends the printed data to both the screen and the file.

### `flush(self)`
- Makes sure everything gets written out right away.

### `close(self)`
- Closes the file (does not close the screen output).

---

## Why It’s Useful

- Lets you see output in the terminal and save it at the same time.
- Great for CTFs, hacking scripts, or debugging tools.
- Very lightweight — no extra packages needed.

---

## Limitations

- Not made for multi-threaded use.
- You must manually reset `sys.stdout` when you're done.
- Doesn’t support `with` statements (but could be improved to do that).

---
