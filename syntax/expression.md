[[expression]] → <br />
  `self` <br />
| [[name|expression]] <br />
| [[old name|expression]]  <br />
| [[symbolic literal|expression]] <br />
| `(`, [[expression]], `)` <br />
| [[unary operator|expression]], [[expression]] <br />
| [[expression]], [[binary operator|expression]], [[expression]] <br />
| `let`, [[local definition|statement]], { `,`, [[local definition|statement]] }, `in`, [[expression]] <br />
| `forall`, [[bind list|pattern]], `@`, [[expression]] <br />
| `exists`, [[bind list|pattern]], `@`, [[expression]] <br />
| `exists1`, [[bind|pattern]], `@`, [[expression]] <br />
| `iota`, [[bind|pattern]], `@`, [[expression]] <br />
| `lambda`, [[type bind list|pattern]], `@`, [[expression]] <br />
| `is_`, `(`, [[expression]], `,`, [[type]], `)` <br />
| `is_`, [[basic type|type]], `(`, [[expression]], `)` <br />
| `is_`, [[name|expression]], `(`, [[expression]], `)` <br />
| `pre_`, `(`, [[expression]], { `,`, [[expression]] }, `)` <br />
| `isofclass`, `(`, [[name|expression]], [[expression]], `)` <br />
| [[tuple expression|expression]] <br />
| [[record expression|expression]] <br />
| [[set expression|expression]] <br />
| [[sequence expression|expression]] <br />
| [[subsequence|expression]] <br />
| [[map expression|expression]] <br />
| [[if expression|expression]] <br />
| [[cases expression|expression]] <br />
| [[apply|expression]] <br />
| [[field select|expression]] <br />
| [[tuple select|expression]] <br />
;

[[name|expression]] → <br />
  [[identifier|lexical]], [ `.`, [[identifier|lexical]] ] <br />
;

[[old name|expression]] → <br />
  [[identifier|lexical]], `~` <br />
;

[[unary operator|expression]] → `+` | `-` | `abs` | `floor` | `not` | `card` | `power` | `dunion` | `dinter` | `hd` | `tl` | `len` | `elems` | `inds` | `reverse` | `conc` | `dom` | `rng` | `merge` | `inverse` <br />
;

[[binary operator|expression]] →
  `+` | `-` | `*` | `/` | `div` | `rem` | `mod` | `<` | `<=` | `>` | `>=` | `=` | `<>` | `or` | `and` | `=>` | `<=>` | `in` `set` | `not` `in` `set` | `subset` | `psubset` | `union` | `\` | `inter` | `^` | `++` | `munion` | `<:` | `<-:` | `:>` | `:->` | `comp` | `**` <br />
;

[[tuple expression|expression]] → <br />
  `mk_`, `(`, [[expression]], `,`, [[expression]], { `,`, [[expression]] }, `)` <br />
;

[[record expression|expression]] → <br />
  `mk_`, `token`, `(`, [[expression]], `)` <br />
| `mk_`, [[name|expression]], `(`, [ [[expression]], { `,`, [[expression]]  } ], `)` <br />
;

[[set expression|expression]] → <br />
  `{`, [ [[expression]], { `,`, [[expression]]  } ], `}` <br />
| `{`, [[expression]], `|`, [[bind list|pattern]], [ `@`, [[expression]] ], `}` <br />
| `{`, [[expression]], `,`, `...`, `,`, [[expression]], `}` <br />
;

[[sequence expression|expression]] → <br />
  `[`, [ [[expression]], { `,`, [[expression]]  } ], `]` <br />
| `[`, [[expression]], `|`, [[set bind|pattern]], [ `@`, [[expression]] ], `]` <br />
;

[[subsequence|expression]] → <br />
  [[expression]], `(`, [[expression]], `,`, `...`, `,`, [[expression]], `)` <br />
;

[[map expression|expression]] → <br />
  `{`, `|->`, `}` <br />
| `{`, [[maplet|expression]], { `,`, [[maplet|expression]] }, `}` <br />
| `{`, [[maplet|expression]], `|`, [[bind list|pattern]], [ `@`, [[expression]] ], `}` <br />
;

[[maplet|expression]] → <br />
  [[expression]], `|->`, [[expression]] <br />
;

[[apply|expression]] → <br />
  [[expression]], `(`, [ [[expression]], { `,`, [[expression]]  } ], `)` <br />
;

[[field select|expression]] → <br />
  [[expression]], `.`, [[identifier|lexical]] <br />
;

[[tuple select|expression]] → <br />
  [[expression]], `.\#`, [[numeral|lexical]] <br />
;

[[if expression|expression]] → <br />
  `if`, [[expression]], `then`, [[expression]], { [[elseif expression|expression]] }, `else`, [[expression]] <br />
;

[[elseif expression|expression]] → <br />
  `elseif`, [[expression]], `then`, [[expression]] <br />
;

[[cases expression|expression]] → <br />
  `cases`, [[expression]], `:`, [[cases expression alternatives|expression]], [ `,`, `others` `->` [[expression]]  ], `end` <br />
;

[[cases expression alternatives|expression]] → <br />
  [[pattern list|pattern]], `->`, [[expression]], { `,`, [[pattern list|pattern]], `->`, [[expression]] } <br />
;

[[assignable expression|expression]] → <br />
  `self` { [[selector|expression]] } <br />
| [[identifier|lexical]] { [[selector|expression]] } <br />
;

[[selector|expression]] → <br />
  `(`, [ [[expression]], { `,`, [[expression]]  } ], `)` <br />
| `(`, [[expression]], `...`, [[expression]], `)` <br />
| `.#`, [[numeral|lexical]] <br />
| `.`, [[identifier|lexical]] <br />
;