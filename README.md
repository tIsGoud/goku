# My Goku / Karabiner configuration

This repository holds my configuration files for Karabiner-Elements.

It contains the fully documented Goku file (karabiner.edn) as well as the generated file (karabiner.json).

In my configuration I remapped some specific "PC" keys for my Qisan Magicforce 68 keyboard.

A cleaned version is also available, I created this version for my colleague with just a Macbook Pro. The same generic functionality.

I wrote two blogposts with background information on the choices made and tools explored:

- [Keyboard redefined - part 1](https://tisgoud.nl/2020/09/keyboard-redefined-part-1/)
- [Keyboard redefined - part 2](https://tisgoud.nl/2020/09/keyboard-redefined-part-2/)

## Shortcuts, remappings and automations

The following sections give an overview of the shortcuts, mappings and automations

### Qisan Magicforce68 keyboard specific settings

The specific settings for my compact Qisan Magicforce68 keyboard

| Shortcut         | Keystroke      | Function                        |
| :--------------- | :--------------| :------------------------------ |
| left-option      | left-&#x2318;  | swapping option and command     |
| left-command     | left-&#x2325;  | swapping command and option     |
| Escape           | \`             | Escape to \`                    |
| Shift+Escape     | \~             | Shift + Escape to ~             |
| right-Command    | &#x2318; + Tab | Toggle current and previous app |
| right-Option     | &#x2318; + \~  | Cycle app windows               |

This section is removed in the cleaned version.

### Apple keyboard specific settings

The specific Apple keyboard setting involve the use of the 'fn' or function key. I was unable to address the function key on my Qisan keyboard.

| Shortcut | Keystroke                   | Function    |
| :------- | :-------------------------- | :---------- |
| fn + l   | &#x2318; + &#x2303; + q     | Lock screen |
| fn + z   | &#x2318; + &#x2325; + Eject | Sleep       |

### Keychron K1 keyboard specific settings

The Keychron K1 keyboard setting has a special keys to take a screenshot right next to it is a key with a microphone that sends out fn + spacebar. I use this key to silently take a screenshot.

| Shortcut   | Keystroke     | Function                  |
| :--------- | :------------ | :------------------------ |
| microphone | fn + spacebar | Call silent screencapture |

### Generic shortcuts

You might wonder why there are so many hyper-keys, yes it is to much but I'm still figuring out which hyperkey location is most convenient. The position of your hands above the keyboard is an important factor in this. Using the capslock as hyper key is also a good option due to the size of the key.

| Shortcut         | Keystroke                   | Function                         |
| :--------------- | :-------------------------- | :------------------------------- |
| Capslock         | Escape                      | hyper-key                        |
| Tab              | Tab / fn18                  | Hammerspoon hyper-key            |
| e                | e                           | hyper-key                        |
| Command (l\|r)   | &#x2318; + Tab              | Toggle current and previous app  |
| Option (l\|r)    | &#x2318; + \~               | Cycle app windows                |
| Control (l\|r)   | &#x2303; + Tab              | Cycle app tabs                   |
| left-Shift       | &#x2325; + left-Arrow       | Move cursor one word left        |
| right-Shift      | &#x2325; + right-Arrow      | Move cursor one word right       |
| e + m            | &#x2318; + &#x2303; + Space | Open Emoji picker                |
| Capslock + l     | &#x2318; + &#x2303; + q     | Lock screen                      |
| Capslock + z     | &#x2318; + &#x2325; + eject | Sleep                            |
| Capslock + m     | &#x2318; + &#x2303; + Space | Open Emoji picker                |
| Capslock + u     |                             | Toggle System UI Sound Effects*  |
| Capslock + \     |                             | Open Finder                      |
| Capslock + s     |                             | Open Safari                      |
| Capslock + f     |                             | Open Firefox                     |
| Capslock + k     |                             | Open Kubernetic                  |
| Capslock + g     |                             | Open Google Chrome               |
| Capslock + t     |                             | Open iTerm                       |
| Capslock + y     |                             | Open Typora                      |
| Capslock + v     |                             | Open VSCodium                    |
| Capslock + 4     |                             | Silent screenshot to clipboard   |
| Capslock + 5     |                             | Screenshot and recording options |
| Capslock + arrow |                             | Move mouse fast                  |
| left-Option + s  |                             | Safari: Save tabs to markdown**  |
| left-Option + s  |                             | Chrome: Save tabs to markdown**  |
| right-Option + o |                             | Finder: Open in VSCodium***      |
| Capslock + t     |                             | VSCodium: Open terminal pane     |
| Capslock + h     |                             | VSCodium: Snippet to clipboard   |

In my current configuration I disabled the left- and right-shift options to move the cursor one word to the left or right. Too many typing errors.

\* See [Silence is foo](https://tisgoud.nl/2020/10/silence-is-foo/)

\*\* See [Saving the Yak browser-trail](https://tisgoud.nl/2020/04/saving-the-yak-browser-trail/)

\*\*\* See [Open in VCodium](https://tisgoud.nl/2019/09/open-in-vscodium/)

### Special characters

Three simlayers have been added to make it easier to type these special vowel characters.

- Slash ('/') + vowel = vowel + acccent aigu
- Semicolon (';') + vowel = vowel + umlaut
- Backslah ('\') + vowel = vowel + accent grave

For example: '/' + 'a' = á

### Example shortcuts

Some shortcuts to test stuff.

| Shortcut      | Keystroke                   | Function                    |
| :------------ | :-------------------------- | :-------------------------- |
| o + s         |                             | Open Safari (example)       |
| o + t         |                             | Type some text (example)    |
| o + b         |                             | Play beep sound (example)   |
| o + p         |                             | Play Purr sound (example)   |
| o + k         |                             | Play Tink sound (example)   |
| e + m         | &#x2318; + &#x2303; + Space | Open Emoji picker (example) |
| Spacebar + \  |                             | Open Finder (example)       |
| Spacebar + p  |                             | Open Preview (example)      |

## Run Goku -c

When the 'karabiner.edn' file is not located in the directory '~/.config' you can run the shell script 'gokuc.sh' which uses the config file from the current directory.

```shell
#!/bin/bash

# Run goku with the karabiner.edn file from the current directory
goku -c $PWD"/karabiner.edn"
```

Output:

```shell
goku$ ./gokuc.sh
Done!
```
