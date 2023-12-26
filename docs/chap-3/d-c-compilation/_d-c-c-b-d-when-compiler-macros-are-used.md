 



The presence of a <GlossaryTerm styled={true} term={"compiler macro"}><i>compiler macro</i></GlossaryTerm> definition for a <ClLinks  term={"function"}><i>function</i></ClLinks> or <ClLinks  term={"macro"}><i>macro</i></ClLinks> indicates that it is desirable for the <ClLinks  term={"compiler"}><i>compiler</i></ClLinks> to use the expansion of the <GlossaryTerm styled={true} term={"compiler macro"}><i>compiler macro</i></GlossaryTerm> instead of the original <GlossaryTerm styled={true} term={"function form"}><i>function form</i></GlossaryTerm> or <GlossaryTerm styled={true} term={"macro form"}><i>macro form</i></GlossaryTerm>. However, no language processor (compiler, evaluator, or other code walker) is ever required to actually invoke <GlossaryTerm styled={true} term={"compiler macro function"}><i>compiler macro functions</i></GlossaryTerm>, or to make use of the resulting expansion if it does invoke a <GlossaryTerm styled={true} term={"compiler macro function"}><i>compiler macro function</i></GlossaryTerm>. 



When the <ClLinks  term={"compiler"}><i>compiler</i></ClLinks> encounters a <ClLinks  term={"form"}><i>form</i></ClLinks> during processing that represents a call to a *compiler macro name* (that is not declared <DictionaryLink  term={"notinline"}><b>notinline</b></DictionaryLink>), the <ClLinks  term={"compiler"}><i>compiler</i></ClLinks> might expand the <GlossaryTerm styled={true} term={"compiler macro"}><i>compiler macro</i></GlossaryTerm>, and might use the expansion in place of the original <ClLinks  term={"form"}><i>form</i></ClLinks>. 



When <DictionaryLink  term={"eval"}><b>eval</b></DictionaryLink> encounters a <ClLinks  term={"form"}><i>form</i></ClLinks> during processing that represents a call to a *compiler macro name* (that is not declared <DictionaryLink  term={"notinline"}><b>notinline</b></DictionaryLink>), <DictionaryLink  term={"eval"}><b>eval</b></DictionaryLink> might expand the <GlossaryTerm styled={true} term={"compiler macro"}><i>compiler macro</i></GlossaryTerm>, and might use the expansion in place of the original <ClLinks  term={"form"}><i>form</i></ClLinks>. 



There are two situations in which a <GlossaryTerm styled={true} term={"compiler macro"}><i>compiler macro</i></GlossaryTerm> definition must not be applied by any language processor: 



*•* The global function name binding associated with the compiler macro is shadowed by a lexical binding of the function name. 



*•* The function name has been declared or proclaimed <DictionaryLink  term={"notinline"}><b>notinline</b></DictionaryLink> and the call form appears within the scope of the declaration. 



It is unspecified whether <GlossaryTerm styled={true} term={"compiler macro"}><i>compiler macros</i></GlossaryTerm> are expanded or used in any other situations.
 