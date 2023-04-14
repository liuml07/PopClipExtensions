# PopClip Extensions

This repo contains several useful PopClip extensions.

Some can be installed directly by installing the whole folder. The other can be simply copy and install as they are [snippets](https://forum.popclip.app/t/introducing-extension-snippets/309). 
Select that text below, and you’ll see an “Install Extension” action in PopClip. Just install it!

###  Fast Open JIRA Links via PopClip

See the `jira/` directory.

### Copy `bat` output to clipboard

It removes the leading line number and | format when you copying a `bat` output. With this you will never miss `cat`!


```
// # popclip
// name: CopyBat
// icon: circle filled BAT
// description: Remove `bat` formatter from the selected text.
// language: javascript
// required apps: [com.googlecode.iterm2]
pasteboard.text = popclip.input.text
  .split('\n')
  .map(line => line.replace(/.*│/g, ''))
  .join('\n');
```
