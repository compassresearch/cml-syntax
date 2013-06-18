
[[expression]] → <br />
  `self` <br />
| [[name]] <br />
| [[old name]]  <br />
| [[symbolic literal]] <br />
| `(`, [[expression]], `)` <br />
| [[unary operator]], [[expression]] <br />
| [[expression]], [[binary operator]], [[expression]] <br />
| `let`, [[local definition]], { `,`, [[local definition]] }, `in`, [[expression]] <br />
| `forall`, [[bind list]], `@`, [[expression]] <br />
| `exists`, [[bind list]], `@`, [[expression]] <br />
| `exists1`, [[bind]], `@`, [[expression]] <br />
| `iota`, [[bind]], `@`, [[expression]] <br />
| `lambda`, [[type bind list]], `@`, [[expression]] <br />
| `is_`, `(`, [[expression]], `,`, [[type]], `)` <br />
| `is_`, [[basic type]], `(`, [[expression]], `)` <br />
| `is_`, [[name]], `(`, [[expression]], `)` <br />
| `pre_`, `(`, [[expression]], { `,`, [[expression]] }, `)` <br />
| `isofclass`, `(`, [[name]], [[expression]], `)` <br />
| [[tuple expression]] <br />
| [[record expression]] <br />
| [[set expression]] <br />
| [[sequence expression]] <br />
| [[subsequence]] <br />
| [[map expression]] <br />
| [[if expression]] <br />
| [[cases expression]] <br />
| [[apply]] <br />
| [[field select]] <br />
| [[tuple select]] <br />
;

[[name|expression]] → <br />
  [[identifier]], [ `.`, [[identifier]] ] <br />
;

[[old name|expression]] → <br />
  [[identifier]], `~` <br />
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
| `mk_`, [[name]], `(`, [ [[expression]], { `,`, [[expression]]  } ], `)` <br />
;

[[set expression|expression]] → <br />
  `{`, [ [[expression]], { `,`, [[expression]]  } ], `}` <br />
| `{`, [[expression]], `|`, [[bind list]], [ `@`, [[expression]] ], `}` <br />
| `{`, [[expression]], `,`, `...`, `,`, [[expression]], `}` <br />
;

[[sequence expression|expression]] → <br />
  `[`, [ [[expression]], { `,`, [[expression]]  } ], `]` <br />
| `[`, [[expression]], `|`, [[set bind]], [ `@`, [[expression]] ], `]` <br />
;

[[subsequence|expression]] → <br />
  [[expression]], `(`, [[expression]], `,`, `...`, `,`, [[expression]], `)` <br />
;

[[map expression|expression]] → <br />
  `{`, `|->`, `}` <br />
| `{`, [[maplet]], { `,`, [[maplet]] }, `}` <br />
| `{`, [[maplet]], `|`, [[bind list]], [ `@`, [[expression]] ], `}` <br />
;

[[maplet|expression]] → <br />
  [[expression]], `|->`, [[expression]] <br />
;

[[apply|expression]] → <br />
  [[expression]], `(`, [ [[expression]], { `,`, [[expression]]  } ], `)` <br />
;

[[field select|expression]] → <br />
  [[expression]], `.`, [[identifier]] <br />
;

[[tuple select|expression]] → <br />
  [[expression]], `.\#`, [[numeral]] <br />
;

[[if expression|expression]] → <br />
  `if`, [[expression]], `then`, [[expression]], { [[elseif expression]] }, `else`, [[expression]] <br />
;

[[elseif expression|expression]] → <br />
  `elseif`, [[expression]], `then`, [[expression]] <br />
;

[[cases expression|expression]] → <br />
  `cases`, [[expression]], `:`, [[cases expression alternatives]], [ `,`, `others` `->` [[expression]]  ], `end` <br />
;

[[cases expression alternatives|expression]] → <br />
  [[pattern list]], `->`, [[expression]], { `,`, [[pattern list]], `->`, [[expression]] } <br />
;

[[assignable expression|expression]] → <br />
  `self` { [[selector]] } <br />
| [[identifier]] { [[selector]] } <br />
;

[[selector|expression]] → <br />
  `(`, [ [[expression]], { `,`, [[expression]]  } ], `)` <br />
| `(`, [[expression]], `...`, [[expression]], `)` <br />
| `.#`, [[numeral]] <br />
| `.`, [[identifier]] <br />
;
