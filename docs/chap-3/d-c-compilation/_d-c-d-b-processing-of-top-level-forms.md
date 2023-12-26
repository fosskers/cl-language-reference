 



Processing of <GlossaryTerm styled={true} term={"top level form"}><i>top level forms</i></GlossaryTerm> in the file compiler is defined as follows: 



1\. If the <ClLinks  term={"form"}><i>form</i></ClLinks> is a <GlossaryTerm styled={true} term={"compiler macro form"}><i>compiler macro form</i></GlossaryTerm> (not disabled by a <DictionaryLink  term={"notinline"}><b>notinline</b></DictionaryLink> <ClLinks  term={"declaration"}><i>declaration</i></ClLinks>), the <ClLinks  term={"implementation"}><i>implementation</i></ClLinks> might or might not choose to compute the <GlossaryTerm styled={true} term={"compiler macro expansion"}><i>compiler macro expansion</i></GlossaryTerm> of the <ClLinks  term={"form"}><i>form</i></ClLinks> and, having performed the expansion, might or might not choose to process the result as a <GlossaryTerm styled={true} term={"top level form"}><i>top level form</i></GlossaryTerm> in the same processing mode (compile-time-too or not-compile time). If it declines to obtain or use the expansion, it must process the original <ClLinks  term={"form"}><i>form</i></ClLinks>. 



2\. If the form is a <GlossaryTerm styled={true} term={"macro form"}><i>macro form</i></GlossaryTerm>, its <GlossaryTerm styled={true} term={"macro expansion"}><i>macro expansion</i></GlossaryTerm> is computed and processed as a <GlossaryTerm styled={true} term={"top level form"}><i>top level form</i></GlossaryTerm> in the same processing mode (compile-time-too or not-compile-time). 



3\. If the form is a <DictionaryLink  term={"progn"}><b>progn</b></DictionaryLink> form, each of its body <ClLinks  term={"form"}><i>forms</i></ClLinks> is sequentially processed as a <GlossaryTerm styled={true} term={"top level form"}><i>top level form</i></GlossaryTerm> in the same processing mode. 



4\. If the form is a <DictionaryLink  term={"locally"}><b>locally</b></DictionaryLink>, <DictionaryLink  term={"macrolet"}><b>macrolet</b></DictionaryLink>, or <DictionaryLink  term={"symbol-macrolet"}><b>symbol-macrolet</b></DictionaryLink>, <DictionaryLink  term={"compile-file"}><b>compile-file</b></DictionaryLink> establishes the appropriate bindings and processes the body forms as <GlossaryTerm styled={true} term={"top level form"}><i>top level forms</i></GlossaryTerm> with those bindings in effect in the same processing mode. (Note that this implies that the lexical <ClLinks  term={"environment"}><i>environment</i></ClLinks> in which <GlossaryTerm styled={true} term={"top level form"}><i>top level forms</i></GlossaryTerm> are processed is not necessarily the <GlossaryTerm styled={true} term={"null lexical environment"}><i>null lexical environment</i></GlossaryTerm>.) 



5\. If the form is an <DictionaryLink  term={"eval-when"}><b>eval-when</b></DictionaryLink> form, it is handled according to Figure 3–7.  







|**CT LT E Mode Action New Mode**|

| :- |

|<p>Yes Yes — — Process compile-time-too No Yes Yes CTT Process compile-time-too No Yes Yes NCT Process not-compile-time No Yes No — Process not-compile-time Yes No — — Evaluate — </p><p>No No Yes CTT Evaluate — No No Yes NCT Discard — No No No — Discard —</p>|





**Figure 3–7. EVAL-WHEN processing** 



Column **CT** indicates whether :compile-toplevel is specified. Column **LT** indicates whether :load-toplevel is specified. Column **E** indicates whether :execute is specified. Column **Mode** indicates the processing mode; a dash (—) indicates that the processing mode is not relevant. 



The
 **Action**
 column specifies one of three actions: 



**Process:** process the body as <GlossaryTerm styled={true} term={"top level form"}><i>top level forms</i></GlossaryTerm> in the specified mode. 



**Evaluate:** evaluate the body in the dynamic execution context of the compiler, using the <GlossaryTerm styled={true} term={"evaluation environment"}><i>evaluation environment</i></GlossaryTerm> as the global environment and the <GlossaryTerm styled={true} term={"lexical environment"}><i>lexical environment</i></GlossaryTerm> in which the <DictionaryLink  term={"eval-when"}><b>eval-when</b></DictionaryLink> appears. 



**Discard:** ignore the <ClLinks  term={"form"}><i>form</i></ClLinks>. 



The **New Mode** column indicates the new processing mode. A dash (—) indicates the compiler remains in its current mode. 



6\. Otherwise, the form is a <GlossaryTerm styled={true} term={"top level form"}><i>top level form</i></GlossaryTerm> that is not one of the special cases. In compile time-too mode, the compiler first evaluates the form in the evaluation <ClLinks  term={"environment"}><i>environment</i></ClLinks> and then minimally compiles it. In not-compile-time mode, the <ClLinks  term={"form"}><i>form</i></ClLinks> is simply minimally compiled. All <ClLinks  term={"subform"}><i>subforms</i></ClLinks> are treated as <GlossaryTerm styled={true} term={"non-top-level form"}><i>non-top-level forms</i></GlossaryTerm>. 



Note that <GlossaryTerm styled={true} term={"top level form"}><i>top level forms</i></GlossaryTerm> are processed in the order in which they textually appear in the file and that each <GlossaryTerm styled={true} term={"top level form"}><i>top level form</i></GlossaryTerm> read by the compiler is processed before the next is read. However, the order of processing (including macro expansion) of <ClLinks  term={"subform"}><i>subforms</i></ClLinks> that are not <GlossaryTerm styled={true} term={"top level form"}><i>top level forms</i></GlossaryTerm> and the order of further compilation is unspecified as long as Common Lisp 



semantics are preserved. 



<DictionaryLink  term={"eval-when"}><b>eval-when</b></DictionaryLink> forms cause compile-time evaluation only at top level. Both :compile-toplevel and :load-toplevel situation specifications are ignored for <GlossaryTerm styled={true} term={"non-top-level form"}><i>non-top-level forms</i></GlossaryTerm>. For *non-top-level*  







<ClLinks  term={"form"}><i>forms</i></ClLinks>, an <DictionaryLink  term={"eval-when"}><b>eval-when</b></DictionaryLink> specifying the :execute situation is treated as an <GlossaryTerm styled={true} term={"implicit progn"}><i>implicit progn</i></GlossaryTerm> including the <ClLinks  term={"form"}><i>forms</i></ClLinks> in the body of the <DictionaryLink  term={"eval-when"}><b>eval-when</b></DictionaryLink> <ClLinks  term={"form"}><i>form</i></ClLinks>; otherwise, the <ClLinks  term={"form"}><i>forms</i></ClLinks> in the body are ignored. 



