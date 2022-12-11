# LabBench.Repository
Template for LabBench Repositories



# What is XML files

XML (Extensible Markup Language) is a markup language that is used to structure, store, and transport data. XML files are text files that use XML tags to define the structure and content of the data they contain. These tags allow the data to be organized into a hierarchical structure, with different levels of information corresponding to different levels of the hierarchy. XML files can be used to store a wide range of different types of data, including text, numbers, images, and other multimedia content. XML files are often used to exchange data between different systems or applications, as they provide a standardized format that can be easily read and interpreted by a variety of different programs.

Here is an example of an XML file that uses attributes to store information about books in a library:

```xml
<library>
  <book id="1" available="true">
    <title>The Catcher in the Rye</title>
    <author>J.D. Salinger</author>
    <genre>Fiction</genre>
    <year>1951</year>
  </book>
    <title>The Great Gatsby</title>
    <author>F. Scott Fitzgerald</author>
    <year>1925</year>
  </book>
  <book id="3" available="true">
    <title>Moby-Dick</title>
    <author>Herman Melville</author>
    <genre>Fiction</genre>
    <year>1851</year>
  </book>
</library>
```

In this example, each <book> element has two attributes: id and available. The id attribute provides a unique identifier for each book, while the available attribute indicates whether the book is currently available for checkout from the library. 

In XML, an attribute is a piece of metadata that is associated with an element and provides additional information about the element. An attribute is specified using name-value pairs within the opening tag of the element. For example, the following XML element uses an attribute to provide a unique identifier for the element:

```xml
<book id="1">
  ...
</book>
```

In this example, the book element has an id attribute with a value of 123456. This attribute provides a way to identify the specific book that is being described in the element. Attributes are a useful way to include additional information about an element in an XML file, without adding additional levels to the hierarchical structure of the file. They can be used to provide metadata or other information that is associated with an element, but that is not part of the element's main content.

Here is a more relevant example; the repository.xml which defines the contents of a LabBench Repository:

```xml
<?xml version="1.0" encoding="utf-8" ?>
<repository xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
            xsi:schemaLocation="http://labbench.io https://labbench.io/xsd/dev/repository.xsd"
            id="example.labbench.io">
    <protocols>
        <protocol id="cpardemo"
                  location="CPARDEMO/"
                  protocol="cpardemo.prtx"
                  name="CPAR Demonstration Protocol" />

        <protocol id="scriptdemo"
                  location="SCRIPTDEMO/"
                  protocol="scriptdemo.prtx"
                  name="Scripting Demonstration Protocol" />

        <protocol id="thrdemo"
                  location="THRDEMO/"
                  protocol="thrdemo.prtx"
                  name="Threshold Demonstration Protocol" />

        <protocol id="sounddemo"
                  location="SOUNDDEMO\"
                  protocol="sounddemo.prtx"
                  name="Sound Demonstration Protocol" />
    </protocols>
</repository>
```

This repository XML file contains a list of protocols that are available in a particular repository. The file begins with an XML declaration that specifies the version of XML and the character encoding used in the file. 

The file then defines a repository element that includes several attributes, including an id attribute that identifies the repository. Within the repository element, there are a protocol elements each of which describes a different protocol that is available in the repository. 

Each protocol element includes several attributes that provide information about the protocol, such as its location, file name, and a description of its purpose. This XML file uses a hierarchical structure to organize the information about the protocols, with the repository element at the top level and the protocol elements at a lower level.

Despite the content of the two examples used in this explanation are very different; 

1. a catalog of books in a library, and
2. and an exampple of the actual format that LabBench uses to store information about the protocols in a repository.

Both examples are written in XML, which is a simple text based formats where you only need to know two fundamental concepts in order to write valid XML:

1. XML Elements: in XML, an element is a structural unit that is used to organize and contain data. An element consists of a start tag, content, and an end tag. The start and end tags define the boundaries of the element, and the content is the data that is contained within the element. Elements can contain other elements, as well as text, numbers, and other types of data. Elements are an important part of the structure of an XML document, and they provide a way to organize and group related data.
2. XML Attributes: In XML, an attribute is a piece of metadata that is associated with an element and provides additional information about the element. An attribute is specified using name-value pairs within the opening tag of the element. Attributes are a useful way to include additional information about an element in an XML file, without adding additional levels to the hierarchical structure of the file. They can be used to provide metadata or other information that is associated with an element, but that is not part of the element's main content.

With these two concepts you can write valid XML. However, as XML is a general purpose format that can be used to describe any data set in a human and machine readable format, you must also know what are valid elements and attributes for the files that LabBench needs for repositories and experimental protocols.

However, you do not need to memorize these as with the right tools (such as Visual Studio Community Edition) you can get what is known as code completion. Code completion is a feature of many code editors and integrated development environments (IDEs) that will help you to write code more quickly and accurately. When you begin typing a piece of code, the code editor or IDE will display a list of possible completions based on the characters that have been typed so far. You can then choose one of the suggested completions, which the editor or IDE will automatically insert into the code. This can save you time and effort by reducing the need to type out long or complex code constructs. Code completion will also help prevent errors by suggesting only valid completions based on the context of the code.

In the repository.xml example above code completion is enabled by the following lines:

```xml
<repository xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
            xsi:schemaLocation="http://labbench.io https://labbench.io/xsd/dev/repository.xsd">
```

The xmlns:xsi attribute is an XML namespace that specifies the location of the XML Schema Definition (XSD) schema that is used to define the XML file. The xsi:schemaLocation attribute specifies the location of the specific XSD schema that is used by the XML file. These attributes provide information that are used to validate the XML file and ensure that it conforms to the specified schema, and to provide code completion with a suitable editor such as Visual Studio.

An XML schema is a document that defines the structure, content, and constraints for an XML file. An XML schema specifies the elements and attributes that can appear in an XML document, as well as the rules for how these elements and attributes can be used. For example, an XML schema might define the set of elements that can appear in an XML file, the attributes that can be associated with each element, and the order in which the elements must appear in the file. By defining the structure and constraints for an XML document, an XML schema provides a way to ensure that the XML files that are created using the schema are well-formed and contain valid data. XML schemas are typically written in the XML Schema Definition (XSD) language, which is a language specifically designed for defining XML schemas.