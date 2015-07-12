# Dumb Slut

[![GoDoc](https://godoc.org/github.com/kpashka/dumbslut?status.svg)](https://godoc.org/github.com/kpashka/dumbslut)

:person_with_pouting_face: Little princess, programmed to serve in mens-only conference rooms.

## Features

* Different backends support:
	* [Slack](https://api.slack.com/bot-users)
	* [Telegram](https://core.telegram.org/bots) (in progress)
* Configurable commands:
	* `Artist` - draws symbolic ASCII art from input word.
	* `Bully` - reacts with pre-defined phrase to matched text.
	* `Postman` - grabs latest unread item from RSS/Atom feed.
	* `Proxy` - fetches JSON document from URL, returns template with populated values from [JSONPath](https://github.com/NodePrime/jsonpath#path-syntax) expressions.
* User-friendly:
	* Configurable greeting and farewell messages.
	* Configurable reaction to user status change (only for `Slack` backend).
	* "Shy" mode in case of being annoyed by chatterbox servant.
	* Live configuration reload from URL - share access to the ear with your mates (upcoming).

## Usage

Grab dependencies:

	$ go get github.com/jteeuwen/go-pkg-rss
	$ go get github.com/nlopes/slack
	$ go get github.com/Sirupsen/logrus
	$ go get github.com/tucnak/telebot
	$ go get golang.org/x/exp

Build and run:

	$ go get github.com/kpashka/dumbslut
	$ cd $GOPATH/src/github.com/kpashka/dumbslut
	$ go build && ./dumpslut -c config.json

## Configuration

See [example configuration](config.json.example) for details.