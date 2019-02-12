
# react-native-markdown-formatter

## Getting started

Install the node module:

`yarn add react-native-markdown-formatter`

or with npm:

`npm install --save eact-native-markdown-formatter`

Then see Usage for futher details


## Usage
```javascript
import RNMarkdownFormatter from 'react-native-markdown-formatter';

Import `RNMarkdownFormatter` from `react-native-markdown-formatter`:

```

In your `Component`'s `render()` method you can then render markdown via JSX e.g.

```

var markdownFormatterRegex = [
		{
					type: 'bold',
					styles: [styles.boldText],
					pattern: '**',
					patternType: 'symmetric',
					groups: 1, 
			},
			{
					type: 'italic',
					styles: [styles.italicText],
					pattern: '_',
					patternType: 'symmetric',
					groups: 1,              
			},            
			{
					type: 'hyperlink',
					styles: [styles.hyperlinkText],
					pattern: '[]()',
					patternType: 'asymmetric',
					groups: 2,              
			},            
];

//TextBlock styles
let textBlockComputedStyle = [];
textBlockComputedStyle.push({
		fontSize: 14,
		color: "red",
});

let text = "This _is_ **Bold_italic_** text, This is **_Italic within Bold_** text (bold italic text), This is more than one hyperlink text => [Adaptive Cards](http://adaptivecards.io) [Adaptive Cards](http://adaptivecards.io), This is a bullet list - Item 1\r- Item 2\r- Item 3\r";

<MarkdownFormatter 
	defaultStyles={textBlockComputedStyle} 
	numberOfLines={numberOfLines} // 1 or 0
	text={text} 
	regexArray={markdownFormatterRegex}/>

```
  