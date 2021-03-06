exml
====

[![Build Status](https://secure.travis-ci.org/esl/exml.png)](http://travis-ci.org/esl/exml)

**exml** is an Erlang library helpful with parsing XML streams
and doing some basic XML structures manipulation.

Building
========

**exml** is a rebar-compatible OTP application, run `make` or
`./rebar compile` in order to build it.

As a requirement, development headers for expat library are
required.

Using
=====

**exml** can parse both XML streams as well as single XML
documents at once.

At first, a new parser instance must be created:

```erlang
{ok, Parser} = exml:new_parser().
```

Then, one must feed the parser with an XML document:

```erlang
ok = exml:parse(Parser, <<"<my_xml_doc/>">>, 1).
```

