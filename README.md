# Elgato Key Light Automator

I forked this from the original project [and rolled back to the commit before the introduction of Bonjour](https://github.com/jasonheecs/elgato-key-light-automator/tree/ead7eb0724150914c775e7bcae7a6ee8eaa9d9ab).

Bonjour was painfully slow and inconsistent, and since the lights are local only, I don't mind using a config file.

[![Build Status][circleci-badge]][circleci-link]

A Node.js script that toggles on and off Elgato Key Lights and Elgato Key Light Airs. Elgato Stream Deck not required.

## Usage
```bash
git clone https://github.com/luminus/elgato-key-light-automator.git
cd elgato-key-light-automator && npm i
node index.js
```

You'll need to edit the `config.json` file with the IP address(es) or human readable URL(s) of your Key Light(s) for the command to work since this doesn't rely on Bonjour anymore.

## Testing
Testing is done via Jest:
```bash
npm run test
```

Refer to the [Circle CI config](.circleci/config.yml) file and [CircleCI build logs][circleci-link] for details on the automated tests and expected outputs.

## License
MIT

[circleci-badge]: https://circleci.com/gh/jasonheecs/elgato-key-light-automator.svg?style=svg
[circleci-link]: https://app.circleci.com/pipelines/github/jasonheecs/elgato-key-light-automator