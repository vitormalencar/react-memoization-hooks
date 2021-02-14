ur code, you agree to license your contribution under the [MIT license](../license).
 Use `rem` unit instead of `px`
- Use lowercase and shorthand hex values, i.e. `#fff`
- Use one discrete selector per line in multi-selector rulesets
- Include a single space after colon and after each comma
- Separate each ruleset by a blank line
- Don't use prefixes, there is a task to generate this automatically

```sass
.selector-a,
.selector-b,
.selector-c,
.selector-d[type='text']
	box-sizing: border-box
	color: #333
	content: ''
	display: inline-block
	font-family: 'Helvetica-Neue', 'Helvetica', 'Arial', sans-serif
	margin-bottom: 0
	margin-left: 5.0rem

	.other-selector-a
		background: #fff

		.other-selector-b
			background: #fff

		&.increasing-the-specificity
			color: #000
```

*NOTE: The best way to learn about that is to just install it and give it a try on your code. This project uses an `.editorconfig` file, which most editors support, to enforce these coding standards.*

## Test

First install [Node.js](https://nodejs.org/en/download/). Now install all the dependencies, run `npm install` from the project directory. Once you have the dependencies installed, run `npm test`.

## Code of Conduct

Help us keep this project open and inclusive. Please read and follow our thoughts on [Code of Conduct](http://confcodeofconduct.com/).

## License

By contributing yo