---
date: 2026-01-06
tags:
  - classics
title: Typing Latin Macrons and Breves
---
# Typing macrons and breves on a Windows machine
As part of my transcription of [North & Hillard's Latin Prose Composition](https://github.com/jacknoutch/north_hillard_latin_vocabulary/tree/master), I have needed to type macrons and breves over all five vowels (and their capitals) to accurately transcribe the text. Copy and paste is too slow.

I use a Windows machine, which has the drawback of not allowing for combining keystrokes such as is possible on Mac.

The simplest way to type many characters with diacritics is to use Alt codes. (Make sure Num lock is on. Holding down Alt, type the corresponding number for the character on the number pad.)

However, Alt codes above 255 only work with some programs. They can be typed in Word, but not in Chrome, Edge, VS Code, etc. The vowels with breves and macrons all have Alt codes over 255.

My workaround is to use [AutoHotkey](https://www.autohotkey.com/) with the following script. This _still_ doesn't work in VS Code with Markdown files (though it does with, e.g., txt files in VSC). This is because VSC seems to "steal" the keystrokes before AutoHotkey is able to register and replace them.

But this works enough for me to type in the browser and edit the files on Github.

The shortcuts work as follows: type the letter (upper or lowercase) then `=` for a macron or `+` for a breve. Eg. `a+` becomes `ă` and `O=` becomes `Ō`.

```
#Requires AutoHotkey v2.0
:*?:a+::ă
:*?:a=::ā
:*?:e+::ĕ
:*?:e=::ē
:*?:i+::ĭ
:*?:i=::ī
:*?:o+::ŏ
:*?:o=::ō
:*?:u+::ŭ
:*?:u=::ū
:*?:A+::Ă
:*?:A=::Ā
:*?:E+::Ĕ
:*?:E=::Ē
:*?:I+::Ĭ
:*?:I=::Ī
:*?:O+::Ŏ
:*?:O=::Ō
:*?:U+::Ŭ
:*?:U=::Ū
```

### The Alt codes

For each vowel, there are four variations: Upper and lower case macron, Upper and lower case breve. These four variations are consecutive in both Unicode and the Alt code.

So, for `a` the Alt codes are `256 Ā`, `257 ā`, `258 Ă`, `259 ă`.

The first Alt code for each of the vowels' quartets is: - `a 256` - `e 274` - `i 298` - `o 332` - `u 362`

A fuller table (without capitals) is given below in a more readable format.

|name|graph|alt code|unicode|
|---|---|---|---|
|a breve|ă|259|U+0103|
|a macron|ā|257|U+0101|
|e breve|ĕ|277|U+0115|
|e macron|ē|275|U+0113|
|i breve|ĭ|301|U+012D|
|i macron|ī|299|U+012B|
|o breve|ŏ|335|U+014F|
|o macron|ō|333|U+014D|
|u breve|ŭ|365|U+016D|
|u macron|ū|363|U+016B|