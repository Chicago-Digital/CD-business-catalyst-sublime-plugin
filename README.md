Business Catalyst Liquid Snippets Triggers
==================

A sublime plugin complete with Adobe Business Catalyst Liquid elements.

Feel free to let me know what else you want added via:

- Twitter [@PhilMarcuson](https://twitter.com/philmarcuson)
- [Issues](https://github.com/PhilMarcuson/business-catalyst-sublime-plugin/issues)


## What's included - contents
- [Installation](#installation)
- [Usage](#usage)
- [Help](#help)
- [IF](#if)
- [IFELSE](#ifelse)
- [UNLESS](#unless)
- [CASE](#case)
- [FOR](#for)
- [FORLOOPS](#forloops)
- [CYCLE](#cycle)
- [INCLUDE](#include)
- [ASSIGN](#assign)
- [CAPTURE](#capture)
- [COMMENT](#comment)
- [RAW](#raw)
- [TABLEROW](#tablerow)
- [GLOBALS](#globals)
- [License](#license)


### Installation

There are 3 methods for installing this plugin.

1. Search for "Business Catalyst Liquid Snippets" via the "Package Control: Install Packages" menu.
**Note:** If you don't have Sublime Package Control installed, you can find out how to install it here [https://sublime.wbond.net/installation](https://sublime.wbond.net/installation)

2. Clone the repository into your Sublime Text 2/3 packages directory.
`git clone https://github.com/PhilMarcuson/business-catalyst-sublime-plugin.git`

3. Download the .zip file and unzip it into your Sublime Text 2/3 packages directory.
**Note:** You can find your Sublime Text 2/3 packages directory by going to Preferences > Browse Packages.

---


### Usage

**all files**: Start typing bcl- in any file along with the element name (see below) and then press 'Tab' to autocomplete the entry.  Once you have the snippet on the page, you can [tab] through the liquid logic to provide your inputs.

**html files**: Start typing `<bcl` in any html file and the autocomplete window opens. It matches fuzzily. So you can type `<bcl-i` to find the `bcl-ifelse` snippet.

Be sure you have enabled "<" in your Preferences.sublime-settings:

`"auto_complete_triggers": [ {"selector": "text.html", "characters": "<"} ],`

---


### Help

Most Liquid logic tags have help snippets.  Append `-help` to the tag and the snippet will provide a prefilled sample to get you started.

You may also find more helpful examples along with other documentation here:  http://docs.businesscatalyst.com/reference/liquid/logic-tags.html

---


### If

Simple if decision block

| Snippet code                   |
| ------------------------------ |
| bcl-if 	 					 |
| bcl-if-help 					 |

**Sample**
```
{% if item.Color == 'red' -%}
	<p>Red is the color</p>
{% endif -%}
```

---


### IfElse

Just like a regular IF condition, the only difference is this adds another possible choice.

| Snippet code                   |
| ------------------------------ |
| bcl-ifelse 					 |
| bcl-ifelse-help				 |

**Sample**
```
{% if item.Color == 'red' -%}
	<p>Red is the color</p>
{% elseif item.Color == 'blue' -%}
	<p>Blue is the color</p>
{% else -%}
	<p>Neither red nor blue.</p>
{% endif -%}
```

---


### Unless

Unless the condition is true the code is executed

| Snippet code                   |
| ------------------------------ |
| bcl-unless 					 |
| bcl-unless-help				 |

**Sample**
```
{% unless item.Color == 'red' -%}
	<p>The color is not red.</p>
{% endunless -%}
```

---


### Case

Do something based on the possible values of a variable. If none of the "known" values are encountered the last "else" branch will be executed.

| Snippet code                   |
| ------------------------------ |
| bcl-case  					 |
| bcl-case-help					 |

**Sample**
```
{% case item.country -%}
	{% when 'DE' -%}
    	Willkommen
	{% when 'ES' -%}
		Bienvenido
	{% when 'EN' -%}
		Welcome
	{% else -%}
    	Bine ai venit
{% endcase -%}
```

---


### For

FOR is used to loop over a collection of items.

| Snippet code                   |
| ------------------------------ |
| bcl-for 						 |
| bcl-for-help					 |

**Sample**
```
{% for item in webapp1.items -%}
<p>
    This item's name is: {{item.name}} 
</p>
{% endfor -%}
```

#### ForLoops

In a FOR loop you can access these variables:

| Description              		 | Snippet code                   |
|------------------------------- | ------------------------------ |
| forloop with autocomplete		 | bcl-forloop 					  |
| length of the entire for loop	 | bcl-forloop-length 			  |
| index of the current iteration | bcl-forloop-index			  |
| index - current (zero based)   | bcl-forloop-index0             |
| how many items left?		  	 | bcl-forloop-rindex			  |
| items left (zero based)		 | bcl-forloop-rindex0			  |
| is this the first iteration?	 | bcl-forloop-first			  |
| is this the last iteration?	 | bcl-forloop-last 			  |
| forloop helper				 | bcl-forloop-help				  |

**Sample**
```
<ul>
{% for item in globals -%}
    <li>{{item[0]}}: {{item[1]}}<br/>
        <p>
            forloop.length is {{forloop.length}} - length of the entire for loop<br/>
            forloop.index is {{forloop.index}}  - index of the current iteration<br/>
            forloop.index0 is {{forloop.index0}} - index of the current iteration (zero based)<br/>
            forloop.rindex is {{forloop.rindex}} - how many items are still left?<br/>
            forloop.rindex0 is  {{forloop.rindex0}} - how many items are still left? (zero based)<br/>
            forloop.first is {{forloop.first}}  - is this the first iteration?<br/>
            forloop.last is {{forloop.last}}   - is this the last iteration? <br/>
        </p>
    </li>
{% endfor -%}
</ul>
```

---


### Cycle

Render one of a few possible items.

| Snippet code                   |
| ------------------------------ |
| bcl-cycle	 					 |
| bcl-cycle-help				 |

**Sample**
```
{% cycle 'red', 'green', 'blue' -%} 
{% cycle 'red', 'green', 'blue' -%} 
{% cycle 'red', 'green', 'blue' -%} 
{% cycle 'red', 'green', 'blue' -%}
```
Renders:
```
red
green
blue
red
```

---


### Include

Include is used to pull data from another page.  You can think of it much like you would think of a content holder. The main difference is when you get a page's contents using include the Liquid objects and collections will become available in your main page.

| Snippet code                   |
| ------------------------------ |
| bcl-include 					 |
| bcl-include-help				 |

**Sample**
```
{%include "/to-be-included.html"-%}
```

---


### Assign

This is used to create a new variable.

| Snippet code                   |
| ------------------------------ |
| bcl-assign 					 |
| bcl-assign-help				 |

**Sample**
```
{% assign new_variable = "my new value" -%}
```

---


### Capture

Assign a block of text, HTML code to a variable.

| Snippet code                   |
| ------------------------------ |
| bcl-capture 	 				 |
| bcl-capture-help 				 |

**Sample**
```
{% capture item_date -%}<span style="color:blue">{{item.releaseDate}}</span>{% endcapture -%}
```

---


### Comment

Comments out a block of text. The text between the comment tags does not render in the front-end.

| Snippet code                   |
| ------------------------------ |
| bcl-comment 					 |
| bcl-comment-help				 |

**Sample**
```
{%comment-%}
	Do not forget to remove comments
{%endcomment-%}
```

---


### Raw

Raw renders liquid markup in plain text.

| Snippet code                   |
| ------------------------------ |
| bcl-raw 	 					 |
| bcl-raw-help 					 |

**Sample**
```
{%raw-%}
	{{this | json}}
{%endraw-%}
```

---


### TableRow

This will draw a table. You can specify how many columns the table will contain using the "cols:" value.

| Snippet code                   |
| ------------------------------ |
| bcl-tablerow 					 |
| bcl-tablerow-help				 |

**Sample**
```
<table>
	{% tablerow item in webapp1.items cols:2 -%}
    	{{item.name}}{{item.counter}}
	{% endtablerow -%}
</table>
```

---


### Globals

http://docs.businesscatalyst.com/reference/liquid/globals.html

| Description              		 | Snippet code                   |
|------------------------------- | ------------------------------ |
| globals tag with automcomplete | bcl-globals					  |
| URL Information				 | bcl-globals-get				  |
| Site information				 | bcl-globals-site 			  |
| User Information (logged in) 	 | bcl-globals-user				  |
| Visitor Information		     | bcl-globals-visitor            |
| Shopping Cart URL		  		 | bcl-globals-cart				  |
| Cookies stored in domain		 | bcl-globals-cookie			  |
| globals helper				 | bcl-globals-help	 			  |

---



### License

Business Catalyst Liquid Snippets is open-sourced software licensed under the [MIT license](/license.txt).
