# emojilist

This package provides a full list of **fully qualified** emoji characters as constants using data from [the Unicode emoji test data](https://unicode.org/Public/emoji/16.0/emoji-test.txt). That's it. 

The `emojilist.go` file within this package is **auto-generated** using `go generate`, see [codegen](codegen/codegen.go).

**Usage:**

```go
import emojilist "github.com/zewebdev1337/emojilist/v16"

fmt.Println(emojilist.EMOJI_GRINNING_FACE) // Output: 😀
```

**Naming:**

Emoji constants are named following the pattern `EMOJI_<EMOJI_NAME>`, where `<EMOJI_NAME>` is the emoji's descriptive name from the Unicode emoji test data, converted to uppercase and with spaces and special characters replaced by underscores. For example:

* "grinning face" becomes `EMOJI_GRINNING_FACE`
* "thumbs up light skin tone" becomes `THUMBS_UP_LIGHT_SKIN_TONE`
* "keycap *" becomes `KEYCAP_STAR`

**Manually updating (or downgrading) the Emoji List:**

If this package is not updated or you need to follow constraints from an older emoji version (and manage to find the txt files for versions below v11), you can manually update the emoji list to a specific Unicode version. Simply update the version number at the top of the [emojilist](emojilist.go) file to point to the desired emoji test data file and run `go generate` in the root of the project to regenerate the file and directory with the updated emoji data.

**License:**

MIT