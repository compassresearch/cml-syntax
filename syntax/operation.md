Operations do not include reactive constructs; while the parser will
accept any action in an operation body, the typechecker will only
allow statements, the `;` sequential composition operator, and
the constant action `Skip`.  In essence, operation bodies in
CML allow only what is allowed in VDM operation bodies.

[[operation declarations|operation]] → <br />
  `operations`, { [[operation definition|operation]] } <br />
;

[[operation definition|operation]] → <br />
  [[explicit operation definition|operation]] <br />
| [[implicit operation definition|operation]] <br />
;

[[explicit operation definition|operation]] → <br />
  [ [[qualifier]] ], [[identifier]], `:`, [[operation type|type]], [[identifier]], [[parameters]], `==`, [[operation body|operation]], [ `pre`, [[expression]] ], [ `post`, [[expression]] ] <br />
;

[[operation type|operation]] → <br />
  [[discretionary type|type]], `==>`, [[discretionary type|type]] <br />
;

[[operation body|operation]] → <br />
  [[action]] <br />
| `is subclass responsibility` <br />
| `is not yet specified` <br />
;

[[implicit operation definition|operation]] → <br />
  [ [[qualifier]] ], [[identifier]], [[parameter types]], [ [[identifier type pair list]] ], [ [[frame]] ], [ `pre`, [[expression]] ], `post`, [[expression]] <br />
;

[[frame|operation]] → <br />
  `frame`, [[var information]], { [[var information]] }
;

[[var information|operation]] → <br />
  `rd`, [[name]], { `,`, [[name]] }, [ `:`, [[type]] ] <br />
| `wr`, [[name]], { `,`, [[name]] }, [ `:`, [[type]] ] <br />
;


