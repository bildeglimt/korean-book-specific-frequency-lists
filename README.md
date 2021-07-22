# Frequency Lists for Korean Books

This repository contains book-specific and series-specific frequency lists for books in Korean.

**These lists are provided as-is, and I make no guarantees about the quality.**
**A fair amount of guesswork is involved in making them.**
**I will probably not be responding to support requests, but freely admit that I might get nerd-sniped by really good ones.**

## How the lists were created

The frequency lists were created using the Mecab parser that is included in https://konlpy.org/.

The parser produces bits and pieces.
Some are grammatical (particles, conjugations, etc).
Some are vocabulary (nouns, pronouns, verb stems, adjective stems, etc.).

When dealing with verb stems, there will always be multiple stems that all correspond to a single headword (dictionary form).

I've done my best to map verb and adjective stems back to the correct headword using https://github.com/Kyubyong/KoParadigm.

Finally, I validated all the headwords against the frequency list found in this report:
https://www.korean.go.kr/front/reportData/reportDataView.do?mn_id=45&report_seq=1

### What is excluded?

The parser does a good job, but it's not infallible.

1. I exclude everything that is tagged with a "part of speech" that I deemed to be grammar. IANAL (I am not a linguist) so I have no idea if I did this right.
2. I exclude any word or word stem that I was unable to validate against the master frequency list from korean.go.kr
3. For a given book, I exclude any word that is not repeated at least once. In my experience it's easier to just guess these from context or do a lookup on the fly than to try to commit them to memory up front.
4. For books in a series I exclude any words that were included in a frequency list for a book earlier in the same series.

### What are the fields in the CSV?

1. First occurrence - the number of the sentence in which the word was first seen. So lower numbers are earlier in the book.
2. Total occurrences - how many times the word is repeated in the book
3. The word itself
4. The part of speech that the word was categorized as
5. The frequency rating of the word in the master list - lower numbers indicate more common words

### How are they ordered?

Ah, yes.
That.

Normally you'd expect a frequency list to be ordered by frequency, in decending order.

However, the goal is to be able to start reading a book... so I ordered the frequency lists by "first occurrence".

For longer books, you can start studying the list, and the start reading without having studied all 4k or whatever words.

That said, if you import the CSV into a spreadsheet, you can reorder by occurrences if that works better for you.

## How to use a list

My recommendation would be to make flashcards for the words.
Since the goal is to enjoy a book, I wouldn't worry about learning them well enough to use them in conversation, just enough to have a rough idea of the meaning so that the story makes sense.
