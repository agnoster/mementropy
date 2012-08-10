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
