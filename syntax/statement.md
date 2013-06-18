
[[statement]] → <br />
  `let`, [[local definition]], { `,`, [[local definition]] },  `in`, [[action]] <br />
| `(`, [ `dcl`, [[assignment definition]], { `,`, [[assignment definition]] }, `@` ],  [[action]], `)` <br />
| [[cases statement|statement]] <br />
| [[if statement|statement]] <br />
| `if` [[non-deterministic alt]], { `|`, [[non-deterministic alt]] }, `end` <br />
| `do` [[non-deterministic alt]], { `|`, [[non-deterministic alt]] }, `end` <br />
| `while`, [[expression]], `do`, [[action]] <br />
| `for`, [[bindable pattern]], [ `:`, [[type]] ] `in`, [[expression]], `do`, [[action]] <br />
| `for`, `all`, [[bindable pattern]], `in set`, [[expression]], `do`, [[action]] <br />
| `for`, [[identifier]], `=`, [[expression]], `to`, [[expression]], [ `by`, [[expression]] ], `do`, [[action]] <br />
| `[`, [ [[frame]] ], [ `pre`, [[expression]] ], `post`, [[expression]], `]` <br />
| `return`, [ [[expression]] ] <br />
| [[assign statement|statement]] <br />
| [[multiple assign statement|statement]] <br />
| [[call statement|statement]] <br />
| [[new statement|statement]] <br />
;

[[local definition|statement]] → <br />
  [[value definition]] <br />
| [[function definition]] <br />
;

[[non-deterministic alt|statement]] → <br />
  [[expression]], `->`, [[action]] <br />
;

[[if statement|statement]] → <br />
  `if`, [[expression]], `then`, [[action]], { [[elseif statement|statement]] }, [ `else`, [[action]] ] <br />
;

[[elseif statement|statement]] → <br />
  `elseif`, [[expression]], `then`, [[action]] <br />
;

[[cases statement|statement]] → <br />
  `cases`, [[expression]], `:`, [[cases statement alt|statement]], { `,`, [[cases statement alt|statement]] }, [ `,`, [[others statement|statement]] ], `end` <br />
;

[[cases statement alt|statement]] → <br />
  [[pattern list]], `->`, [[action]] <br />
;

[[others statement|statement]] → <br />
  `others`, `->`, [[action]] <br />
;

[[assign statement|statement]] → <br />
  [[assignable expression]], `:=`, [[expression]] <br />
;

[[multiple assign statement|statement]] → <br />
  `atomic`, `(`, [[assign statement|statement]], `;`, [[assign statement|statement]], { `;`, [[assign statement|statement]] }, `)` <br />
;

[[call statement|statement]] → <br />
  [[name]], `(`, [ [[expression]], { `,`, [[expression]]  } ], `)` <br />
| [[assignable expression]], `:=`, [[name]], `(`, [ [[expression]], { `,`, [[expression]]  } ], `)` <br />
;

[[new statement|statement]] → <br />
  [[assignable expression]], `:=`, `new`, [[name]], `(`, [ [[expression]], { `,`, [[expression]]  } ], `)` <br />
;

