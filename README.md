# wordle-assistant
Python CLI assistant for Wordle players

```console
$ wordle --help
Wordle Assistant.

Usage:
  wordle: list all 5-letter words

  wordle wrongletters: same, but remove words that contain any of the wrong letters
  Caution: this parameter cannot be empty.
  Example: wordle tyrch

  wordle wrongletters pattern: same, but keep only words that match the given (Python) regex pattern
  Use a dash (-) character if you do not have a pattern yet
  Examples:
    wordle tyrch g.e.s
    wordle tyrch ^g
    wordle tyrch s$
    wordle tyrch '^g[ue]'

  wordle wrongletters pattern misplaced_letters ...: same but takes misplaced letters into account
  There are multiple supported notations:
  - positions range from 1 to 5
  - "3g" or "g3" means that a "g" at position 3 was considered misplaced
  - "^u" means that a "u" at the start of the word was considered misplaced
  - "e$" means that an "e" at the end of the word was considered misplaced
  - ".s.u." means that an "s" at position 2 and a "u" at position 4 were considered misplaced
  Examples:
    wordle tyrch - 3g ^u e$ .s.u.
    wordle tyrch '^g[ue]' 3g ^u e$ .s.u.
```
