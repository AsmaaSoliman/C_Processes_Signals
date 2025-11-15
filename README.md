https://github.com/AsmaaSoliman/C_Processes_Signals/releases

![Release badge](https://img.shields.io/github/v/release/AsmaaSoliman/C_Processes_Signals.svg)

# C Process Signals: OS Exercises in C, Concurrency and Data

Overview
- These exercises were done as part of the Operating Systems course during my bachelor studies in Computer Science and Engineering at the University of Catania.
- The work explores core OS ideas through C programs. It focuses on processes, signals, synchronization, and inter-process communication.
- The set includes practical demonstrations of how processes interact, how signals are delivered and handled, and how to coordinate work using concurrency primitives.
- The repository aligns with topics in algorithms, C programming, concurrent programming, data structures, debugging, English-language documentation, Git, GitHub, imperative programming, Markdown, and project management.

What you will learn
- How to create and manage processes in Linux using C.
- How signals work at the OS level and how to handle them safely in user space.
- How to synchronize work across processes and threads.
- How to implement data structures that support OS-style tasks, such as queues and linked lists.
- How to debug and reason about concurrent code with clear, well-documented examples.
- How to write clear English documentation for technical projects.
- How to manage a project using Git and GitHub workflows.

Repository topics
- algorithms, c, concurrent-programming, data-structures, debugging, english-language, git, github, imperative-programming, markdown, project-management

Downloads and releases
- The assets for this project are published in the Releases section of the repository. From the Releases page you can download the prepared binaries or source archives and run them on a suitable Linux environment. For convenience, download the release asset that matches your system, then execute the included binary or build from the source as described in the Getting started guide.
- If you want to review the exact assets before downloading, visit the Releases page at the following link: https://github.com/AsmaaSoliman/C_Processes_Signals/releases

Table of contents
- Quick start
- Project structure
- How to run locally
- Programs and modules
- Algorithms and data structures
- Concurrency and signals
- Debugging and testing
- Documentation and style
- Development workflow
- Release assets
- License
- Acknowledgements

Quick start
- Prerequisites: a Linux environment, GCC or Clang, and Make.
- Step 1: Get the code. Open a terminal and clone the repository or download the archive from the Releases page.
- Step 2: Build. Use the provided build system if present, otherwise compile the sources with a standard C compiler.
- Step 3: Run. Execute the programs with their required arguments to observe process creation, signaling, and synchronization in action.
- Step 4: Explore. Read the documentation in the repository to understand how each example works and what it demonstrates about OS behavior.

Project structure
- src/ - Core C sources that implement the exercises.
- include/ - Header files with public interfaces used across the projects.
- tests/ - Small test harnesses and verification scripts for the exercises.
- docs/ - Expanded explanations, diagrams, and design notes.
- examples/ - Ready-to-run usage demonstrations showing typical scenarios.
- assets/ - Supporting files for assets used by the exercises.
- scripts/ - Helpful utilities to automate building, testing, and running samples.
- README.md - This document, which explains the project and how to use it.

How to run locally
Prerequisites
- A modern Linux system with POSIX APIs.
- GCC (version 9 or newer recommended) or Clang.
- Make (optional if you use a direct compiler command).
- A standard C library with pthreads support.

Build and run options
- If a Makefile exists, simply run:
  - make
  - make test (if tests are provided)
  - make clean
- If there is no Makefile, compile individual sources with a typical command, for example:
  - gcc -Wall -Wextra -pthread -o program src/program.c
  - ./program
- Some examples require linking with math or other libraries; adjust linker flags as needed:
  - gcc -Wall -Wextra -pthread -lm -o program src/main.c

Running examples
- Each example demonstrates a specific OS concept. Typical usage looks like:
  - ./program [ARGS]
- Common arguments include:
  - --init: initialize resources
  - --run: start the demonstration
  - --signal SIGINT: specify how the program should respond to a signal
- Outputs show process IDs, signal delivery, and synchronization events, giving a concrete view of OS internals.

Program and module overview
- Process creation and lifecycle: Demonstrations of fork(), exec(), and wait() semantics, including how a parent and child interact.
- Signal handling: Plain handlers, blocking signals, and the effect of signals on process groups and sessions.
- Inter-process communication (IPC): Pipes, named pipes (FIFOs), and simple shared data exchanges to illustrate data flow between processes.
- Concurrency primitives: Pthreads where used, including mutexes, condition variables, and barrier-like coordination.
- Data structures: Implementations of dynamic arrays, singly and doubly linked lists, and simple queues to manage tasks and messages.
- Debugging aids: Built-in logging, assertions, and hooks to enable easier tracing of events during runs.
- Documentation quality: All code is documented in clear English with inline comments and external docs that explain the design choices.

Algorithms and data structures
- Sorting and searching within small data sets to illustrate typical algorithmic thinking in OS tasks.
- Queue management for task scheduling and message passing.
- Linked lists used to maintain dynamic process tables or resource trackers.
- Simple hash-like collections for quick lookups in demonstrations that simulate resource tracking.

Concurrency and signals
- Signals as asynchronous events: how signals interrupt execution and what it takes to handle them safely.
- Signal-safe programming practices: minimal work inside signal handlers, deferring heavy processing to main loops.
- Race condition awareness: examples show how improper synchronization can lead to data corruption or unexpected behavior.
- Process coordination: parent-child collaboration, shared resource access, and synchronized termination.

Debugging and testing
- Command-line tracing: how to observe process creation, signal delivery, and inter-process communication.
- Debugging tools: gdb for stepping through code, strace for tracing system calls, and valgrind for memory checks.
- Test strategies: small, deterministic tests that verify behavior for common scenarios and edge cases.
- Reproducibility: instructions to reproduce a failing case by controlling timing with sleeps or deliberate delays.

Documentation and style
- Documentation aims for clarity and accessibility. The English used is precise and straightforward.
- Inline comments explain why decisions were made, not just what the code does.
- Public interfaces are documented with input, output, and expected behavior.
- Code style follows a consistent pattern for readability, with simple constructs and minimal complexity.

Development workflow
- Branching: work on features or experiments in separate branches and merge after review.
- Commits: small, focused commits that explain the change and its intent.
- Reviews: seek feedback on design decisions, edge cases, and potential pitfalls.
- CI: where available, run automated tests to verify correctness and stability across changes.

Release assets
- The official release assets are available in the Releases section of the repository. To obtain the latest stable version, open the Releases page and download the appropriate archive or binary for your system. After downloading, extract and run the binaries as described in the Getting started section.
- From the Releases page you can download the prepared assets and run them on a compatible Linux system. If you want to verify the exact assets before downloading, revisit the same Releases page at https://github.com/AsmaaSoliman/C_Processes_Signals/releases

Contributing
- You can contribute by adding new exercises, improving documentation, and refining the examples.
- Start by opening an issue to discuss a feature or fix. Then create a branch for your work and a pull request with a concise description.
- Follow the project’s style guide for C code, add tests for new features, and document any new behavior clearly.

Code style and conventions
- Use clear, direct language in documentation and comments.
- Favor explicit over implicit behavior. Name functions and variables clearly.
- Keep functions small and focused on a single responsibility.
- Use defensive checks for pointers and system calls.
- Prefer simple data structures for clarity unless a complex structure is necessary.

File and directory conventions
- src/: Core logic and OS-related demonstrations.
- include/: Public headers for the modules.
- tests/: Small unit and integration tests.
- docs/: Explanations, diagrams, and extended notes.
- examples/: Ready-to-run demonstrations for users.
- assets/: Release-related files and resources.
- scripts/: Helpers for build, test, and run tasks.

Usage scenarios
- Student exploration: A learner can study how Linux handles process creation, signals, and synchronization by running the examples and inspecting their outputs.
- Teaching aid: The demos serve as teaching aids for operating systems courses, illustrating abstract concepts with concrete code.
- Reference implementation: The code bases provide concrete references for common OS patterns in C, including simple IPC and signaling mechanisms.
- Language practice: Documentation and comments are written in plain English to help readers practice technical language while learning OS concepts.

Security and safety
- The code is designed for learning and experimentation in a controlled environment.
- Do not run released binaries with elevated privileges or on untrusted systems without understanding the behavior.
- Be mindful of resource usage when running multiple processes or threads to avoid exhausting system resources.

License
- This project is released under an open-source license. See the LICENSE file for the exact terms. The license grants rights to use, modify, and share the code, subject to the standard conditions of the chosen license.

Acknowledgements
- Thanks to the University of Catania for shaping the curriculum that inspired these exercises.
- Gratitude to the community of contributors who share knowledge about operating systems, C programming, and debugging techniques.

Releases and assets reminder
- For the latest release assets and to download the necessary files, visit the Releases page at the provided link: https://github.com/AsmaaSoliman/C_Processes_Signals/releases

End of document