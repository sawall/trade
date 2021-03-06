# trade: ssh -> telnet proxy with bonus sugar

trade is intended to connect to Tradewars 2002 servers. It performs a number of
features which make tradewars playable on a modern computer:

<img src="example.png" />

This image is taken from a standard SSH connection through `trade` inside
of `putty`.

Some features of `trade`:

* Multiple connections, same proxy -- all connections route to the same telnet
  session.
* translates DOS Code Page 437 to UTF-8, including line drawing characters.
  Works great with putty default settings over SSH, or most modern terminals
  with openssh.
* operates over SSH (telnet is still used to connect to tradewars)
* Menu for controlling your sessions (press `^E` in a session to escape to the menu)
* *COMING SOON* expect-like scripting capabilities with mruby
* *COMING SOON* outbound ssh support for controlling things that are not tradewars!

## Usage

```bash
$ go get github.com/erikh/trade
$ trade gen # generates a host key in ~/.config/trade/host_key
$ trade &
$ ssh -p 2002 localhost
```

After connecting with SSH, you can press enter or `?` to get a menu. Press `c` to connect
to a server (try `home.hollensbe.org:2002`!) or `s` to shutdown the server.

## Author

Erik Hollensbe <github@hollensbe.org>
