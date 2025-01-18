# VS Code C++ Snippets for Orthodox Canonical Form

This repository provides ready-to-use VS Code snippets for quickly generating the **Orthodox Canonical Form** in C++. These snippets help streamline C++ development by reducing repetitive typing.

## 📌 How to Configure the Snippets in VS Code

Follow these steps to add the snippets to your VS Code setup:

### 1️⃣ Open VS Code Snippet Configuration

1. Open **VS Code**.
2. Press `Ctrl + Shift + P` (or `Cmd + Shift + P` on macOS) to open the **Command Palette**.
3. Type **"Preferences: Configure User Snippets"** and select it.
4. Choose either:
   - `cpp.json` → If you want the snippets to be available only for C++.
   - `New Global Snippets file` → If you want the snippets to be available for all languages.

### 2️⃣ Add the Snippets

Copy and paste the following JSON content into your snippet file:

```json
{
    "Exam Header": {
        "prefix": "examh",
        "body": [
            "#ifndef ${TM_FILENAME_BASE}_HPP",
            "#define ${TM_FILENAME_BASE}_HPP",
            "",
            "class ${TM_FILENAME_BASE} {",
            "  public:",
            "      ${TM_FILENAME_BASE}();",
            "      ${TM_FILENAME_BASE}(const ${TM_FILENAME_BASE}& other);",
            "      ~${TM_FILENAME_BASE}();",
            "      ${TM_FILENAME_BASE}& operator=(const ${TM_FILENAME_BASE}& other);",
            "};",
            "",
            "#endif"
        ],
        "description": "Header for Orthodox Canonical Form"
    },
    "Exam Implementation": {
        "prefix": "examc",
        "body": [
            "#include \"${TM_FILENAME_BASE}.hpp\"",
            "",
            "${TM_FILENAME_BASE}::${TM_FILENAME_BASE}() {}",
            "${TM_FILENAME_BASE}::${TM_FILENAME_BASE}(const ${TM_FILENAME_BASE}& other) {}",
            "${TM_FILENAME_BASE}::~${TM_FILENAME_BASE}() {}",
            "${TM_FILENAME_BASE}& ${TM_FILENAME_BASE}::operator=(const ${TM_FILENAME_BASE}& other) {}",
            ""
        ],
        "description": "Implementation of Orthodox Canonical Form"
    }
}
```

### 3️⃣ Save and Test

1. **Save** the file (`Ctrl + S` or `Cmd + S`).
2. Open a new `.hpp` or `.cpp` file.
3. Type `examh` or `examc` and press `Tab` to insert the snippet.

## 🎯 Example Usage

### Typing `examh` will generate:
```cpp
#ifndef CLASSNAME_HPP
#define CLASSNAME_HPP

class CLASSNAME {
  public:
      CLASSNAME();
      CLASSNAME(const CLASSNAME& other);
      ~CLASSNAME();
      CLASSNAME& operator=(const CLASSNAME& other);
};

#endif
```

### Typing `examc` will generate:
```cpp
#include "CLASSNAME.hpp"

CLASSNAME::CLASSNAME() {}
CLASSNAME::CLASSNAME(const CLASSNAME& other) {}
CLASSNAME::~CLASSNAME() {}
CLASSNAME& CLASSNAME::operator=(const CLASSNAME& other) {}
```

## 🚀 Enjoy Efficient C++ Development!
Now, you can write C++ classes following the Orthodox Canonical Form in just a few keystrokes!

---

### 📝 Additional Notes
- Modify the snippet file anytime to adjust the formatting.
- You can add more snippets for additional boilerplate code.
- Make sure the filename of the `.hpp` and `.cpp` files matches the class name to avoid compilation issues.

Happy coding! 🎉

