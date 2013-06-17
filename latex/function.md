[[function declarations|function]] → <br />
  `functions`, { [[function definition]] } <br />
;

[[function definition|function]] → <br />
  [[explicit function definition|function]] <br />
| [[implicit function definition|function]] <br />
;

[[explicit function definition|function]] → <br />
  [ [[qualifier]] ], [[identifier]], `:`, [[function type]], [[identifier]], [[parameters list]], `==`, [[function body]], [ `pre`, [[expression]] ], [ `post`, [[expression]] ], [ `measure`, [[name]] ] <br />
;

[[parameters list|function]] → <br />
  [[parameters]], { [[parameters]] } <br />
;

[[parameters|function]] → <br />
  `(`, [ [[pattern list]] ], `)` <br />
;

[[implicit function definition|function]] → <br />
  [ [[qualifier]] ], [[identifier]], [[parameter types]], [[identifier type pair list]], [ `pre`, [[expression]] ], `post`, [[expression]] <br />
;

[[parameter types|function]] → <br />
 `(`, [ [[pattern list]], `:`, [[type]], { `,`, [[pattern list]], `:`, [[type]] } ], `)`
}

[[identifier type pair list|function]] → <br />
  [[identifier]], `:`, [[type]], { `,`, [[identifier]], `:`, [[type]] }
;

[[function body]] → <br />
  [[expression]] <br />
| `is not yet specified` <br />
| `is subclass responsibility` <br />
;

