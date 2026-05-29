# Notes App

> Academic project — IU5-24B, Bauman Moscow State Technical University

A desktop notes application written in C++ with a GTK 3 interface. Notes are analyzed automatically to extract a scheduled notification time and estimate the emotional tone of the text.

## Features

- Create, edit, and delete notes with timestamps
- Automatic parameter extraction via neural network processing:
  - Notification time detection
  - Emotional tone analysis
- Persistent storage — notes saved to disk and reloaded on startup
- Desktop notifications via the Windows notification API

## Design Patterns

The project demonstrates several OOP and design pattern concepts:
- **Singleton** — `NoteApp` instance
- **Command** — `AddNoteCommand`, `DeleteNoteCommand`, `EditNoteCommand`, `SaveNoteCommand`
- **Proxy** — `NoteSaverProxy` wraps disk I/O

## Tech Stack

- C++17, GTK 3 (`gtk+-3.0`)
- CMake build system
- Windows API for notifications
- CLion IDE

## Build

**Requirements:** CMake 3.10+, GTK 3 development libraries.

```bash
mkdir build && cd build
cmake ..
make
./NoteApp
```

## Authors

Kirill Yurchenko, Pavel Kuznetsov — group IU5-24B
