# PopClip Extensions

This repo contains several useful PopClip extensions.

Some can be installed directly by installing the whole folder. The other can be simply copy and install as they are [snippets](https://github.com/pilotmoon/PopClip-Extensions/blob/master/README.md).
Select that text below, and you’ll see an “Install Extension” action in PopClip. Just install it!

###  Fast Open JIRA Links via PopClip

See the `jira/` directory.

### Copy `bat` output to clipboard

It removes the leading line number and | format when you copying a `bat` output. With this you will never miss `cat`!
If you want, feel free to add more apps to `required apps` where this extension should be actived.
To get the app ID, use `osascript -e 'id of app "iTerm"'`

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
