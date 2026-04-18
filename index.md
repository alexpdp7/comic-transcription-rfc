# Comic transcription RFC

This document is a request for comments about a comic transcription standard.

The purpose of the standard is to help organizations that want to make transcriptions of comics for accessibility purposes.

## Writing the transcription

Prepare the transcription of a comic in a single file formatted as Markdown.

Write all Markdown text with one sentence per line.

Do not embed HTML nor use images.

Reduce the use of Markdown formatting, favor text that conveys the comic when read aloud.

Use external links *only* for additional information.

### Headers

The transcription should have a single top-level header (`#`) with the comic title.

For comics with no other structure, the following headers should be used:

* Second level headers for each page, such as `## Page 3`
* Third level headers for each panel, such as `### Panel 2`

### Additional sections

#### Transcription notes

Immediately after the title, the transcription can include a second level header `## Transcription notes`.

The transcription notes section can include the following third level sections:

* "Format", describing the physical comic format.

The transcription notes section can include any other third level sections with any required explanation to enjoy the comic, such as:

* Notes about how certain comic characteristics are transcribed, such as onomatopeia, different illustration styles, or graphical elements.
* Notes about the comic structure, such as parts, chapters, or others.

The transcription should try to avoid relying on the reader having read the transcription notes or remembering them completely.

#### Prefaces and postfaces

Use a second level header `## Preface` to organize any content that comes before the main content of the comic.

Use third level headers such as:

* External cover (or cover, if there is no internal cover)
* Internal cover
* Inner sleeve

Conversely, use another second level header `## Postface` for content after the main content.

Use third level headers such as:

* External end cover

## Transcribing

Image descriptions should be as brief as possible while including all information necessary to enjoy the comic, including:

* The point of view of the panel or the framing.
  For example, a landscape, a portrait of a character, a detail of an object, the positions of characters relative to each other, and others.

* Physical descriptions of characters, including their clothing.
  Do not repeat physical descriptions.

### Describing sequences of actions

Panels can depict a sequence of actions, including dialogue lines, actions, and reactions.

The transcription should reproduce the sequence of actions and can fragment the image description to follow the sequence of actions.

For example, although in general you describe the image at the beginning of the panel description, you might describe a character's facial expression only after the dialogue line they are reaction to.

Any action should disambiguate clearly which character performs the action.
You might omit the character name if there are no other characters in the scene.

Try to refer to characters by the name that most characters address them as consistently.

You can use their name before the character name is introduced in the comic.
However, use something else if revealing the character name could spoil a surprise.

If the other characters change how they address the character during the comic (for example, a character gains a nickname), then the transcription should start referring to the character with the new name too in the same point.
If the change of name is not obvious, then include a transcription note to emphasize this.

### Transcribing notes

Notes included in the comic should be clearly labelled as such, but integrated in the flow of the text.

For example, if a dialogue has an asterisk on a word and there's a note on the margin explaining the word, you can transcribe the note as a separate paragraph, prefixed by "note about x:", "translator's note about x:", or similar.
You can omit the asterisk for the transcription if the result is clear enough.

### Transcription notes

You might add additional notes required to enjoy the comic.
Transcription notes should be prefixed by "transcription note:" or similar.

## Generating HTML

Use [Pandoc](https://pandoc.org/) to convert the Markdown file into HTML with the following command:

```
pandoc -s transcription.md -o transcription.html
```

Distribute both the Markdown file (to enable editing the transcription) and the HTML (for readers).

## Rationale

* Reading the transcription should require as little knowledge and resources as possible.
* The transcription should be usable with a screenreader.
* Readers should be able to navigate through the transcription quickly.
* Transcribing should require as little technical knowledge as possible.
* The transcription should be usable without an Internet connection.

## TODO

* Cross references
* Use of emphasis
* Punctuation and capitalization
* Use of foreign language
