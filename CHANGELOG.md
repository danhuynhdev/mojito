# Changelog

## 0.2.2 (2019-04-46)

Fixed a bug where long requests could exceed the given timeout without
failing (#17).  Thanks for the report,
[mischov](https://github.com/mischov)!

Improved documentation about receiving `:tcp` and `:ssl` messages.
Thanks for the report,
[axelson](https://github.com/axelson)!

Removed an extra `Task` process creation in `Mojito.Pool.request/2`.

## 0.2.1 (2019-04-23)

Refactored `Mojito.request/5` so it doesn't spawn a process.  Now all
TCP messages are handled within the caller process.

Added `Mojito.request/1` and `Mojito.Pool.request/2`, which accept a
`%Mojito.Request{}` struct as input.

Removed dependency on Fuzzyurl in favor of built-in URI module.

## O.2.0 (2019-04-19)

Messages sent by Mojito now contain a `:mojito_response` prefix, to allow
processes to select or ignore these messages with `receive`.
Thanks [@AnilRedshift](https://github.com/AnilRedshift)!

Upgraded to Mint 0.2.0.

## 0.1.1 (2019-03-28)

`request/5` emits better error messages when confronted with nil or blank
method or url.  Thanks [@AnilRedshift](https://github.com/AnilRedshift)!

## 0.1.0 (2019-02-25)

Initial release, based on [Mint](https://github.com/ericmj/mint) 0.1.0.

