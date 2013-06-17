
[[action]] → <br />
  `Skip` <br/>
| `Stop` <br/>
| `Chaos` <br/>
| `Div` <br/>
| `Wait` [[expression]] <br/>
| [[communication]], `->`, [[action]]   <br/>
| `[`, [[expression]], `]`, `&`, [[action]]   <br/>
| [[action]], `;`, [[action]]   <br/>
| [[action]], `[]`, [[action]]   <br/>
| [[action]], `|~|`, [[action]]   <br/>
| [[action]], `/_\`, [[action]]   <br/>
| [[action]], `/_`, [[expression]], `_\`, [[action]]   <br/>
| [[action]], `[_>`, [[action]]   <br/>
| [[action]], `[_`, [[expression]], `_>`, [[action]]   <br/>
| [[action]], `\\`, [[chanset expression]]   <br/>
| [[action]], `startby`, [[expression]]  <br/>
| [[action]], `endby`, [[expression]]  <br/>
| [[action]], [[renaming expression]]   <br/>
| `mu`, [[identifier]], { `,` [[identifier]] }, `@`, `(`, [[action]], { `,` [[action]] }, `)`  <br/>
| [[parallel action]]  <br/>
| [[parametrised action]]  <br/>
| `(`, [[action]], `)`  <br/>
| [[instantiated action]]  <br/>
| [[replicated action]]  <br/>
| [[statement]]  <br/>
;

[[communication|action]] → <br />
  [[identifier]], { [[communication parameter|action]] } <br />
;

[[communication parameter|action]] → <br />
  `?`, [[bindable pattern]], [ `in set`, [[expression]] ] <br />
| `!`, [[parameter]] <br />
| `.`, [[parameter]] <br />
;

[[parameter|action]] → <br />
  [[identifier]] <br />
| `(` [[expression]] `)` <br />
| [[symbolic literal]] <br />
| [[tuple expression]] <br />
| [[record expression]] <br />
;

[[parallel action|action]] → <br />
| [[action]], `||` [[action]], <br />
| [[action]], `[|`, [[nameset expression]], `|`, [[nameset expression]], `|]`, [[action]] <br /> 
| [[action]], `|||`, [[action]] <br /> 
| [[action]], `[||`, [[chanset expression]], `|`,  [[chanset expression]], `||]`, [[action]] <br /> 
| [[action]], `[`, [[chanset expression]], `||`, [[chanset expression]], `]`, [[action]] <br />
| [[action]], `[`, [[nameset expression]], `|`, [[chanset expression]], `||`, [[chanset expression]], `|`, [[nameset expression]], `]`, [[action]] \\
| [[action]], `[|`, [[chanset expression]], `|]`, [[action]] <br />
| [[action]], `[|`, [[nameset expression]], `|`, [[chanset expression]], `|`, [[nameset expression]], `|]`, [[action]] <br /> 
;

[[parametrised action|action]] → <br />
  `(` [[parametrisation]], { `,`, [[parametrisation]] }, `@`, [[action]], `)` <br />
;

[[instantiated action|action]] → <br />
  [[parametrised action|action]], `(`, [[expression]], { `,`, [[expression]] }, `)` <br />
;

[[replicated action|action]] → <br />
  `;`, [[replication declarations]], `@`, [[action]] <br /> 
| `[]`, [[replication declarations]], `@`, [[action]] <br /> 
| `|~|`, [[replication declarations]], `@`, [[action]] <br />  
| `[||`, [[nameset expression]], `||]`, [[replication declarations]], `@`, [[action]] <br /> 
| `|||`, [[replication declarations]], `@`, `[`, [[nameset expression]], `]`, [[action]] <br /> 
| `[|`, [[chanset expression]] `|]`, [[replication declarations]], `@`, `[` , [[nameset expression]], `]`, [[action]] <br /> 
| `||`, [[replication declarations]], `@`, `[`, [[nameset expression]], `|`, [[chanset expression]], `]`, [[action]] <br /> 
| `||`, [[replication declarations]], `@`, `[`, [[nameset expression]], `]`, [[action]] <br /> 
;
