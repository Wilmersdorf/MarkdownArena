# MarkdownArena

Website: [https://markdownarena.com](https://markdownarena.com/)

I've created this project when I was looking for a Markdown editor myself.

It compares the following 24 Markdown editors:

TipTap, CodeMirror, ProseMirror, Quill, Plate, Lexical, Monaco, Slate, CKEditor 5, Ace, TinyMCE, Trix, BlockNote, Editor.js, EasyMDE, Toast UI Editor, Remirror, React MD Editor, MDXEditor, Milkdown, Summernote, ByteMD, Novel, Vditor

You can directly sort be NPM downloads, hide inactive editors or see the math support etc.

Each editor also has a live demo directly on the website.

# Learnings

- iframes have a bad rep. Therefore I first tried to implement the website by dynamically adding / removing the css, scripts and body of each individual editor to the main website. This quickly led to an ever growing mountain of hacks: Editors needed help unloading, scripts between different editors would interfer with each other etc. Hence iframes it is.
- Some editors (react based ones) cannot directly use normal CDNs - they need ESM-aware CDNs. When a new version is published on npm (or a new version of some build tool the CDN uses), some ESM-aware CDNs build new files or even rebuild old files. Due to semver notation it can then happen that a library requests a version which is not build yet and an editor that worked yesterday is not working today. I found the most stability using [JSPM](https://jspm.org/) and their [import map generator](https://www.npmjs.com/package/@jspm/generator).

# Notable Mentions

- [marijnh](https://github.com/marijnh) is directly reponsible for 3 editors (ProseMirror, CodeMirror, Wordgard). Another 8 are based on ProseMirror or CodeMirror: TipTap, Toast UI Editor, Remirror, Milkdown, EasyMDE, ByteMD, BlockNote, Novel.
- tiptap's github developer name is [ueberdosis](https://github.com/ueberdosis) (overdose) which I thought was kind of edgy. I guess it's not illegal in Germany to use a German word as your github profile name ... yet.
- [Trix](https://trix-editor.org/) and 37signals for revolutionizing how people work ... with contenteditable.

# Feedback

Please let me know any additional features / missing editors / other feedback:

- Open an issue on here on GitHub (no pull requests).
- Mail [info@markdownarena.com](mailto:info@markdownarena.com)
- Message me on [X](https://x.com/wilmers_dorf)
