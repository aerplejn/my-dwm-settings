# dwm - Dynamic Window Manager

**dwm** is an extremely fast, small, and dynamic window manager for Linux.

## Requirements

- **Xlib header files**: Necessary for building dwm.

## Installation

1. **Edit `config.mk`**: Adjust the settings to match your local setup. By default, dwm is installed into the `/usr/local` namespace.

2. **Build and Install**:
   - Run the following command to build and install dwm. You might need to execute this as root:
   
     ```sh
     make clean install
     ```

## Running dwm

- **Starting via `.xinitrc`**:
  - Add the following line to your `.xinitrc` to start dwm with `startx`:
  
    ```sh
    exec dwm
    ```

- **Specifying a Display**:
  - Ensure the `DISPLAY` environment variable is set correctly for a specific display, for example:
  
    ```sh
    DISPLAY=foo.bar:1 exec dwm
    ```
  
    This command will start dwm on display `:1` of the host `foo.bar`.

- **Displaying Status Info**:
  - To show status information in the bar, you can add the following script to your `.xinitrc`:
  
    ```sh
    while xsetroot -name "`date` `uptime | sed 's/.*,//'`"
    do
        sleep 1
    done &
    exec dwm
    ```

## Configuration

- **Custom Configuration**:
  - Configuration of dwm is achieved by creating or editing a `config.h` file and then recompiling the source code. This allows for personalization of window management behaviors, keybindings, and more.
