<!-- default file list -->
*Files to look at*:

* [Form1.cs](./CS/DocumentIteratorExample/Form1.cs) (VB: [Form1.vb](./VB/DocumentIteratorExample/Form1.vb))
* [Program.cs](./CS/DocumentIteratorExample/Program.cs) (VB: [Program.vb](./VB/DocumentIteratorExample/Program.vb))
<!-- default file list end -->
# How to use the Document Iterator object to iterate over document elements


This example creates a <a href="http://help.devexpress.com/#CoreLibraries/clsDevExpressXtraRichEditAPINativeDocumentIteratortopic">DocumentIterator</a> instance for the current document and calls its <a href="http://help.devexpress.com/#CoreLibraries/DevExpressXtraRichEditAPINativeDocumentIterator_MoveNexttopic">MoveNext</a> method to iterate over document elements. A <strong>Visitor pattern </strong>is implemented to process a document element. The implementation is done by calling each element's <a href="http://help.devexpress.com/#CoreLibraries/DevExpressXtraRichEditAPINativeIDocumentElement_Accepttopic">Accept</a>  method with the <strong>MyVisitor</strong> object instance as a parameter. <strong><br>MyVisitor </strong>is a custom class which descends from the <strong>DocumentVisitorBase </strong>class and provides a method that processes <a href="http://help.devexpress.com/#CoreLibraries/clsDevExpressXtraRichEditAPINativeDocumentTexttopic">DocumentText</a> elements to enclose <a href="http://help.devexpress.com/#CoreLibraries/DevExpressXtraRichEditAPINativeCharacterPropertiesBase_Boldtopic">Bold</a> text in asterisks and return all characters without formatting. Paragraph ends are replaced with newline symbols, other document elements are skipped.<br>You can customize MyVisitor class to perform any operation with any type of element which the DocumentIterator encounters.

<br/>


