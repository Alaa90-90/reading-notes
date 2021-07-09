# DOM
The Document Object Model (DOM) is the data representation of the objects that comprise the structure and content of a document on the web. how the DOM represents an HTML or XML document in memory and how you use APIs to create web content and applications.


![dom](https://devopedia.org/images/article/282/2000.1595439379.jpg)


# What is the DOM?
The Document Object Model (DOM) is a programming interface for HTML and XML documents. It represents the page so that programs can change the document structure, style, and content. The DOM represents the document as nodes and objects. That way, programming languages can connect to the page.

A Web page is a document. This document can be either displayed in the browser window or as the HTML source. But it is the same document in both cases. The Document Object Model (DOM) represents that same document so it can be manipulated. The DOM is an object-oriented representation of the web page, which can be modified with a scripting language such as JavaScript.

The W3C DOM and WHATWG DOM standards are implemented in most modern browsers. Many browsers extend the standard, so care must be exercised when using them on the web where documents may be accessed by various browsers with different DOMs.

For example, the standard DOM specifies that the querySelectorAll method in the code below must return a list of all the <p> elements in the document:

>const paragraphs = document.querySelectorAll("p");
// paragraphs[0] is the first <p> element
// paragraphs[1] is the second <p> element, etc.
>alert(paragraphs[0].nodeName);

All of the properties, methods, and events available for manipulating and creating web pages are organized into objects (for example, the document object that represents the document itself, the table object that implements the special HTMLTableElement DOM interface for accessing HTML tables, and so forth). This documentation provides an object-by-object reference to the DOM.

The modern DOM is built using multiple APIs that work together. The core DOM defines the objects that fundamentally describe a document and the objects within it. This is expanded upon as needed by other APIs that add new features and capabilities to the DOM. For example, the HTML DOM API adds support for representing HTML documents to the core DOM.

# DOM and JavaScript
The short example above, like nearly all of the examples in this reference, is JavaScript. That is to say, it's written in JavaScript, but it uses the DOM to access the document and its elements. The DOM is not a programming language, but without it, the JavaScript language wouldn't have any model or notion of web pages, HTML documents, XML documents, and their component parts (e.g. elements). Every element in a document—the document as a whole, the head, tables within the document, table headers, text within the table cells—is part of the document object model for that document, so they can all be accessed and manipulated using the DOM and a scripting language like JavaScript.

In the beginning, JavaScript and the DOM were tightly intertwined, but eventually, they evolved into separate entities. The page content is stored in the DOM and may be accessed and manipulated via JavaScript, so that we may write this approximative equation:

API = DOM + JavaScript

The DOM was designed to be independent of any particular programming language, making the structural representation of the document available from a single, consistent API. Though we focus exclusively on JavaScript in this reference documentation, implementations of the DOM can be built for any language, as this Python example demonstrates:
>#python DOM example
import xml.dom.minidom as m
doc = m.parse(r"C:\Projects\Py\chap1.xml")
doc.nodeName # DOM property of document object
>p_list = doc.getElementsByTagName("para")
# Fundamental data types
This reference tries to describe the various objects and types in simple terms. But there are a number of different data types being passed around the API that you should be aware of.

The following table briefly describes these data types.

|||      
|------|---------------------------------------------------------------------------------------------------------------------------------|       
|||         
|||      
|||         
|_| )`.`             
       

          
|              
|| |          
|||         



|Data type (Interface|Description|      
|--------------------|-----------|      
|Document    |When a member returns an object of type document (e.g., the ownerDocument property of an element returns the document to which it   belongs), this object is the root document object itself. The DOM document Reference chapter describes the document object.       |      
|Node    |   Every object located within a document is a node of some kind. In an HTML document, an object can be an element node but also a text node or attribute node.    |    
| Element     |    The element type is based on node. It refers to an element or a node of type element returned by a member of the DOM API. Rather than saying, for example, that the document.createElement() method returns an object reference to a node, we just say that this method returns the element that has just been created in the DOM. element objects implement the DOM Element interface and also the more basic Node interface, both of which are included together in this reference. In an HTML document, elements are further enhanced by the HTML DOM API's HTMLElement interface as well as other interfaces describing capabilities of specific kinds of elements (for instance, HTMLTableElement for table elements).    |      
|   Node List    |    node  List is an array of elements, like the kind that is returned by the method `document.querySelectorAll`(/.Items in a node List are accessed by index in either of two ways  1-list.item  ,2-list , ,                        
 These two are equivalent. In the first, item () is the single method on the nodeList object. The latter uses the typical array syntax to fetch the  second item in the list.    |     
|   Attribute  |  When an attribute is returned by a member (e.g., by the createAttribute() method), it is an object reference that exposes a special (albeit small) interface for attributes. Attributes are nodes in the DOM just like elements are, though you may rarely use them as such. |
|   NamedNodeMap     |   A namedNodeMap is like an array, but the items are accessed by name or index, though this latter case is merely a convenience for enumeration, as they are in no particular order in the list. A namedNodeMap has an item() method for this purpose, and you can also add and remove items from a namedNodeMap.   |

There are also some common terminology considerations to keep in mind. It's common to refer to any Attribute node as an attribute, for example, and to refer to an array of DOM nodes as a nodeList. You'll find these terms and others to be introduced and used throughout the documentation.

