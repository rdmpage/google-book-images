# Google Books images

Notes on how to achieve small image size like Google Books. For background read:

 Adam Langley, Dan S. Bloomberg, "Google Books: making the public domain universally accessible", Proc. SPIE 6500, Document Recognition and Retrieval XIV, 65000H (2007/01/29); doi: 10.1117/12.710609; http://dx.doi.org/10.1117/12.710609

A PDF of this document is in this repository.

## Requirements

Use [jbig2enc](https://github.com/agl/jbig2enc) to compress images (and also convert them to B&W). This library in turn depends on [leptonica](http://leptonica.com).

## Example

Given the page image from BHL (34565786.jpeg)

```
jbig2 -s -S -p -v -O 34565786.png 34565786.jpeg 
```

will create a smaller PNG. For darker images you may need to tweak the T parameter, e.g. use -T 100.

Before:
![Example](https://github.com/rdmpage/google-book-images/raw/master/34565786.jpeg)

After
![Example](https://github.com/rdmpage/google-book-images/raw/master/34565786.png)

