# bing-cli

Execute Bing Search queries from the terminal including Web, News, Related Search, AutoSuggest, and Images. Images are displayed as colorized-ASCII art or as inline images directly (if using iTerm2).

*Note: This project is not affiliated with Microsoft Corporation*


[![Join the chat at https://gitter.im/bing-cli/Lobby](https://badges.gitter.im/bing-cli/Lobby.svg)](https://gitter.im/bing-cli/Lobby?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge) [![build status](https://secure.travis-ci.org/scottbea/bing-cli.png)](http://travis-ci.org/scottbea/bing-cli) [![npm version](https://badge.fury.io/js/bing-cli.svg)](https://badge.fury.io/js/bing-cli) [![License](http://img.shields.io/:license-mit-blue.svg)](http://doge.mit-license.org) 
[![dependency Status](https://david-dm.org/scottbea/bing-cli.svg?style=flat)](https://david-dm.org/scottbea/bing-cli) [![devDependency Status](https://david-dm.org/scottbea/bing-cli/dev-status.png?style=flat)](https://david-dm.org/scottbea/bing-cli?type=dev)

## Installation

First, install GraphicsMagick to support the image search features [GraphicsMagick](http://www.graphicsmagick.org/). In Mac OS X, you can simply use [Homebrew](http://mxcl.github.io/homebrew/) and do:

``` bash
$ brew install graphicsmagick
```

Then, the Bing-CLI module is installed globally via npm:

``` bash
$ npm install bing-cli -g
```


## Usage
This package is meant to be used as a command-line tool.

``` js
$ bing <search query> [-c <n>]
$ bing image <query> [-full] [-unsafe] [-c <n>] [-type <imageType>] [-size <imageSize> [-bw] [-grey] [-pixels] [-blocks] [-bg <rgb>]]
$ bing images <query> [-unsafe] [-c <n>]
$ bing news
$ bing news <query>
$ bing related <query>
$ bing suggest <query>
$ bing -version
```

## Examples
This package is meant to be used as a command-line tool.

``` js
$ bing puff the magic dragon
$ bing -c 3 "sql server on linux"
$ bing images famous people
$ bing image yosemite -full
$ bing image apple logo -size small -full -scale 0.5 -ascii -bw -invert
$ bing image hawaii -ascii -pixels
$ bing news
$ bing news politics
$ bing news azure aws google cloud
$ bing related apache spark
$ bing suggest gaussi
$ bing netscaler manual fileType:pdf
$ bing image homeaway.com logo -ascii -blocks -size medium -invert -scale 0.8
```

![Example Screen Shot](https://github.com/scottbea/bing-cli/raw/master/docs/screen3.png)

## Configuration
### Subscribing to APIs
Bing-CLI requires API keys from Microsoft to work at scale. There is a trial set of API keys included with limited query quota that is enough for trying it out. 

Sustained usage will require that you 
get your API keys, you will need to sign up for [Microsoft Congnitive Services](https://www.microsoft.com/cognitive-services/en-us/subscriptions) by creating a new account with an email, or by signing up with your GitHub or LinkedIn account. Once you do this, you can click on the Pricing link to subscribe to a free-tier of services (more than enough for personal use) for the following APIs:

- Bing Web Search - Free
- Bing Autosuggest - Free 

### Setting Environment Variables
Once you subscribe to each API, you can then click the Show link to reveal the API keys. Then copy these keys and put them in the exports for the .bash_profile (as mentioned above).

``` shell
export BING_SEARCH_KEY=<your key here>
export BING_AUTOSUGGEST_KEY=<your key here>
```

Make sure to restart the shell or source .bash_profile (or other shell profile file) for the changes to take effect.

``` shell
$ source ~/.bash_profile
```

## Development

### Testing

```
npm test
```

### Bugs

Please report any bugs [here](https://github.com/scottbea/bing-cli/issues).

### Changelog

Available [here](https://github.com/scottbea/bing-cli/blob/master/CHANGELOG.md).


## License

MIT
