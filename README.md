# MemEntropy - a client-side XKCD 936 password generation

> For a password, you want memorable entropy

Now, in JavaScript! All the code runs client-side, so your password never gets sent over the wire in plaintext.

Good for you, good for the servers.

## Corpus

The corpus of `words.txt` is provided by taking a [list of English words by frequency][wordlist] and restricting it to words with 5 letters or more, leaving 8340 of the original 10000 words. This comes out to about 13 bits of entropy per word choice, which actually increases the strength of passwords using this beyond what XKCD suggested. In fact, 4-word passwords from this corpus have 52 bits of entropy; even at a million guesses per second, it would take over 150 years to search this space exhaustively -- that's close to 300 times more secure!

## How it works

We pick 4 words from the corpus at random and show them. Clicking the input field selects the whole thing. Just press whatever key combination your system uses for "Copy to Clipboard" and — hey presto! — a nice, secure password is in your clipboard.

![XKCD comic on password strength](http://imgs.xkcd.com/comics/password_strength.png)

[wordlist]: http://www.cs.utexas.edu/users/ear/cs378NLP/EnglishWordFrequencies.txt
[xkcd img]: http://imgs.xkcd.com/comics/password_strength.png


## Contributing

Under MIT license. Go nuts. Fork, add issues, and submit pull requests to your heart's content!

## MIT License

Copyright (C) 2012 by Isaac Wolkerstorfer

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.

