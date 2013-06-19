[[pattern]] → <br />
  [[bindable pattern|pattern]] <br />
| [[match value|pattern]] <br />
;

[[bindable pattern|pattern]] → <br />
  `-` <br />
| [[identifier|lexical]] <br />
| `mk_`, `(`, [[pattern]], `,`, [[pattern list|pattern]], `)` <br />
| `mk_`, [[name|expression]], `(`, [ [[pattern list|pattern]] ], `)` <br />
;

[[match value|pattern]] → <br />
  `(`, [[expression]], `)` <br />
| [[symbolic literal|lexical]] <br />
;

[[pattern list|pattern]] → <br />
  [[pattern]], { `,`, [[pattern]] } <br />
;

[[bind|pattern]] → [[set bind|pattern]] | [[type bind|pattern]] <br />
;

[[set bind|pattern]] → <br />
  [[pattern]], `in` `set`, [[expression]] <br />
;

[[type bind|pattern]] → <br />
  [[pattern]], `:`, [[type]] <br />
;

[[bind list|pattern]] → <br />
  [[multiple bind|pattern]], { `,`, [[multiple bind|pattern]] } <br />
;

[[multiple bind|pattern]] → <br />
  [[pattern list|pattern]], `in` `set`, [[expression]] <br />
| [[pattern list|pattern]], `:`, [[type]] <br />
;

[[type bind list|pattern]] → <br />
  [[type bind|pattern]], { `,`, [[type bind|pattern]] } <br />
;

