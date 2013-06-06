
[[action]] –>
  `Skip`
| `Stop`  
| `Chaos`  
| `Div`  
| `Wait` [[expression]]
% communication
| [[communication]], `->`, [[action]]  
% boolean guard
| `[`, [[expression]], `]`, `\&`, [[action]]  
% sequential composition
| [[action]], `;`, [[action]]  
% external choice
| [[action]], `[]`, [[action]]  
% internal choice
| [[action]], `|mytilde|`, [[action]]  
% interrupt
| [[action]], `/\mybackslash`, [[action]]  
| [[action]], `/(`, [[expression]], `)\mybackslash`, [[action]]  
% untimed timeout
| [[action]], `[>`, [[action]]  
% exception
| [[action]], `[(`, [[expression]], `)>`, [[action]]  
% hiding
| [[action]], `\mybackslash\mybackslash`, [[chanset expression]]  
| [[action]], `startby`, [[expression]] 
| [[action]], `endby`, [[expression]] 
% variable renaming --- confirm!!!!
%\Alt\ [[action]], `[`, [[identifier list]],
%      `:=`, [[identifier list]], `]`  
% channel renaming
| [[action]], [[renaming expression]]  
| `mu`, \CommaSepList{[[identifier]]}, `@`, `(`, \CommaSepList{[[action]]}, `)` 
% parallelism
| [[parallel action]] 
| [[parametrised action]] 
| `(`, [[action]], `)` 
| [[instantiated action]] 
| [[replicated action]] 
| [[statement]] 


