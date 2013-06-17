[[chanset expression|varset]] → <br />
  [[identifier]] \\
| `{`,  [ [[identifier]], { `,`, [[identifier]] } ], `}` \\
| `{|`, [ [[identifier]], { `,`, [[identifier]] } ], `|}` \\
| `{|`, [[identifier]], { `.`, [[expression]] }, `|` [[bind list]], [ `@`, [[expression]] ], `|}` \\
| [[chanset expression|varset]], `union`, [[chanset expression|varset]] \\
| [[chanset expression|varset]], `inter`, [[chanset expression|varset]] \\
| [[chanset expression|varset]], `\`, [[chanset expression|varset]] \\
;

[[nameset expression|varset]] → [[chanset expression|varset]] <br />
;

