[dotbot_repo]: https://github.com/anishathalye/dotbot
[dotbot_plugin_firefox_repo]: https://github.com/kurtmckee/dotbot-firefox

# dotbot librewolf Plugin

Plugin for [Dotbot][dotbot_repo], that adds ```librewolf``` directive, which allows you to use your own librewolf.overrides.cfg, user.js or userChrome. The plugin is inspired by [dotbot-firefox][dotbot_plugin_firefox_repo] from kurtmckee.

## Installation

```
git submodule add https://gitlab.com/paulbecker/dotbot_plugin_librewolf.git
```

## Usage

```yaml
# Example 1: 
# user.js and userChrome.css
- librewolf:
    user.js: librewolf/user.js
    userChrome.css: librewolf/userChrome.css

# Example 2: 
# librewolf.overrides.cfg and chrome Directory with a whole theme inside
- librewolf:
  chrome: librewolf/chrome
  librewolf.overrides.cfg: librewolf/librewolf.overrides.cfg
```

# Librewolf profile locations

The dotbot librewolf plugin is aware of the folliwng default directories:

* %APPDATA%\Librewolf (Windows)
* ~/Library/Application Support/Librewolf (Mac OS)
* ~/.librewolf (Linux)
* ~/var/app/io.gitlab.librewolf-community/.librewolf (Librewolf Flatpak for Linux)

Only profile subdirectories that contain a prefs.js file will be considered valid by the plugin.
