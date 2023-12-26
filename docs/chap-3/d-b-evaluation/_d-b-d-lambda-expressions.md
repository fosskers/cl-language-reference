 



In a <GlossaryTerm styled={true} term={"lambda expression"}><i>lambda expression</i></GlossaryTerm>, the body is evaluated in a lexical <GlossaryTerm  term={"environment"}><i>environment</i></GlossaryTerm> that is formed by adding the <GlossaryTerm  term={"binding"}><i>binding</i></GlossaryTerm> of each <GlossaryTerm  term={"parameter"}><i>parameter</i></GlossaryTerm> in the <GlossaryTerm styled={true} term={"lambda list"}><i>lambda list</i></GlossaryTerm> with the corresponding <GlossaryTerm  term={"value"}><i>value</i></GlossaryTerm> from the <GlossaryTerm  term={"argument"}><i>arguments</i></GlossaryTerm> to the current lexical <GlossaryTerm  term={"environment"}><i>environment</i></GlossaryTerm>. 



For further discussion of how <GlossaryTerm  term={"binding"}><i>bindings</i></GlossaryTerm> are *established* based on the <GlossaryTerm styled={true} term={"lambda list"}><i>lambda list</i></GlossaryTerm>, see Section 3.4 (Lambda Lists). 



The body of a <GlossaryTerm styled={true} term={"lambda expression"}><i>lambda expression</i></GlossaryTerm> is an <GlossaryTerm styled={true} term={"implicit progn"}><i>implicit progn</i></GlossaryTerm>; the <GlossaryTerm  term={"value"}><i>values</i></GlossaryTerm> it returns are returned by the <GlossaryTerm styled={true} term={"lambda expression"}><i>lambda expression</i></GlossaryTerm>. 



