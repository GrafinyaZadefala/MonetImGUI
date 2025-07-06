# MonetImGUI

This repository contains only the **ImGui binding for LuaJIT**.

## Overview

This project provides LuaJIT bindings for the Dear ImGui library, enabling you to write ImGui-based user interfaces using LuaJIT scripts.  
**Note:** This repository includes only the binding layer and does not provide the core ImGui library itself or any backend/platform implementations.

## Usage

- The binding exposes ImGui functions and types to LuaJIT, allowing you to create and manipulate ImGui UI elements directly from Lua scripts.
- You must separately compile and link the Dear ImGui core library into your application.
- This binding does **not** include or manage the graphics rendering pipeline or input event handling.

## Important: Rendering and Input Handling

Dear ImGui is a platform-agnostic UI library that requires a backend for rendering and input.  
This binding does **not** provide:

- **Rendering implementation:** You need to integrate ImGui draw data with your graphics API (OpenGL, Vulkan, DirectX, Metal, etc.) yourself.
- **Keyboard input processing:** Key presses, releases, and text input must be forwarded to ImGui by your application.
- **Touch and mouse input:** Touch gestures, clicks, and movement events must be captured and delivered appropriately.

You are responsible for implementing or integrating these platform-specific systems alongside this LuaJIT binding to achieve a fully functional UI.

## Recommendations

- Refer to the official [Dear ImGui examples](https://github.com/ocornut/imgui/tree/master/examples) for backend implementations in various graphics APIs and platforms.
- Consider using existing backend implementations and adapting them to forward input and rendering data into your LuaJIT environment.
- Modularize your codebase to separate the binding layer, rendering, and input logic for maintainability and flexibility.

## Contributing

Contributions, bug reports, and pull requests are welcome! Please feel free to:

- Suggest improvements to the binding interface.
- Submit fixes or extensions.
- Share examples of backend integrations.

## Contact

If you have any questions, ideas, or want to get in touch, please contact me:

- Telegram: [@UxyOy](https://t.me/UxyOy)  
- GitHub: [DobruiKola](https://github.com/DobruiKola)

---

Happy coding! 🎉
