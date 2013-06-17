Operations do not include reactive constructs; while the parser will
accept any action in an operation body, the typechecker will only
allow statements, the `;` sequential composition operator, and
the constant action `Skip`.  In essence, operation bodies in
CML allow only what is allowed in VDM operation bodies.

[[operation declarations]] → <br />
  `operations`, { [[operation definition]] } <br />
;

[[operation definition]] → <br />
  [[explicit operation definition]] <br />
| [[implicit operation definition]] <br />
;

[[explicit operation definition]] → <br />
  [ [[qualifier]] ], [[identifier]], `:`, [[operation type]], [[identifier]], [[parameters]], `==`, [[operation body]], [ `pre`, [[expression]] ], [ `post`, [[expression]] ] <br />
;

[[operation type]] → <br />
  [[discretionary type|type]], `==>`, [[discretionary type|type]] <br />
;

[[operation body]] → <br />
  [[action]] <br />
| `is subclass responsibility` <br />
| `is not yet specified` <br />
;

[[implicit operation definition]] → <br />
  [ [[qualifier]] ], [[identifier]], [[parameter types]], [ [[identifier type pair list]] ], [ [[frame]] ], [ `pre`, [[expression]] ], `post`, [[expression]] <br />
;

[[frame|operation]] → <br />
  `frame`, [[var information]], { [[var information]] }
;

[[var information|operation]] → <br />
  `rd`, [[name]], { `,`, [[name]] }, [ `:`, [[type]] ] <br />
| `wr`, [[name]], { `,`, [[name]] }, [ `:`, [[type]] ] <br />
;


