## Weather & Time Controller

**Weather & Time Controller** is an open-source FiveM client script that allows players to dynamically change the in-game time and weather through an intuitive menu system. This script provides real-time environment control with seamless integration into ESX, making it perfect for roleplay servers and custom gameplay scenarios.

## Features

* [x] Change time of day with presets: Morning, Afternoon, Evening
* [x] Change weather conditions on the fly with multiple weather types
* [x] Freezes time at chosen hour/minute for consistent gameplay atmosphere
* [x] Smooth weather transitions and persistent weather effects
* [x] Easy-to-use ESX menu integration with clear notifications
* [x] Commands to open the menu (`changetime` and `changeweather`)
* [x] Minimal performance impact with efficient threads
* [ ] Planned future enhancements and customization options

## How it works

The script hooks into ESX menus to provide a user interface for selecting time and weather presets. It uses native FiveM functions to override the server clock and weather, applying changes immediately and persisting them until changed again.

```lua
currentHour = 12
currentMinute = 0
freezeTime = true
NetworkOverrideClockTime(currentHour, currentMinute, 0)
PauseClock(true)
```

> \[!TIP]
> Use the commands `/changetime` or `/changeweather` in-game to open the environment control menu quickly.

## Installation

1. Download or copy the `client.lua` and `config.lua` files.
2. Place them inside a resource folder, e.g. `/resources/[local]/fivem-weather-control/`.
3. Add the following to the resource’s `fxmanifest.lua` file:

```lua
fx_version 'cerulean'
game 'gta5'
version '1.0.0'

client_script 'client.lua'
shared_script 'config.lua'
```

4. Configure the command names or menu labels inside `config.lua` as needed.
5. Enable the resource by adding this line to your `server.cfg`:

```cfg
ensure fivem-weather-control
```

> \[!WARNING]
> This script requires the ESX framework (`es_extended`) to be installed and running on your server.

## Contributing

Contributions are highly welcome! To help improve this script:

* Submit Pull Requests (PRs) for new features or bug fixes.
* For minor typos or documentation fixes, consider opening an issue instead.
* Keep pull requests focused and avoid large-scale rewrites in a single submission.
* Refrain from submitting spam or irrelevant content.

## License

This project is licensed under the **MIT License**, granting permission to use, modify, distribute, and sublicense freely, provided the original copyright and license notice remain intact.

The software is provided "as-is" without any warranty.

For full license details, see the [MIT License](https://opensource.org/licenses/MIT).
