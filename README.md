# statsd-erlang

an Erlang client for [statsd](https://github.com/etsy/statsd) that is based on OTP's gen_server behaviour.
Adapted for ejabberd.

## Usage

Add statsd-erlang to your modules configuration section in ejabberd.cfg like this:

```erlang
{statsd, ['localhost', 8125]}
```

```erlang
statsd:increment("foo.bar").
statsd:count("foo.bar", 5).
statsd:timing("foo.bar", 2500).
```

## Development

To compile, make sure that you have the ejabberd source files in the same parent directory as statsd-erlang and run `./build.sh`.

## Author

Original author: Dominik Liebler <liebler.dominik@googlemail.com>
Ejabberd adjustements by: Michael Weibel <michael@mila.com>

## License

(The MIT License)

Copyright (c) 2012 Dominik Liebler

Permission is hereby granted, free of charge, to any person obtaining
a copy of this software and associated documentation files (the
'Software'), to deal in the Software without restriction, including
without limitation the rights to use, copy, modify, merge, publish,
distribute, sublicense, and/or sell copies of the Software, and to
permit persons to whom the Software is furnished to do so, subject to
the following conditions:

The above copyright notice and this permission notice shall be
included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED 'AS IS', WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.
IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY
CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT,
TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE
SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
