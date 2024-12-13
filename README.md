# dwm - Dynamic Window Manager

**dwm** is an extremely fast, small, and dynamic window manager for Linux.

## Requirements

To build dwm, you need:
- Xlib header files

## Installation

1. **Configure the Makefile**:
   - Edit `config.mk` to match your local setup. By default, dwm is installed into the `/usr/local` namespace.

2. **Build and Install**:
   - Run the following command (as root if necessary):
     ```sh
     make clean install
     ```

## Running dwm

- **Starting with `.xinitrc`**:
  - Add this line to your `.xinitrc` to start dwm using `startx`:
    ```sh
    exec dwm
    ```
  
- **Specific Display Connection**:
  - Ensure the `DISPLAY` environment variable is set correctly. For example:
    ```sh
    DISPLAY=foo.bar:1 exec dwm
    ```
    This command starts dwm on display `:1` of host `foo.bar`.

- **Displaying Status Info in the Bar**:
  - Add this to your `.xinitrc` for status updates:
    ```sh
    while xsetroot -name "`date` `uptime | sed 's/.*,//'`"
    do
        sleep 1
    done &
    exec dwm
    ```

## Configuration

- **Customizing dwm**:
  - Configuration is done by creating a custom `config.h` file and recompiling the source code. This allows you to tailor dwm to your preferences without altering the main codebase.
