[[type declarations|type]] → <br />
  `types`, [ [[type definition]], { `;`, [[type definition]] } ]
;

[[type definition|type]] → <br />
  [ [[qualifier]] ], [[identifier]], `=`, [[type]], [ [[type invariant|type]] ] <br />
| [ [[qualifier]] ], [[identifier]], `::`, { [[field]] }, [ [[type invariant|type]] ]
}

[[type]] → <br />
  `(`, [[type]], `)` <br />
| [[basic type]] <br />
| [[quote literal]] <br />
| `compose`, [[identifier]], `of`, { [[field|type]] }, `end` <br />
| [[type]], `|`, [[type]], { `|`, [[type]] } <br />
| [[type]], `*`, [[type]], { `*`, [[type]] } <br />
| `[`, [[type]], `]` <br />
| `set` `of`, [[type]] <br />
| `seq` `of`, [[type]] <br />
| `seq1` `of`, [[type]] <br />
| `map`, [[type]], `to`, [[type]] <br />
| `inmap`, [[type]], `to`, [[type]] <br />
| [[function type|type]] <br />
| [[name]] 
}

[[basic type|type]] →
  `bool` 
| `nat` 
| `nat1` 
| `int` 
| `rat` 
| `real` 
| `char` 
| `token`
;

[[field|type]] → <br />
  [[type]] <br />
| [[identifier]], `:`, [[type]] <br />
| [[identifier]], `:-`, [[type]]
}

[[function type|type]] → <br />
  [[discretionary type|type]], `+>`, [[type]] <br />
| [[discretionary type|type]], `->`, [[type]]
}

[[discretionary type|type]] → <br />
  [[type]] <br />
| `()`
}

[[type invariant|type]] → <br />
  `inv`, [[pattern]], `==`, [[expression]]
}


