[[value declarations|declaration]] → <br />
  `values`, { [[value definition|declaration]] } <br />
;

[[value definition|declaration]] → <br />
  [ [[qualifier|declaration]] ], [[bindable pattern|pattern]], [ `:`, [[type]] ], `=`, [[expression]] <br />
;

[[qualifier|declaration]] → `private` | `protected` | `public` | `logical` <br />
;

[[channel declarations|declaration]] → <br />
  `channels`, { [[channel name declaration|declaration]] } <br />
;

[[channel name declaration|declaration]] → <br />
  [[identifier|lexical]], { `,`, [[identifier|lexical]] }, [ `:`, [[type]] ] <br />
;

[[chanset declarations|declaration]] → <br />
  `chansets`, { [[chanset definition|varset]] } <br />
;

[[chanset definition|declaration]] → <br />
  [[identifier]], `=`, [[chanset expression]] <br />
;

[[class declaration|declaration]] → <br />
  `class`, [[identifier]], [ `extends`, [[identifier]] ], `=`, `begin`, { [[class paragraph]] }, `end` <br />
;

[[class paragraph|declaration]] → <br />
  [[type declarations]] <br />
| [[value declarations]] <br />
| [[function declarations]] <br />
| [[operation declarations]] <br />
| [[state declarations]] <br />
| `initial`, [[operation definition]] <br />
;

[[nameset declarations|declaration]] → <br />
  `namesets`, { [[nameset definition]] } <br />
;

[[nameset definition|declaration]] → <br />
  [[identifier]], `=`, [[nameset expression]] <br />
;

[[state declarations|declaration]] → <br />
  `state`, { [[instance variable definition]] } <br />
;

[[instance variable definition|declaration]] → <br />
  [ [[qualifier]] ], [[assignment definition]] <br />
| [[invariant definition]] <br />
;

[[assignment definition|declaration]] → <br />
  [[identifier]], `:`, [[type]], [ `:=`, [[expression]]  ] <br />
| [[identifier]], `:`, [[type]], [ `in`, [[expression]]  ] <br />
;

[[invariant definition|declaration]] → <br />
  `inv`, [[expression]] <br />
;

[[process declaration|declaration]] → <br />
  `process`, [[identifier]], `=`, [ [[parametrisation]], `@` ], [[process]] <br />
;

Note: the only parametrisation qualifier allowed in a process
declaration is `val`.  (Omitting a parametrisation qualifier defaults
to `val`, and is permitted as well.)

[[parametrisation|declaration]] → <br />
  [ [[parametrisation qualifier]] ], [[identifier]], { `,`, [[identifier]] }, `:`, [[type]]
;

[[parametrisation qualifier|declaration]] → `val` | `res` | `vres` <br />
;

[[action declarations|declaration]] → <br />
  `actions`, { [[action definition]] } <br />
;

[[action definition|declaration]] → <br />
  [[identifier]], `=`, [  [[parametrisation]], `@`  ], [[action]] <br />
;