# WGU Workspace Launcher

A lightweight, unofficial desktop launcher built with **Python and GTK 4** for my Fedora Linux workstation. It brings together quick access to the WGU student portal and Microsoft 365 applications in a single, consistent interface.

## Why I built it

I wanted a convenient way to open the student and productivity tools I use frequently without navigating through multiple browser bookmarks or menus. This personal project combines desktop integration, application discovery, and a simple graphical interface.

## Features

- GTK 4 graphical interface with a two-column application grid
- Shortcuts for the WGU student portal, Outlook, Word, Excel, PowerPoint, OneNote, Teams, and OneDrive
- Detection of locally installed desktop launchers
- Application icons and disabled buttons when a launcher cannot be found
- A custom-themed window and application icon

## Technologies

Python 3, PyGObject, GTK 4, Linux desktop entry files, and `gtk-launch`.

## Environment

Developed and used on **Fedora Linux with GNOME**. Other Linux distributions and desktop environments have not been tested.

Applications in the grid rely on compatible `.desktop` entries already being present on the computer. The project does not install Microsoft 365 apps or authenticate to WGU on the user's behalf.

## Source and setup

The Python source is in [`wgu-menu`](./wgu-menu), with a sample [desktop entry](./com.alec.WGULauncher.desktop) and [SVG application icon](./assets/wgu-launcher.svg). The desktop entry assumes `wgu-menu` is on your `PATH` and the icon is installed under the `wgu-launcher` icon name. GTK 4, PyGObject, and `gtk-launch` are required. This is a portfolio code sample, not a packaged installer.

The public copy uses application-name discovery for Outlook rather than the original machine-specific Chrome web-app identifier. If Outlook is not detected, its button remains disabled. This public version has not yet been run-tested.

## Engineering takeaways

This project demonstrates practical Python scripting, GTK desktop UI development, Linux application integration, and simplifying a repetitive user workflow.

## Disclaimer

This is an independent, **unofficial** personal project. It is not affiliated with, endorsed by, or supported by Western Governors University or Microsoft. The names of third-party products and services are used for identification only.
