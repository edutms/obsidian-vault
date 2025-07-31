2025-07-31 08:57

### Status: #baby

### Tags: [[os]]

# What is  stdio?

stdio is short for ==Standard Input-Output==, a foundational concept in programming.

## Descriptions
 `stdio` is an abstraction layer used in programming languages (mostly low-level such as C) to handle the following methods:
 - `stdin` - reading input (for example your keyboard)
 - `stdout` - writing output (in console)
 - `stderr` - writing error messages

--- 
Example in C:
 ```
 #include <stdio.h>

int main() {
    char name[50];

    printf("Enter your name: ");          // writes to stdout
    scanf("%s", name);                    // reads from stdin
    printf("Hello, %s!\n", name);         // writes to stdout

    return 0;
}
```

Example in Python:

```
name = input("Enter your name: ")         # stdin
print(f"Hello, {name}!")                  # stdout
```






# References









