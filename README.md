## Phyllite

Phyllite is a mod loader and mod management system for Geometry Dash, designed with a simple, clean, and expandable mod format.

Features

* .phle — Phyllite’s native mod package format
* Built-in mod management
* Enable and disable mods
* Mod information through mod.json and about.json
* Custom mod icons
* Phyllite settings
* Automatic mod registration through mods.conf
* Built-in language selection
* iOS-focused design

Mod Structure

A basic Phyllite mod can be as simple as:

ExampleMod/
mod.json
about.json
icon.png

icon.png is optional.

Mods are packaged as .phle files for sharing and installation:

ExampleMod.phle

mod.json

mod.json contains the basic information Phyllite needs to identify a mod.

Example:

{
    "id": "com.example.examplemod",
    "name": "Example Mod",
    "version": "1.0.0",
    "author": "Author",
    "description": "An example Phyllite mod.",
    "game": "Geometry Dash",
    "icon": "icon.png"
}

about.json

about.json contains additional information that Phyllite can display when viewing a mod.

settings.json

Phyllite uses settings.json to define its available settings, such as language, notifications, mod management, debugging, and update options.

mods.conf

mods.conf keeps track of installed, enabled, and disabled mods.

A fresh Phyllite installation starts with:

installed {
    "com.r3alcyb3r.phyllite" {
        name = "Phyllite"
        version = "1.0.0"
        enabled = true
    }
}
enabled {
    "com.r3alcyb3r.phyllite"
}
disabled {
    null
}

Phyllite automatically updates this file when mods are installed, enabled, disabled, or removed.

.phle

.phle is Phyllite’s mod package format.

A .phle package contains the files required for a Phyllite mod and can be shared through iOS. Phyllite recognizes .phle files and can import them into the user’s Mods collection.

Project

Phyllite is developed by R3ALCYB3R.

Note: this is NOT the same thing as geode SDK.

Version: 1.0.0
