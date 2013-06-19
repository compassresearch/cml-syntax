[[value declarations|declaration]] →
  `values`, { [[value definition|declaration]] } <br />
;

[[value definition|declaration]] → 
  [ [[qualifier|declaration]] ], [[bindable pattern|pattern]], [ `:`, [[type]] ], `=`, [[expression]] <br />
;

[[qualifier|declaration]] →
  `private` | `protected` | `public` | `logical` <br />
;

[[channel declarations|declaration]] →
  `channels`, { [[channel name declaration|declaration]] } <br />
;

[[channel name declaration|declaration]] →
  [[identifier|lexical]], { `,`, [[identifier|lexical]] }, [ `:`, [[type]] ] <br />
;

[[chanset declarations|declaration]] →
  `chansets`, { [[chanset definition|declaration]] } <br />
;

[[chanset definition|declaration]] →
  [[identifier|lexical]], `=`, [[chanset expression|varset]] <br />
;

[[class declaration|declaration]] →
  `class`, [[identifier|lexical]], [ `extends`, [[identifier|lexical]] ], `=`, `begin`, { [[class paragraph|declaration]] }, `end` <br />
;

[[class paragraph|declaration]] → <br />
  [[type declarations|declaration]] <br />
| [[value declarations|declaration]] <br />
| [[function declarations|function]] <br />
| [[operation declarations|declaration]] <br />
| [[state declarations|declaration]] <br />
| `initial`, [[operation definition|operation]] <br />
;

[[nameset declarations|declaration]] →
  `namesets`, { [[nameset definition|declaration]] } <br />
;

[[nameset definition|declaration]] →
  [[identifier|lexical]], `=`, [[nameset expression|varset]] <br />
;

[[state declarations|declaration]] →
  `state`, { [[instance variable definition|declaration]] } <br />
;

[[instance variable definition|declaration]] → <br />
  [ [[qualifier|declaration]] ], [[assignment definition|declaration]] <br />
| [[invariant definition|declaration]] <br />
;

[[assignment definition|declaration]] →
  [[identifier|lexical]], `:`, [[type]], [ [[assignment defintion value|declaration]]  ] <br />
;

[[assignment definition value|declaration]] → <br />
  `:=`, [[expression]] <br />
| `in`, [[expression]] <br />
;

[[invariant definition|declaration]] →
  `inv`, [[expression]] <br />
;

[[process declaration|declaration]] →
  `process`, [[identifier|lexical]], `=`, [ [[parametrisation|declaration]], `@` ], [[process]] <br />
;

Note: the only parametrisation qualifier allowed in a process
declaration is `val`.  (Omitting a parametrisation qualifier defaults
to `val`, and is permitted as well.)

[[parametrisation|declaration]] →
  [ [[parametrisation qualifier|declaration]] ], [[identifier|lexical]], { `,`, [[identifier|lexical]] }, `:`, [[type]] <br />
;

[[parametrisation qualifier|declaration]] → `val` | `res` | `vres` <br />
;

[[action declarations|declaration]] →
  `actions`, { [[action definition|declaration]] } <br />
;

[[action definition|declaration]] →
  [[identifier|lexical]], `=`, [  [[parametrisation|declaration]], `@`  ], [[action]] <br />
;