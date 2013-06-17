
[[process]] → <br />
  `begin`, { [[action paragraph]] }, `@`, [[action]], `end` <br />
| [[process]], `;`, [[process]] <br /> 
| [[process]], `[]`, [[process]] <br /> 
| [[process]], `|~|`, [[process]] <br /> 
| [[process]], `[|`, [[chanset expression]], `|]`, [[process]] <br /> 
| [[process]], `[`, [[chanset expression]], `||`, [[chanset expression]], `]`, [[process]] <br /> 
| [[process]], `||`, [[process]] <br /> 
| [[process]], `|||`, [[process]] <br /> 
| [[process]], `/_\`, [[process]] <br /> 
| [[process]], `/_`, [[expression]], `_\`, [[process]] <br /> 
| [[process]], `[_>`, [[process]] <br /> 
| [[process]], `[_`, [[expression]], `_>`, [[process]] <br /> 
| [[process]], `\\`, [[chanset expression]] <br /> 
| [[process]], `startsby`, [[expression]] <br /> 
| [[process]], `endsby`, [[expression]] <br /> 
| `(`, [[parametrisation]], `@`, [[process]], `)`, `(`, [[expression]], { `,`, [[expression]] }, `)` <br /> 
| [[identifier]], [ `(`, [ [[expression]], { `,`, [[expression]] } ], `)` ] <br /> 
| [[process]], [[renaming expression]] <br />
| [[replicated process|process]] <br />
| `(`, [[process]], `)` <br />
;

[[replicated process|process]] → <br />
  `;`, [[replication declarations]], `@`, [[process]] <br /> 
| `[]`, [[replication declarations]], `@`, [[process]] <br /> 
| `|~|`, [[replication declarations]], `@`, [[process]] <br /> 
| `[|`, [[chanset expression]], `|]`, [[replication declarations]], `@`, [[process]] <br /> 
| `||`, [[replication declarations]], `@`, `[`, [[chanset expression]], `]`, [[process]] <br />
| `||`, [[replication declarations]], `@`, [[process]] <br />
| `|||`, [[replication declarations]], `@`, [[process]] <br />
;

[[action paragraph|process]] → <br />
  [[type declarations]] <br />
| [[value declarations]] <br />
| [[function declarations]] <br />
| [[operation declarations]] <br />
| [[action declarations]] <br />
| [[nameset declarations]] <br />
| [[state declarations]] <br />
;

[[renaming expression|process]] → <br />
  '[[`[[`]], [[renaming pair|process]], { `,`, [[renaming pair]] }, `]]` <br />
| '[[`[[`]], [[renaming pair]], `|` [[bind list]], [ `@`, [[expression]] ], `]]` <br />
;
 
[[renaming pair|process]] → <br />
  [[identifier]], [ `.`, [[expression]] ], `<-`, [[identifier]], [ `.`, [[expression]] ] <br />
;

[[replication declarations|process]] → <br />
  [[replication declaration]], { `,`, [[replication declaration]] } <br />
;

[[replication declaration|process]] → <br />
  [[identifier]], { `,`, [[identifier]] }, `:`, [[type]] <br />
| [[identifier]], { `,`, [[identifier]] }, `in` `set`, [[expression]] <br />
;
