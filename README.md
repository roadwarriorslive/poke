# Poke
[![npm](https://img.shields.io/npm/v/poke-site.svg)](https://www.npmjs.com/package/poke-site)
[![Build Status](https://travis-ci.org/adamisntdead/poke.svg?branch=master)](https://travis-ci.org/adamisntdead/poke)
[![JavaScript Style Guide](https://img.shields.io/badge/code_style-standard-brightgreen.svg)](https://standardjs.com)

A simple tool to check your site for broken links, media, iframes, stylesheets, scripts, forms or metadata.
Will also test for images over 500kb.

## Usage

1. Install it: `npm install -g poke-site`
2. Run it: `poke <url>` where <url> is the base of the site you want to test
3. Profit

```
  Usage: poke [options] <url>

  Options:

    -V, --version               output the version number
    -r, --retry [value]         broken links are retried with new hostname
    -s, --shallow               do not check pages rooted outside of provided url
    -m, --max-img-size [value]  looks for images that are over this size in kb. Defaults to 500
    -q, --quiet                 Supress warnings and loading messages(for ci)
    -m, --method [head|post]    HTTP method used to check links, defaults to head
    --skip-images               Skip the image checks
    --skip-duplicates           Skip the duplicate page checks
    -h, --help                  output usage information
```

Sample Output

![Sample Output](https://raw.githubusercontent.com/adamisntdead/poke/master/test/public/output.png)

Usually you should run with the `--shallow` option, otherwise you might get into checking for broken links in twitter or another external site, which you may not want!

## License

MIT
