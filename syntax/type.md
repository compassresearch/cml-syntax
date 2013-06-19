[[type declarations|type]] → <br />
  `types`, [ [[type definition|type]], { `;`, [[type definition|type]] } ]
;

[[type definition|type]] → <br />
  [ [[qualifier|declaration]] ], [[identifier|lexical]], `=`, [[type]], [ [[type invariant|type]] ] <br />
| [ [[qualifier|declaration]] ], [[identifier|lexical]], `::`, { [[field|type]] }, [ [[type invariant|type]] ]
}

[[type]] → <br />
  `(`, [[type]], `)` <br />
| [[basic type|type]] <br />
| [[quote literal|lexical]] <br />
| `compose`, [[identifier|lexical]], `of`, { [[field|type]] }, `end` <br />
| [[type]], `|`, [[type]], { `|`, [[type]] } <br />
| [[type]], `*`, [[type]], { `*`, [[type]] } <br />
| `[`, [[type]], `]` <br />
| `set` `of`, [[type]] <br />
| `seq` `of`, [[type]] <br />
| `seq1` `of`, [[type]] <br />
| `map`, [[type]], `to`, [[type]] <br />
| `inmap`, [[type]], `to`, [[type]] <br />
| [[function type|type]] <br />
| [[name|expression]] <br />
;

[[basic type|type]] →
  `bool` 
| `nat` 
| `nat1` 
| `int` 
| `rat` 
| `real` 
| `char` 
| `token` <br />
;

[[field|type]] → <br />
  [[type]] <br />
| [[identifier|lexical]], `:`, [[type]] <br />
| [[identifier|lexical]], `:-`, [[type]]
;

[[function type|type]] → <br />
  [[discretionary type|type]], `+>`, [[type]] <br />
| [[discretionary type|type]], `->`, [[type]]
;

[[discretionary type|type]] → <br />
  [[type]] <br />
| `()`
;

[[type invariant|type]] → <br />
  `inv`, [[pattern]], `==`, [[expression]]
;

