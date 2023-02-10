# darkfang browser

Darkfang is a fast, minimal browser that protects your privacy. It includes an interface designed to minimize distractions, and features such as:

- Information from [DuckDuckGo](https://duckduckgo.com) in the search bar.
- Full-text search for visited pages
- Ad and tracker blocking
- Automatic reader view
- Tasks (tab groups)
- Password manager integration
- Dark theme

It also aims to eventually incorporate AI and web3 tools to help you on the "new internet", one powered by AI search and decentralized technologies. This work is in the planning stages for this browser project and is ongoing.

We will soon have some downloads ready for different operating systems here, beginning, as usual, with builds for GNU/Linux.

## Screenshots

<img alt="The search bar, showing information from DuckDuckGo" src="http://minbrowser.org/tour/img/searchbar_duckduckgo_answers.png" width="650"/>

<img alt="The Tasks Overlay" src="http://minbrowser.org/tour/img/tasks.png" width="650"/>

<img alt="Reader View" src="https://user-images.githubusercontent.com/10314059/53312382-67ca7d80-387a-11e9-9ccc-88ac592c9b1c.png" width="650"/>

## Installing

You can find prebuilt binaries for darkfang [here](https://github.com/Nightshade-Foundation/darkfang/releases). Alternatively, skip to the section below for instructions on how to build Min directly from source.

### Installation on Linux

- To install the .deb file, use `sudo dpkg -i /path/to/download`
- To install the RPM build, use `sudo rpm -i /path/to/download --ignoreos`

## Developing

If you want to buid on top of Darkfang:

- Install [Node](https://nodejs.org).
- Run `npm install` to install dependencies.
- Start Darkfang in development mode by running `npm run start`.
- After you make changes, you can press `ctrl+r` (or `cmd+r` on Mac) twice to restart the browser.

### Building binaries

In order to build darkfang from source, follow the installation instructions above, then use one of the following commands to create binaries:

- `npm run buildWindows`
- `npm run buildMacIntel`
- `npm run buildMacArm`
- `npm run buildDebian`
- `npm run buildRaspi` (for 32-bit Raspberry Pi)
- `npm run buildLinuxArm64` (for 64-bit Raspberry Pi or other ARM Linux)
- `npm run buildRedhat`

Depending on the platform you are building for, you may need to install additional dependencies:

- If you are using macOS and building a package for Linux, install [Homebrew](http://brew.sh), then run `brew install fakeroot dpkg` first.
- If you are using macOS or Linux and building a package for Windows, you will need to install [Mono](https://www.mono-project.com/) and [Wine](https://www.winehq.org/).
- If you are building a macOS package, you'll need to install Xcode and the associated command-line tools. You may also need to set your default SDK to macOS 11.0 or higher, which you can do by running `export SDKROOT=/Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX11.1.sdk`. The exact command will depend on where Xcode is installed and which SDK version you're using.
- To build on Windows, you'll need to install Visual Studio. Once it's installed, you may also need to run `npm config set msvs_version 2019` (or the appropriate version).

## Contributing to Darkfang

Thanks for taking the time to contribute to Darkfang!

### Getting Help

If you're experiencing a bug or have a suggestion for how to improve darkfang, please open a [new issue](https://github.com/Nightshade-Foundation/darkfang/issues/new/choose).

### Contributing Translations

#### Adding a new language

- Find the language code that goes with your language from [this list](https://source.chromium.org/chromium/chromium/src/+/main:ui/base/l10n/l10n_util.cc;l=55) (line 55 - 230).
- In the `localization/languages` directory, create a new file, and name it "[your language code].json".
- Open your new file, and copy the contents of the <a href="https://github.com/minbrowser/min/blob/master/localization/languages/en-US.json">localization/languages/en-US.json</a> file into your new file.
- Change the "identifier" field in the new file to the language code from step 1.
- Inside the file, replace each English string in the right-hand column with the equivalent translation.
- (Optional) See your translations live by following the [development instructions](#installing) above. Min will display in the same language as your operating system, so make sure your computer is set to the same language that you're translating.
- That's it! Make a pull request with your changes.

#### Updating an existing language

- Find the language file for your language in the `localization/languages` directory.
- Look through the file for any items that have a value of "null", or that have a comment saying "missing translation".
- For each of these items, look for the item with the same name in the `en-US.json` file.
- Translate the value from the English file, replace "null" with your translation, and remove the "missing translation" comment.
- Make a pull request with the updated file.

[DiscordBadge]: https://img.shields.io/discord/764269005195968512.svg?label=Discord&logo=discord&logoColor=white
[DiscordUrl]: https://discord.gg/bRpqjJ4
[DownloadsBadge]: https://img.shields.io/github/downloads/minbrowser/min/total.svg
[DownloadsUrl]: https://github.com/minbrowser/min/releases

### Credits

We are building on top of the excellent [Min](https://github.com/minbrowser) project. 

This project also could not exist without **Electron** and **Chromium**. 

We will also be building on top of some artificial intelligence and web3 applications. Credits for these will be forthcoming once they are decided on and implemented into the Darkfang project.
