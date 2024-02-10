## Display Currently Selected Lang
- Display current language above the *Change Language* button.
- Updates itself when user changes language by grabbing the *current language* class variable and using its string.
- Also displays correct lang on start-up by loading the variable after it has been updated with config info.
## Sentence Mode now Phrase Mode
- Sentence mode is not very useful.
- Phrase mode looks up the entire string, rather than individual words. Useful for adverbial phrases, etc.
- Saving phrases overwrites most recent save, but appears only to do on the GUI.
	- ~~Probably because the saved temp dictionary isn't being updated.~~
	- It has nothing to do with phrases. There's a bug in the GUI save function. Now fixed.
## Add Plurals to Cards and Search
This will be hard.