 



Some <GlossaryTerm  term={"operator"}><i>operators</i></GlossaryTerm> make use of an <GlossaryTerm  term={"object"}><i>object</i></GlossaryTerm>, called an <GlossaryTerm styled={true} term={"environment object"}><i>environment object</i></GlossaryTerm>, that represents the set of <GlossaryTerm styled={true} term={"lexical binding"}><i>lexical bindings</i></GlossaryTerm> needed to perform semantic analysis on a <GlossaryTerm  term={"form"}><i>form</i></GlossaryTerm> in a given <GlossaryTerm styled={true} term={"lexical environment"}><i>lexical environment</i></GlossaryTerm>. The set of <GlossaryTerm  term={"binding"}><i>bindings</i></GlossaryTerm> in an <GlossaryTerm styled={true} term={"environment object"}><i>environment object</i></GlossaryTerm> may be a subset of the <GlossaryTerm  term={"binding"}><i>bindings</i></GlossaryTerm> that would be needed to actually perform an <GlossaryTerm  term={"evaluation"}><i>evaluation</i></GlossaryTerm>; for example, <GlossaryTerm  term={"value"}><i>values</i></GlossaryTerm> associated with *variable names* and <GlossaryTerm styled={true} term={"function name"}><i>function names</i></GlossaryTerm> in the corresponding <GlossaryTerm styled={true} term={"lexical environment"}><i>lexical environment</i></GlossaryTerm> might not be available in an <GlossaryTerm styled={true} term={"environment object"}><i>environment object</i></GlossaryTerm>. 



The <GlossaryTerm  term={"type"}><i>type</i></GlossaryTerm> and nature of an <GlossaryTerm styled={true} term={"environment object"}><i>environment object</i></GlossaryTerm> is <GlossaryTerm  term={"implementation-dependent"}><i>implementation-dependent</i></GlossaryTerm>. The <GlossaryTerm  term={"value"}><i>values</i></GlossaryTerm> of <GlossaryTerm styled={true} term={"environment parameter"}><i>environment parameters</i></GlossaryTerm> to <GlossaryTerm styled={true} term={"macro function"}><i>macro functions</i></GlossaryTerm> are examples of <GlossaryTerm styled={true} term={"environment object"}><i>environment objects</i></GlossaryTerm>. 



The <GlossaryTerm  term={"object"}><i>object</i></GlossaryTerm> <DictionaryLink  term={"nil"}><b>nil</b></DictionaryLink> when used as an <GlossaryTerm styled={true} term={"environment object"}><i>environment object</i></GlossaryTerm> denotes the <GlossaryTerm styled={true} term={"null lexical environment"}><i>null lexical environment</i></GlossaryTerm>; see Section 3.1.1.3.1 (The Null Lexical Environment). 



