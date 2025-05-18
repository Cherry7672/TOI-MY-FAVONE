# Junnu

[![Build Status](https://travis-ci.org/sukeesh/Jarvis.svg?branch=master)](https://travis-ci.org/sukeesh/Jarvis) [![Join the chat at https://gitter.im/Sukeesh_Jarvis/Lobby](https://badges.gitter.im/Sukeesh_Jarvis/Lobby.svg)](https://gitter.im/Sukeesh_Jarvis/Lobby?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

A Personal Non-AI Assistant for Linux, MacOS and Windows

![Junnu](http://i.imgur.com/xZ8x9ES.jpg)

Junnnu is a simple personal assistant for Linux, MacOS and Windows which works on the command line. He can talk to you if you enable his voice. He can tell you the weather, he can find restaurants and other places near you. He can do some great stuff for you.

## 🚀 20 Different Tasks That Junnu Can Do For You:

1. **Entertainment & Suggestions**
   - Suggest activities if you're bored (`activity`, `bored`)
   - Provide ideas on what to draw, watch, or listen to (`prompt`, `top_media`, `taste dive`, `mood music`)

2. **Sports Updates**
   - Get up-to-date sports information: team rankings, match times, player stats (`basketball`, `cricket`, `soccer`, `tennis`)

3. **Games**
   - Play games: Blackjack, Connect Four, Hangman, Rock-Paper-Scissors, etc. (`blackjack`, `connect_four`, `guess_number_game`, `hangman`, `rockpaperscissors`, `roulette`, `tic_tac_toe`, `word_game`, `wordle`)

4. **Health & Fitness**
   - Access nutrition facts, recipes, workout programs, and health trackers (`bmi`, `bmr`, `calories`, `food recipe`, `fruit`, `fruit nutrition`, `workout`)

5. **Cocktail Recipes**
   - Learn how to make cocktails (`cocktail`, `drink`)

6. **Random Generators**
   - Generate random lists, numbers, passwords (`random list`, `random number`, `random password`)

7. **Unit Conversions**
   - Convert units: binary, currency, hex, length, mass, speed, temperature, time (`binary`, `currencyconv`, `hex`, `lengthconv`, `massconv`, `speedconv`, `string_convert`, `tempconv`, `timeconv`)

8. **Photography**
   - Take pictures and screenshots (`open camera`, `screencapture`)

9. **System Information**
   - Get computer specifications (`battery`, `cat his`, `dns forward`, `dns reverse`, `hostinfo`, `ip`, `scan_network`, `speedtest`, `os`, `check ram`, `systeminfo`)

10. **File Management**
    - Manage and organize files (`file manage`, `file organize`)

11. **Image Processing**
    - Upload, edit, and convert images (`imgur`, `image to pdf`, `image compressor`)

12. **PDF Conversion**
    - Convert webpages to PDF or PDFs to images (`htmltopdf`, `pdf to images`)

13. **Jokes & Facts**
    - Enjoy jokes and random facts (`dadjoke`, `joke daily`, `joke chuck`, `joke`, `fact`, `cat fact`)

14. **Calculations**
    - Perform calculations and solve equations (`calculate`, `factor`, `solve`, `equations`, `plot`, `matrix add`)

15. **QR Code Generation**
    - Generate QR codes for URLs (`qr`)

16. **Weather Updates**
    - Check the weather forecast (`weather report`)

17. **Language Translation**
    - Translate languages (`translate`)

18. **Stock Market Information**
    - Display stock and cryptocurrency information (`stock`, `cryptotracker`)

## 🛠️ Getting Started

### Installation

1. **Clone the Repository**

   ```bash
   git clone https://github.com/sukeesh/Junnu.git
   ```

2. **Run the installer**
   ```bash
   python installer
   ```
   If that doesn't work, try:
   ```bash
   python3 installer
   ```

### Running Jarvis

- Run Junnu from anywhere:
  
   ```bash
   junnu
   ```

  Or from within the project folder:
  
   ```bash
   ./junnu
   ```

You can start by typing `help` within the Junnu command line to check what Junnu can do for you.

## ❓Frequently encountered issues
**Question**: 
When I run Junnu, it shows an error relating to module not found<br>

**Platform**: 
Windows<br>

**Solution 1**: Uninstall and/or install the module package.<br>

**Example:**<br>
Error: `ImportError: DLL load failed while importing win32api: The specified module could not be found.`<br>

**Solution:**<br>
`pip uninstall pywin32`<br>
`pip install pywin32` or `conda install pywin32`<br>

**Solution 2**: add the package to your environment variables system PATH.<br>

-----

**Question**: After cloning the repo in terminal it gives an error when running python3 installer saying please install virtual environemnt.

**Solution**: 
- Install virtual env using this command:
  ```bash
  python3 -m pip install virtualenv
  ```
- OR: On Linux use package manager (e.g. Ubuntu sudo apt install python3-venv)
  
- Restart Installer

-----

**If you find other issues and/or have found solutions to them on any platform, please consider adding to this list!**

## 🤝 Contributing

Check out our [CONTRIBUTING.md](CONTRIBUTING.md) to learn how you can contribute!

### QuickStart: Create a new feature (plugin)

Create new file custom/hello_world.py

```
from plugin import plugin


@plugin("helloworld")
def helloworld(junnu, s):
    """Repeats what you type"""
    junnu.say(s)
```

Check it out!
```
./junnu
Junnu' sound is by default disabled.
In order to let Jarvis talk out loud type: enable sound
Type 'help' for a list of available actions.

~> Hi, what can I do for you?
helloworld junnu is cool!
junnu is cool
```

### Plugins

[Click here](doc/PLUGINS.md) to learn more about plugins.

### Creating a test

Creating a test is optional but never a bad idea ;).

[Click here](doc/TESTING.md) to learn more about testing.

### How to run tests:

 Run `test.sh`
 ```bash
 ./test.sh
 ```
## Optional Dependencies

- Any pyttsx3 text-to-speech engine (``sapi5, nsss or espeak``) for Jarvis to talk out loud (e.g. Ubuntu do ``sudo apt install espeak``)
- Portaudio + python-devel packages for voice control
- ``notify-send`` on Linux if you want to receive *nice* and desktop-notification instead of *ugly* pop up windows (e.g. Ubuntu do ``sudo apt install libnotify-bin``)
- ``ffmpeg`` if you want ``music`` to download songs as .mp3 instead of .webm

## Docker

Run with docker (docker needs to be installed and running):

```
[sudo] make build_docker
[sudo] make run_docker
```

## Authors

 **cherry**

See also the list of [contributors](https://github.com/Cherry7672/TOI-MY-FAVONE) who have participated in this project.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
