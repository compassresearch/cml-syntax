[[process]] → <br />
  `begin`, { [[action paragraph|process]] }, `@`, [[action]], `end` <br />
| [[process]], `;`, [[process]] <br /> 
| [[process]], `[]`, [[process]] <br /> 
| [[process]], `|~|`, [[process]] <br /> 
| [[process]], `[|`, [[chanset expression|varset]], `|]`, [[process]] <br /> 
| [[process]], `[`, [[chanset expression|varset]], `||`, [[chanset expression|varset]], `]`, [[process]] <br /> 
| [[process]], `||`, [[process]] <br /> 
| [[process]], `|||`, [[process]] <br /> 
| [[process]], `/_\`, [[process]] <br /> 
| [[process]], `/_`, [[expression]], `_\`, [[process]] <br /> 
| [[process]], `[_>`, [[process]] <br /> 
| [[process]], `[_`, [[expression]], `_>`, [[process]] <br /> 
| [[process]], `\\`, [[chanset expression|varset]] <br /> 
| [[process]], `startsby`, [[expression]] <br /> 
| [[process]], `endsby`, [[expression]] <br /> 
| `(`, [[parametrisation|declaration]], `@`, [[process]], `)`, `(`, [[expression]], { `,`, [[expression]] }, `)` <br /> 
| [[identifier|lexical]], [ `(`, [ [[expression]], { `,`, [[expression]] } ], `)` ] <br /> 
| [[process]], [[renaming expression|process]] <br />
| [[replicated process|process]] <br />
| `(`, [[process]], `)` <br />
;

[[replicated process|process]] → <br />
  `;`, [[replication declarations|process]], `@`, [[process]] <br /> 
| `[]`, [[replication declarations|process]], `@`, [[process]] <br /> 
| `|~|`, [[replication declarations|process]], `@`, [[process]] <br /> 
| `[|`, [[chanset expression|varset]], `|]`, [[replication declarations|process]], `@`, [[process]] <br /> 
| `||`, [[replication declarations|process]], `@`, `[`, [[chanset expression|varset]], `]`, [[process]] <br />
| `||`, [[replication declarations|process]], `@`, [[process]] <br />
| `|||`, [[replication declarations|process]], `@`, [[process]] <br />
;

[[action paragraph|process]] → <br />
  [[type declarations|declaration]] <br />
| [[value declarations|declaration]] <br />
| [[function declarations|declaration]] <br />
| [[operation declarations|declaration]] <br />
| [[action declarations|declaration]] <br />
| [[nameset declarations|declaration]] <br />
| [[state declarations|declaration]] <br />
;

[[renaming expression|process]] → <br />
  '[[`[[`]], [[renaming pair|process]], { `,`, [[renaming pair|process]] }, `]]` <br />
| '[[`[[`]], [[renaming pair|process]], `|` [[bind list|pattern]], [ `@`, [[expression]] ], `]]` <br />
;
 
[[renaming pair|process]] → <br />
  [[identifier|lexical]], { `.`, [[expression]] }, `<-`, [[identifier|lexical]], { `.`, [[expression]] } <br />
;

[[replication declarations|process]] → <br />
  [[replication declaration|process]], { `,`, [[replication declaration|process]] } <br />
;

[[replication declaration|process]] → <br />
  [[identifier|lexical]], { `,`, [[identifier|lexical]] }, `:`, [[type]] <br />
| [[identifier|lexical]], { `,`, [[identifier|lexical]] }, `in` `set`, [[expression]] <br />
;