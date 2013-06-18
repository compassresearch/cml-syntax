[[chanset expression|varset]] → <br />
  [[identifier]] <br />
| `{`,  [ [[identifier]], { `,`, [[identifier]] } ], `}` <br />
| `{|`, [ [[identifier]], { `,`, [[identifier]] } ], `|}` <br />
| `{|`, [[identifier]], { `.`, [[expression]] }, `|` [[bind list]], [ `@`, [[expression]] ], `|}` <br />
| [[chanset expression|varset]], `union`, [[chanset expression|varset]] <br />
| [[chanset expression|varset]], `inter`, [[chanset expression|varset]] <br />
| [[chanset expression|varset]], `\`, [[chanset expression|varset]] <br />
;

[[nameset expression|varset]] → [[chanset expression|varset]] <br />
;

