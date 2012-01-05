# Simple SAX-based XML2JSON Parser.

It does not parse the following elements: 

* CDATA sections
* Processing instructions
* XML declarations
* Entity declarations
* Comments

## Installation 
`npm install xml2json`

## Usage 
```javascript
var parser = require('xml2json');

var xml = "<foo>bar</foo>";
parser.toJson(xml, options, function(err, data){
	if(err) throw err;
	console.log(data);
}); 
```
* if you want to get the Javascript object then you might want to invoke parser.toJson(xml, {object: true},callback);
* if you want a reversible json to xml then you should use parser.toJson(xml, {reversible: true}, callback);


## License
Copyright 2011 BugLabs Inc. All rights reserved.
