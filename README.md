# Spectrum C++ Style Guide

## Naming Conventions

Class and struct names should be `CamelCase`.

Variable and function names should be all lowercase and separated by underscores (ex. `int number_of_wheels`).

In addition, the following prefixes should be used:
- `m_` for member variables
- `s_` for static variables
- `g_` for global variables

Note that function parameters have no special prefix.

Use `ALL_CAPS` for macro and `enum` fields only - *not* constants.

Example:
```cpp
enum class ErrorCode
{
  ERROR_OUT_OF_MEMORY,
  ERROR_BAD_PATH,
  // ...
}
```

Namespaces should also be all lowercase and separated by underscores (ex. `namespace graphics`).

## Modifiers

Reference and pointer modifiers (`&` and `*`) always appear *closest* to the type.

Examples:
```cpp
// Free-standing variables
T* ptr;

// Function return types
T& operator[](size_t index);

// Function parameters
void set_value(T& value);
```

## Curly Braces

Always place curly braces on newlines. This includes:
- Class / struct declarations
- If-else blocks
- Try-catch statements
- Switch statements
- Function definitions
- Etc.

Example:
```cpp
if (condition)
{
  // ...
}
```

## Comments

Use doxygen style `//!` comments above class and function declarations to describe their
intended purpose / functionality.

Otherwise, use the standard `//` comment notation. Do not use `/* */` for multi-line comments.

## Class Structure

Use the `public` before `protected` before `private` order.

Within each block, items should appear in the following order:

1. `using` declarations and `typedef`s
2. Static functions
3. Constructors
4. Destructors
5. Member functions
6. Static variables
7. Member variables
8. `friend` declarations
