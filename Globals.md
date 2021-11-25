# Globals

In C++, by default, globals are strong. To make them weak we need
`__attribute__((weak))`

## Strong Globals [[Symbols#Strong Symbols]]
- Initialized to non-zero
- Initialized to zero
Stored in `.DATA` or `.BSS` section

## Weak Globals [[Symbols#Weak Symbols]]
- Not initialized, only defined
Stored in `.COMMON` section