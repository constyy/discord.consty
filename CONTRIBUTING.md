# Contributing

**The issue tracker is only for bug reports and enhancement suggestions. If you have a question, please ask it in the [Official Discord.JS Discord server](https://discord.gg/bRCvFy9) instead of opening an issue – you will get redirected there anyway.**

If you wish to contribute to the discord.js codebase or documentation, feel free to fork the repository and submit a
pull request. We use ESLint to enforce a consistent coding style, so having that set up in your editor of choice
is a great boon to your development process.

## Setup

To get ready to work on the codebase, please do the following:

1. Fork & clone the repository, and make sure you're on the **master** branch
2. Run `npm ci`
3. If you're working on voice, also run `npm install @discordjs/opus` or `npm install opusscript`
4. Code your heart out!
5. Run `npm test` to run ESLint and ensure any JSDoc changes are valid
6. [Submit a pull request](https://github.com/discordjs/discord.js/compare) (Make sure you follow the [conventional commit format](https://github.com/discordjs/discord.js-next/blob/master/.github/COMMIT_CONVENTION.md))