Convert library
Encoders and decoders for converting between different data representations, including JSON and UTF - 8.

In addition to conveters for common data representations, this library provides support for implementing converters in a way which makes them easy to chain and to use with stream. 

To use this library in your code:
import 'dart:convert';

Two vommonluy used converters are the top-level instances of JsonCodec and Utf8Codec, named json and utf8, respectovely.

JSON 
JSON id a simple text format for representing structured onjects and collections.
A JsonCodec rncedes JSON objects to strings and decodes strings to JSON object. The json encoder/docoder transforms between string and object structures, as lists and maps, using the JSON format.

The json is the default implementation of JsonCodec.

Exemples

var encoded = json. encode([1, 2, {"a" : null }]);
var decoded = json.decode('["foo", { "bar": 499}]');

For more informatin, see also JsonEncoder and JsonDeconder. 

UTF - 8 
A Utf8Codec rncodes strings to UTF - 8 code units (bytes) and decodes UTF - 8 codef units to string. 

The utf8 is the default implementation of UTF8Codec.
Example: 
var encoded = utf8.encode('Îñţérñåţîöñåļîžåţîờñ');

ASCII 
An AsciiCodec encodes strings as ASCII codes stored as bytes and decodes ASCII bytes to string. Not all characters can be represented as ASCII, so not all string can be successfully converted.

The ascii is the default implementation of AsciiCodec.

Example: 

var encoded = ascii.encode('This is ASCII!'); 
var decoded = ascii.decode([0x54, 0x68, 0x69, 0x73, 0x20, 0x69, 0x73, 0x20, 0x41, 0x53, 0x43,
											0x49, 0x49, 0x21]);

Base64
A Baset64Codec encodes bytes using the defult base 64 alphabet, decodes using both the base 64 and base64url alphabets, does not allow invalid characters and requires padding.

The base64 is the default implementation of Base64Codec

Example: 
var encoded = base64.encode([0x62, 0x6c, 0xc3, 0xa5, 0x62, 0xc3, 0xa6, 0x72, 0x67, 0x72, 0xc3, 0xb8, 0x64]); 
var decoded = base64.decode('YmzDpWLDpnJncsO4ZAo=');

For more information, see also Base64Encoder and Base64Decoder.

Converters 
Converters are often used with streams to treansform the data that comes therough the stream as it becomes avilable. The following coder uses two converters. The first is a UTD - 8 decoder, which converts the data from bytes to UTF - 8 as it is read from a file, The secend is an instance of LineSpolitter, which splits the data on newline boundaries. 

```dart
const showLineNumbers = true; var lineNumber = 1; var stream = File('quotes.txt').openRead(); stream.transform(utf8.decoder) .transform(const LineSplitter()) .forEach((line) { if (showLineNumbers) { stdout.write('${lineNumber++} '); } stdout.writeln(line); });
```

See the documentation for the Coderc and Converter classes for inforamtion about coreating your own converters. 

HTML Escape 
HtmlEscape converter  escapes characters with special meanung un HTML. The converter finds characters that are signidicant in HTML source and replaces them with corresponding HTML entities.

Costom escape modes can be created using the HtmlEscapeMode.HtmlEscapeMode constructor.
