[[function declarations|function]] → <br />
  `functions`, { [[function definition|function]] } <br />
;

[[function definition|function]] → <br />
  [[explicit function definition|function]] <br />
| [[implicit function definition|function]] <br />
;

[[explicit function definition|function]] → <br />
  [ [[qualifier|declaration]] ], [[identifier|lexical]], `:`, [[function type|type]], [[identifier|lexical]], [[parameters list|function]], `==`, [[function body|function]], [ `pre`, [[expression]] ], [ `post`, [[expression]] ], [ `measure`, [[name|expression]] ] <br />
;

[[parameters list|function]] → <br />
  [[parameters|function]], { [[parameters|function]] } <br />
;

[[parameters|function]] → <br />
  `(`, [ [[pattern list|pattern]] ], `)` <br />
;

[[implicit function definition|function]] → <br />
  [ [[qualifier|declaration]] ], [[identifier|lexical]], [[parameter types|function]], [[identifier type pair list|function]], [ `pre`, [[expression]] ], `post`, [[expression]] <br />
;

[[parameter types|function]] → <br />
 `(`, [ [[pattern list|pattern]], `:`, [[type]], { `,`, [[pattern list|pattern]], `:`, [[type]] } ], `)` <br />
}

[[identifier type pair list|function]] → <br />
  [[identifier|lexical]], `:`, [[type]], { `,`, [[identifier|lexical]], `:`, [[type]] } <br />
;

[[function body|function]] → <br />
  [[expression]] <br />
| `is not yet specified` <br />
| `is subclass responsibility` <br />
;
