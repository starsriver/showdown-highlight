
# `$ showdown-highlight`

 [![Patreon](https://img.shields.io/badge/Support%20me%20on-Patreon-%23e6461a.svg)][patreon] [![PayPal](https://img.shields.io/badge/%24-paypal-f39c12.svg)][paypal-donations] [![AMA](https://img.shields.io/badge/ask%20me-anything-1abc9c.svg)](https://github.com/IonicaBizau/ama) [![Version](https://img.shields.io/npm/v/showdown-highlight.svg)](https://www.npmjs.com/package/showdown-highlight) [![Downloads](https://img.shields.io/npm/dt/showdown-highlight.svg)](https://www.npmjs.com/package/showdown-highlight) [![Get help on Codementor](https://cdn.codementor.io/badges/get_help_github.svg)](https://www.codementor.io/johnnyb?utm_source=github&utm_medium=button&utm_term=johnnyb&utm_campaign=github)

> A Showdown extension for highlight the code blocks.

## :cloud: Installation

You can install the package globally and use it as command line tool:


```sh
$ npm i -g showdown-highlight
```


Then, run `showdown-highlight --help` and see what the CLI tool can do.


```
$ showdown-highlight --help
Usage: showdown-highlight [options]

A Showdown extension for highlight the code blocks.

Options:
  -f, --foo <foo>  Dummy argument
  -v, --version    Displays version information.
  -h, --help       Displays this help.

Documentation can be found at https://github.com/IonicaBizau/showdown-highlight#readme.
```

## :clipboard: Example


Here is an example how to use this package as library. To install it locally, as library, you can do that using `npm`:

```sh
$ npm i --save showdown-highlight
```



```js
const showdown = require('showdown')
    , showdownHighlight = require("showdown-highlight")
    ;

// After requiring the module, use it as extension
let converter = new showdown.Converter({
    extensions: [showdownHighlight]
});

// Now you can Highlight code blocks
let html = converter.makeHtml(`
## Highlighting Code with Showdown

Below we have a piece of JavaScript code:

\`\`\`js
function sayHello (msg, who) {
    return \`\${who} says: msg\`;
}
sayHello("Hello World", "Johnny");
\`\`\`
`);

console.log(html);
// <h2 id="highlightingcodewithshowdown">Highlighting Code with Showdown</h2>
//
// <p>Below we have a piece of JavaScript code:</p>
//
// <pre><code class="js language-js"><span class="hljs-function"><span class="hljs-keyword">function</span> <span class="hljs-title">sayHello</span> (<span class="hljs-params">msg, who</span>) </span>{
//     <span class="hljs-keyword">return</span> <span class="hljs-string">`<span class="hljs-subst">${who}</span> says: msg`</span>;
// }
// sayHello(<span class="hljs-string">"Hello World"</span>, <span class="hljs-string">"Johnny"</span>);
// </code></pre>
```

## :memo: Documentation

For full API reference, see the [DOCUMENTATION.md][docs] file.

## :yum: How to contribute
Have an idea? Found a bug? See [how to contribute][contributing].


## :moneybag: Donations

Another way to support the development of my open-source modules is
to [set up a recurring donation, via Patreon][patreon]. :rocket:

[PayPal donations][paypal-donations] are appreciated too! Each dollar helps.

Thanks! :heart:


## :scroll: License

[MIT][license] © [Ionică Bizău][website]

[patreon]: https://www.patreon.com/ionicabizau
[paypal-donations]: https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=RVXDDLKKLQRJW
[donate-now]: http://i.imgur.com/6cMbHOC.png

[license]: http://showalicense.com/?fullname=Ionic%C4%83%20Biz%C4%83u%20%3Cbizauionica%40gmail.com%3E%20(http%3A%2F%2Fionicabizau.net)&year=2016#license-mit
[website]: http://ionicabizau.net
[contributing]: /CONTRIBUTING.md
[docs]: /DOCUMENTATION.md