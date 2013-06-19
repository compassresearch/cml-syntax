[[chanset expression|varset]] → <br />
  [[identifier|lexical]] <br />
| `{`,  [ [[identifier|lexical]], { `,`, [[identifier|lexical]] } ], `}` <br />
| `{|`, [ [[identifier|lexical]], { `,`, [[identifier|lexical]] } ], `|}` <br />
| `{|`, [[identifier|lexical]], { `.`, [[expression]] }, `|` [[bind list|pattern]], [ `@`, [[expression]] ], `|}` <br />
| [[chanset expression|varset]], `union`, [[chanset expression|varset]] <br />
| [[chanset expression|varset]], `inter`, [[chanset expression|varset]] <br />
| [[chanset expression|varset]], `\`, [[chanset expression|varset]] <br />
;

[[nameset expression|varset]] → [[chanset expression|varset]] <br />
;
