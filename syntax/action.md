[[action]] → <br />
  `Skip` <br/>
| `Stop` <br/>
| `Chaos` <br/>
| `Div` <br/>
| `Wait` [[expression]] <br/>
| [[communication|action]], `->`, [[action]]   <br/>
| `[`, [[expression]], `]`, `&`, [[action]]   <br/>
| [[action]], `;`, [[action]]   <br/>
| [[action]], `[]`, [[action]]   <br/>
| [[action]], `|~|`, [[action]]   <br/>
| [[action]], `/_\`, [[action]]   <br/>
| [[action]], `/_`, [[expression]], `_\`, [[action]]   <br/>
| [[action]], `[_>`, [[action]]   <br/>
| [[action]], `[_`, [[expression]], `_>`, [[action]]   <br/>
| [[action]], `\\`, [[chanset expression|varset]]   <br/>
| [[action]], `startby`, [[expression]]  <br/>
| [[action]], `endby`, [[expression]]  <br/>
| [[action]], [[renaming expression|process]]   <br/>
| `mu`, [[identifier|lexical]], { `,` [[identifier|lexical]] }, `@`, `(`, [[action]], { `,` [[action]] }, `)`  <br/>
| [[parallel action|action]]  <br/>
| [[parametrised action|action]]  <br/>
| `(`, [[action]], `)`  <br/>
| [[instantiated action|action]]  <br/>
| [[replicated action|action]]  <br/>
| [[statement]]  <br/>
;

[[communication|action]] → <br />
  [[identifier|lexical]], { [[communication parameter|action]] } <br />
;

[[communication parameter|action]] → <br />
  `?`, [[bindable pattern|pattern]], [ `:`, `(`, [[expression]], `)` ] <br />
| `!`, [[parameter|action]] <br />
| `.`, [[parameter|action]] <br />
;

[[parameter|action]] → <br />
  [[identifier|lexical]] <br />
| `(` [[expression]] `)` <br />
| [[symbolic literal|lexical]] <br />
| [[tuple expression|expression]] <br />
| [[record expression|expression]] <br />
;

[[parallel action|action]] → <br />
| [[action]], `||` [[action]], <br />
| [[action]], `[|`, [[nameset expression|varset]], `|`, [[nameset expression|varset]], `|]`, [[action]] <br />
| [[action]], `|||`, [[action]] <br />
| [[action]], `[||`, [[chanset expression|varset]], `|`,  [[chanset expression|varset]], `||]`, [[action]] <br />
| [[action]], `[`, [[chanset expression|varset]], `||`, [[chanset expression|varset]], `]`, [[action]] <br />
| [[action]], `[`, [[nameset expression|varset]], `|`, [[chanset expression|varset]], `||`, [[chanset expression|varset]], `|`, [[nameset expression|varset]], `]`, [[action]] \\
| [[action]], `[|`, [[chanset expression|varset]], `|]`, [[action]] <br />
| [[action]], `[|`, [[nameset expression|varset]], `|`, [[chanset expression|varset]], `|`, [[nameset expression|varset]], `|]`, [[action]] <br />
;

[[parametrised action|action]] → <br />
  `(` [[parametrisation|declaration]], { `,`, [[parametrisation|declaration]] }, `@`, [[action]], `)` <br />
;

[[instantiated action|action]] → <br />
  [[parametrised action|action]], `(`, [[expression]], { `,`, [[expression]] }, `)` <br />
;

[[replicated action|action]] → <br />
  `;`, [[replication declarations|declaration]], `@`, [[action]] <br />
| `[]`, [[replication declarations|declaration]], `@`, [[action]] <br />
| `|~|`, [[replication declarations|declaration]], `@`, [[action]] <br />
| `[||`, [[nameset expression|varset]], `||]`, [[replication declarations|declaration]], `@`, [[action]] <br />
| `|||`, [[replication declarations|declaration]], `@`, `[`, [[nameset expression|varset]], `]`, [[action]] <br />
| `[|`, [[chanset expression|varset]] `|]`, [[replication declarations|declaration]], `@`, `[` , [[nameset expression|varset]], `]`, [[action]] <br />
| `||`, [[replication declarations|declaration]], `@`, `[`, [[nameset expression|varset]], `|`, [[chanset expression|varset]], `]`, [[action]] <br />
| `||`, [[replication declarations|declaration]], `@`, `[`, [[nameset expression|varset]], `]`, [[action]] <br />
;