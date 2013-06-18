
Unlike the rest of this specification, the rules in this section are
sensitive to whitespace; as such, whitespace may not implicity
separate any pair of components in a rule here.

Note that the unicode character categories can be found online at
<http://www.fileformat.info/info/unicode/category/index.htm>.  The
present release of the tool only supports characters below U+0100;
support for characters outside of the extended ASCII subset of unicode
is planned for a future release.

((LEX)) [[initial letter|lexical]] → <br />
if `codepoint < U+0100` <br />
then Any character in categories *Ll*, *Lm*, *Lo*, *Lt*, *Lu*, or the character `U+0024` (`\$`) <br />
else Any character, excluding categories *Cc*, *Zl*, *Zp*, *Zs*, *Cs*, *Cn*, *Nd*, *Pc*.


((LEX)) [[following letter|lexical]] → <br />
if `codepoint < U+0100` <br />
then Any character in categories *Ll*, *Lm*, *Lo*, *Lt*, *Lu*, *Nd*, or the characters `U+0024` (`\$`), `U+0027` (`'`), and `U+005F` (`_`) <br />
else Any character, excluding categories *Cc*, *Zl*, *Zp*, *Zs*, *Cs*, *Cn*.

((LEX)) [[ascii letter|lexical]] → <br />
Any character in the ranges [`U+0041`,`U+005A`] and [`U+0061`,`U+007A`] --- A-Z and a-z, respectively.

((LEX)) [[character|lexical]] → <br />
Is left underdefined, except to note that it may be any unicode
character except those that conflict with the lexical rule that uses
the character class.  For example, character does not include `\` in
the [[character literal|lexical]] rule.

[[identifier|lexical]] → <br />
  [[initial letter]], { [[following letter]] } <br />
;

[[digit|lexical]] → `0` | `1` | `2` | `3` | `4` | `5` | `6` | `7` | `8` | `9` <br />
;

[[hex digit|lexical]] → [[digit]]  | `a` | `b` | `c` | `d` | `e` | `f` | `A` | `B` | `C` | `D` | `E` | `F` <br />
;

[[numeral|lexical]] → <br />
  [[digit]], { [[digit]] } <br />
;

[[symbolic literal|lexical]] → <br />
  [[numeric literal]] <br />
| [[boolean literal]] <br />
| [[nil literal]] <br />
| [[character literal]] <br />
| [[text literal]] <br />
| [[quote literal]] <br />
;

[[numeric literal|lexical]] → <br />
  [[decimal literal]] <br />
| [[hex literal]] <br />
;

[[exponent|lexical]] → (`E` | `e`), [ `+` | `-`], [[numeral]] <br />
;

[[decimal literal|lexical]] → <br />
  [[numeral]], [ `.`, [[digit]], { [[digit]] } ], [ [[exponent]] ] <br />
;

[[hex literal|lexical]] → (`0x` | `0X`), [[hex digit]], { [[hex digit]] } <br />
;

[[boolean literal|lexical]] → `true` | `false` <br />
;

[[nil literal|lexical]] → `nil` <br />
;

[[character literal|lexical]] → <br />
  `'`, [[character]], `'` <br />
| `'`, [[escape sequence]], `'` <br />
;

[[escape sequence|lexical]] → <br />
  `\\` | `\r` | `\n` | `\t` | `\f` | `\e` | `\a`| `\"`| `\'` <br />
| `\x`, [[hex digit]], [[hex digit]] <br />
| `\u`, [[hex digit]], [[hex digit]], [[hex digit]], [[hex digit]] <br />
| `\c`, [[ascii letter]] <br />
;

[[text literal|lexical]] → <br />
  `"`, { [[character]] | [[escape sequence]] }, `"` <br />
;

[[quote literal|lexical]] → <br />
  `<`, [[identifier]], `>` <br />
;

