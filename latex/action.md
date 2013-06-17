
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

[[action|communication]] → <br />
  [[identifier]], { [[action|communication parameter]] } <br />
;

[[action|communication parameter]] → <br />
  `?`, [[bindable pattern]], [ `in set`, [[expression]] ] <br />
| `!`, [[parameter]] <br />
| `.`, [[parameter]] <br />
;
