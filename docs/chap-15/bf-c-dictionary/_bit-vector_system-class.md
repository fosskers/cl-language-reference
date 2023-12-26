**bit-vector** <GlossaryTerm styled={true} term={"system class"}><i>System Class</i></GlossaryTerm> 



**Class Precedence List:** 



<ClLinks  term={"bit-vector"}><b>bit-vector</b></ClLinks>, <ClLinks  term={"vector"}><b>vector</b></ClLinks>, <ClLinks  term={"array"}><b>array</b></ClLinks>, <ClLinks  term={"sequence"}><b>sequence</b></ClLinks>, <ClLinks  term={"t"}><b>t</b></ClLinks> 



**Description:** 



A <GlossaryTerm styled={true} term={"bit vector"}><i>bit vector</i></GlossaryTerm> is a <ClLinks  term={"vector"}><i>vector</i></ClLinks> the <GlossaryTerm styled={true} term={"element type"}><i>element type</i></GlossaryTerm> of which is <ClLinks  term={"bit"}><i>bit</i></ClLinks>. 



The <ClLinks  term={"type"}><i>type</i></ClLinks> <ClLinks  term={"bit-vector"}><b>bit-vector</b></ClLinks> is a <ClLinks  term={"subtype"}><i>subtype</i></ClLinks> of <ClLinks  term={"type"}><i>type</i></ClLinks> <ClLinks  term={"vector"}><b>vector</b></ClLinks>, for <ClLinks  term={"bit-vector"}><b>bit-vector</b></ClLinks> means (vector bit). 



**Compound Type Specifier Kind:** 



Abbreviating. 



**Compound Type Specifier Syntax:** 



(bit-vector [*size*]) 



**Compound Type Specifier Arguments:** 



*size*—a non-negative <ClLinks  term={"fixnum"}><i>fixnum</i></ClLinks>, or the <ClLinks  term={"symbol"}><i>symbol</i></ClLinks> **\***. 



**Compound Type Specifier Description:** 



This denotes the same <ClLinks  term={"type"}><i>type</i></ClLinks> as the <ClLinks  term={"type"}><i>type</i></ClLinks> (array bit (*size*)); that is, the set of <GlossaryTerm styled={true} term={"bit vector"}><i>bit vectors</i></GlossaryTerm> of size *size*. 



**See Also:** 



Section 2.4.8.4 (Sharpsign Asterisk), Section 22.1.3.6 (Printing Bit Vectors), Section 15.1.2.2 (Required Kinds of Specialized Arrays) 



