# C# Style Guidelines

This is a guide for styling C# code, summarised from MS guidelines and other places.

This guide was created by [Dan Petitt](http://www.coderanger.com/) and is
licensed under the [CC BY-SA 3.0](http://creativecommons.org/licenses/by-sa/3.0/)
license. You are encouraged to fork this repository and make adjustments
according to your preferences.

![Creative Commons License](http://i.creativecommons.org/l/by-sa/3.0/88x31.png)

First off, install and use [StyleCop] (http://stylecop.codeplex.com)

## Element Ordering

Elements at the file root level or within a namespace must be positioned in the following order:
* Extern Alias Directives
* Using Directives
* Namespaces
* Delegates
* Enums
* Interfaces
* Structs
* Classes

Within a class, struct, or interface, elements must be positioned in the following order:
* Fields
* Constructors
* Finalizers (Destructors)
* Delegates
* Events
* Enums
* Interfaces
* Properties
* Indexers
* Methods
* Structs
* Classes

## Capitalisation
### Casing Styles
#### Pascal Casing
The first letter in the identifier and the first letter of each subsequent concatenated word are capitalized. You can use Pascal case for identifiers of three or more characters. For example:

    BackColor

#### Camel Casing
The first letter of an identifier is lowercase and the first letter of each subsequent concatenated word is capitalized. For example:

    backColor

#### Uppercase
All letters in the identifier are capitalized. For example:

    IO

### Capitalization Rules for Identifiers
**Names cannot differ by case alone**

When an identifier consists of multiple words, do not use separators, such as underscores ("_") or hyphens ("-"), between words. Instead, use casing to indicate the beginning of each word.

**USE Pascal casing for all public member, type, and namespace names consisting of multiple words**

(Note that this rule does not apply to instance fields as you should not use public instance fields, but private fields accessed by public Properties.)

**USE camel casing for parameter and variable names**

### Capitalization Rules for Acronyms
An acronym is a word that is formed from the letters of words in a term or phrase. For example, HTML is an acronym for Hypertext Markup Language. You should include acronyms in identifiers only when they are widely known and well understood. Acronyms differ from abbreviations in that an abbreviation shortens a single word. For example, ID is an abbreviation for identifier. In general, library names should not use abbreviations.

> **Note: The two abbreviations that can be used in identifiers are ID and OK.
> In Pascal-cased identifiers they should appear as Id, and Ok.
> If used as the first word in a camel-cased identifier, they should appear as id and ok, respectively.**

Casing of acronyms depends on the length of the acronym.

| Characters  | Type          |
|-------------|---------------|
| 2           | Short Acronym |
| 3+          | Long Acronym  |

The identifier casing rules take precedence over acronym casing rules.

**DO** capitalize both characters of two-character acronyms, except when its the first word of a camel-cased identifier. Examples: DBRate or ioChannel

**DO** capitalize only the first character of acronyms with three or more characters, except the first word of a camel-cased identifier. Examples:  XmlWriter or htmlReader

**DO NOT** capitalize any of the characters of any acronyms, whatever their length, at the beginning of a camel-cased identifier. Example: xmlStream or dbServerName

### Capitalization Rules for Compound Words and Common Terms
**DO NOT** capitalize each word in so-called closed-form compound words. These are compound words written as a single word, such as 'endpoint' or 'hashtable'.

The following list identifies some common terms that are not closed-form compound words. The word is shown in Pascal casing followed by the camel-cased form in parentheses.

| Term       |  camelCase   |
|------------|--------------|
| BitFlag    | (bitFlag)    |
| FileName   | (fileName)   |
| LogOff     | (logOff)     |
| LogOn      | (logOn)      |
| SignIn     | (signIn)     |
| SignOut    | (signOut)    |
| UserName   | (userName)   |
| WhiteSpace | (whiteSpace) |

### References
http://msdn.microsoft.com/en-us/library/vstudio/ms229043(v=vs.100).aspx
http://msdn.microsoft.com/en-us/library/vstudio/ms229059(v=vs.100).aspx
