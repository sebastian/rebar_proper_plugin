

#rebar_proper_plugin#


Copyright (c) 2012 Andrzej Śliwa.

__Version:__ 0.1


![rebar plus proper](https://raw.github.com/andrzejsliwa/rebar_proper_plugin/master/priv/rebar_plus_proper.png)

**rebar_proper_plugin** is a simple rebar plugin for handling PropEr tests.

[![Build Status](https://secure.travis-ci.org/andrzejsliwa/rebar_proper_plugin.png?branch=master)](http://travis-ci.org/andrzejsliwa/rebar_proper_plugin)

Main features:

- run all prop_* tests
- check all specs of module or explicit functions in

Note: This is a work in progress, see the
[TODO](http://github.com/andrzejsliwa/rebar_proper_plugin/blob/master/TODO.md) for more
informations on what still need to be done.

## License
See [LICENSE](http://github.com/andrzejsliwa/rebar_proper_plugin/blob/master/LICENSE) file for licensing information.

## Installation

Download the sources from our [Github
repository](http://github.com/andrzejsliwa/rebar_proper_plugin)

Important!: Plugin tested with **rebar 2.0.0 R15B02 20121106_155240 git 2.0.0-237-ga2fb8fd**

To generate doc, run 'make doc'.

To use plugin:Add it to own '~/.erlang' file
<pre>code:add_pathz("/Users/andrzejsliwa/.erlang_tools/deps/proper/ebin").</pre>

Add it to own your rebar config<pre>%% define deps repo of plugin
{deps, [
    ...
	{rebar_proper_plugin, ".*", {git, "git://github.com/andrzejsliwa/rebar_proper_plugin.git", {branch, "master"}}}
]}.
%% define plugin usage
{plugins, [rebar_proper_plugin]}.
%% define PropEr options
{proper_opts, [{numtests, 200}]}.
%% define function to check (MFA format)
{proper_check_spec, [{example, is_empty, 1}]}.
%% or define just module {proper_check_spec, [example]}.</pre>

## Basic usage

The basic usage of rebar_proper_plugin (after 'rebar compile') is:<pre>$ rebar proper
Testing example:pop/1
........................................................................................................................................................................................................
OK: Passed 200 test(s).
...</pre>

## Contribute

For issues, comments or feedback please [create an
issue](http://github.com/andrzejsliwa/rebar_proper_plugin/issues).

### Notes for developers

If you want to contribute patches or improve the doc, you will need to
build hackney using the `rebar.dev.config`  file. It can also be built
using the **Makefile**:<pre>$ make dev       ; # compile & get deps
$ make dev_clean ; # clean all files</pre>


##Modules##


<table width="100%" border="0" summary="list of modules">
<tr><td><a href="http://github.com/andrzejsliwa/rebar_proper_plugin/blob/master/doc/rebar_proper_plugin.md" class="module">rebar_proper_plugin</a></td></tr></table>

