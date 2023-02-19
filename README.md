# git-seq is a git extension for creating sequentially named branches.

## Usage

If `git-seq` is in `PATH`, it can be invoked by running `git seq`.

To create a new branch simply run

``` shell
git seq new new-feature-branch
```

This will result in the creation of a new branch with the name
`<user>001-new-feature-branch`. Subsequent branches created with
this command will have increasing sequence numbers.

By default the sequence number is prefixed with the linux system
username, but that is configurable (see Configuration).

## Installation

The easiest way to install `git-seq` is to add the shell-script file
to your path.

## Configuration

The prefix and number padding can be configured on a per-repo basis:

``` shell
git seq config g 5
```

This will set the prefix to `g` and the padding to 5 places, resulting in
branch names such as `g00001-new-feature-branch`.
