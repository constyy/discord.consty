<div align="center">
  <br />
  <br />
  <p>
    <a href="https://www.npmjs.com/package/discord.consty"><img src="https://img.shields.io/npm/v/discord.consty.svg?maxAge=3600" alt="NPM version" /></a>
    <a href="https://www.npmjs.com/package/discord.consty"><img src="https://img.shields.io/npm/dt/discord.consty.svg?maxAge=3600" alt="NPM downloads" /></a>
  </p>
  <p>
    <a href="https://nodei.co/npm/discord.consty/"><img src="https://nodei.co/npm/discord.consty.png?downloads=true&stars=true" alt="npm installnfo" /></a>
  </p>
</div>

## Table of contents

- [About](#about)
- [Installation](#installation)
  - [Audio engines](#audio-engines)
  - [Optional packages](#optional-packages)
- [Example Usage](#example-usage)
- [Links](#links)
  - [Extensions](#extensions)
- [Contributing](#contributing)
- [Help](#help)

## About

discord.consty (a framework for discord.js) is a powerful [Node.js](https://nodejs.org) module that allows you to easily interact with the
[Discord API](https://discord.com/developers/docs/intro).

- Object-oriented
- Predictable abstractions
- Performant
- 100% coverage of the Discord API

## Installation

**Node.js 12.0.0 or newer is required.**  
Ignore any warnings about unmet peer dependencies, as they're all optional.

Without voice support: `npm install discord.consty`  
With voice support ([@discordjs/opus](https://www.npmjs.com/package/@discordjs/opus)): `npm install discord.consty @discordjs/opus`  
With voice support ([opusscript](https://www.npmjs.com/package/opusscript)): `npm install discord.consty opusscript`

### Audio engines

The preferred audio engine is @discordjs/opus, as it performs significantly better than opusscript. When both are available, discord.consty will automatically choose @discordjs/opus.
Using opusscript is only recommended for development environments where @discordjs/opus is tough to get working.
For production bots, using @discordjs/opus should be considered a necessity, especially if they're going to be running on multiple servers.

### Optional packages

- [zlib-sync](https://www.npmjs.com/package/zlib-sync) for WebSocket data compression and inflation (`npm install zlib-sync`)
- [erlpack](https://github.com/discord/erlpack) for significantly faster WebSocket data (de)serialisation (`npm install discord/erlpack`)
- One of the following packages can be installed for faster voice packet encryption and decryption:
  - [sodium](https://www.npmjs.com/package/sodium) (`npm install sodium`)
  - [libsodium.js](https://www.npmjs.com/package/libsodium-wrappers) (`npm install libsodium-wrappers`)
- [bufferutil](https://www.npmjs.com/package/bufferutil) for a much faster WebSocket connection (`npm install bufferutil`)
- [utf-8-validate](https://www.npmjs.com/package/utf-8-validate) in combination with `bufferutil` for much faster WebSocket processing (`npm install utf-8-validate`)

## Example usage

```js
const Discord = require('discord.consty');
const client = new Discord.Client();

client.on('ready', () => {
  console.log(`Logged in as ${client.user.tag}!`);
});

client.on('message', msg => {
  if (msg.content === 'ping') {
    msg.reply('pong');
  }
});

client.login('token');
```

### Extensions

- [RPC](https://www.npmjs.com/package/discord-rpc) ([source](https://github.com/discordjs/RPC))

## Contributing

Before creating an issue, please ensure that it hasn't already been reported/suggested, and double-check the
[official documentation of discord.js](https://discord.js.org/#/docs).  
See [the contribution guide](https://github.com/constyy/discord.consty/blob/master/.github/CONTRIBUTING.md) if you'd like to submit a PR.
