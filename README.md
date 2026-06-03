# Mini GUI Terminal

A simple graphical terminal application built with **C++** and **GTKMM**. It allows users to execute shell commands through a graphical interface and view the output in a scrollable window.

## Features

- Graphical terminal interface
- Execute shell commands
- Scrollable output display
- Simple and lightweight design
- Built with C++ and GTKMM

---

## Requirements

- C++17 or later
- GTKMM 3.x
- GCC/G++ Compiler
- MSYS2 (Windows)

---

## Installation

### 1. Install MSYS2

Download and install MSYS2:

https://www.msys2.org/

### 2. Update Packages

Open **MSYS2 UCRT64** and run:

```bash
pacman -Syu
```

### 3. Install GTKMM

```bash
pacman -S mingw-w64-ucrt-x86_64-gtkmm3
```

### 4. Verify Installation

```bash
pkg-config --modversion gtkmm-3.0
```

---

## Build

Navigate to the project directory:

```bash
cd /c/path/to/project
```

Compile the application:

```bash
g++ gui_terminal.cpp -o terminal_app $(pkg-config --cflags --libs gtkmm-3.0)
```

---

## Run

```bash
./terminal_app
```

---

## Usage

1. Enter a command in the input field.
2. Click the **Run** button.
3. View the output in the terminal window.

### Example

Input:

```bash
echo Hello World
```

Output:

```text
>>> echo Hello World
Hello World
```

---

## Project Structure

```text
.
├── gui_terminal.cpp
└── README.md
```

---

## Technologies Used

- C++
- GTKMM
- GCC / G++
- MSYS2

---

## How It Works

The application uses:

- `Gtk::Entry` for command input
- `Gtk::Button` to trigger command execution
- `Gtk::TextView` to display command output
- `Gtk::ScrolledWindow` for scrolling

Commands are executed using:

```cpp
popen()
```

The output is captured and displayed inside the GUI.

---

## Limitations

- Commands run synchronously
- Long-running commands may freeze the UI
- No command history
- No interactive shell support
- Output is not persisted between sessions

---

## Future Enhancements

- Command history
- Asynchronous execution
- Dark/Light themes
- Keyboard shortcuts
- Save output to file
- Interactive terminal support

---

## License

This project is licensed under the MIT License.

---

## Author

**Nishidhx**

Software Engineer | Open Source Learner