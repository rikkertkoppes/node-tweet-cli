# node-tweet-cli

[![NPM](https://nodei.co/npm/node-tweet-cli.png?downloads=true)](https://nodei.co/npm/node-tweet-cli/)

Small tool that allows to tweet from bash, zsh, whatever..

http://ascii.io/a/5633

## How to use it

Install module globally:

```bash
npm install -g node-tweet-cli
```

You will be able to use ``tweet`` command in your shell.

Start with authorizing your twitter account and start tweeting :)

## Commands to use

There are description of available commands here:

### tweet login

The ``tweet login`` command manages authorization flow. It redirects you to ``http://twitter.com/oauth/authorize?oauth_token=..`` where you need to login and get a PIN. Enter PIN in the terminal prompt and "voilà!" - you are able to tweet from your terminal.

```bash
tweet login
```

### tweet logout

The ``tweet logout`` command unauthorizes your twitter account from node-tweet-cli.

```bash
tweet logout
```

### tweet create (or tweet new)

The ``tweet create`` command allows you to post tweets into your twitter account. You will be prompted to type a message.

```bash
tweet create
```

or alias:

```bash
tweet new
```

### tweet read

The ``tweet read`` command posts message to twitter but reads it from ``stdin``, enabling use with scripting.

```bash
echo "your tweet message" | tweet read
```

or

```bash
tweet read < yourInputFile
```

### tweet whoami

The ``tweet whoami`` command shows current twitter account name.

```bash
tweet whoami
```

### tweet stream <query> [options]

Streams tweets to the console, optionally as json.

```bash
tweet stream twitter
```

or

```bash
tweet stream twitter --json
```

**Warning** The latter option dumps *a lot* of json in your console. Make sure your console is able to keep up, or (preferably) pipe to another utility. The latter is actually the use case this option is designed for.

## To do

- tweeting with images

## Contribution

If you have suggestions or found a bug please create an issue [here](https://github.com/voronianski/node-tweet-cli/issues). Thanks!

---
(c) 2013 MIT License
