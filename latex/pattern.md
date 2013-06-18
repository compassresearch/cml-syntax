[[pattern]] → <br />
  [[bindable pattern]] <br />
| [[match value]] <br />
;

[[bindable pattern|pattern]] → <br />
  `-` <br />
| [[identifier]] <br />
| `mk_`, `(`, [[pattern]], `,`, [[pattern list]], `)` <br />
| `mk_`, [[name]], `(`, [ [[pattern list]] ], `)` <br />
;

[[match value|pattern]] → <br />
  `(`, [[expression]], `)` <br />
| [[symbolic literal]] <br />
;

[[pattern list|pattern]] → <br />
  [[pattern]], { `,`, [[pattern]] } <br />
;

[[bind|pattern]] → [[set bind]] | [[type bind]] <br />
;

[[set bind|pattern]] → <br />
  [[pattern]], `in` `set`, [[expression]] <br />
;

[[type bind|pattern]] → <br />
  [[pattern]], `:`, [[type]] <br />
;

[[bind list|pattern]] → <br />
  [[multiple bind]], { `,`, [[multiple bind]] } <br />
;

[[multiple bind|pattern]] → <br />
  [[pattern list]], `in` `set`, [[expression]] <br />
| [[pattern list]], `:`, [[type]] <br />
;

[[type bind list|pattern]] → <br />
  [[type bind]], { `,`, [[type bind]] } <br />
;


