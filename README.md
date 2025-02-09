# ISOTPlib
Highly configurable and flexible C library for implementing ISO 15765-2 (Transport Layer) for CAN, CAN-FD, and LIN networks.

> [!IMPORTANT] 
This library solely focuses on implementation of the ISO-TP protocol. As ISO-TP is often implemented alongside UDS, this library was designed to integrate seamlessly with [udslib](https://github.com/nickdaria/udslib).

# 🚀 Key Features
- CAN, CAN-FD, and LIN implementations of ISO-TP
- Strict adherence to ISO 15765-2 specification
- Easy-to-use callbacks and error handling
- Pure C, platform agnostic with C++/Arduino compatibility
- Static memory allocation
- Tight scope - no bloat

# ⚡️ Advanced Features
- Concurrent sessions
- Per-session protocol configuration - padding enable, padding byte, consecutive index ordering, etc
- Supports user implementation of dynamic RX memory allocation

# ❓Why isotplib?
When I set out on my latest vehicle module project which needed to make UDS queries against multiple modules concurrently, I could not find any ISOTP libraries that met my needs and functional criteria. I kept seeing the following:
- Reliance on shims and polling functions for interaction with the bus and timed events
- Stepping outside of ISO-TPs scope, dealing with arbitration IDs and sometimes even UDS
- Focused exclusively on CAN 2.0, largely ignoring support for CAN-FD or LIN
- Configuration like padding and block size requests are set as a preprocessor macro

I solved this by writing isotplib as a non-polling, tight-scope, configurable library that supports CAN, CAN-FD, and LIN implementations of ISO-TP.

# ✏️ Usage
- See `examples/` for functioning code (command line & microcontroller)
- See the [implementation wiki page](https://github.com/nickdaria/isotplib/wiki/Implementation) for a quick overview of how to start using isotplib
