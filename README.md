Business Catalyst Liquid Snippets
==================

A sublime plugin complete with Adobe Business Catalyst Liquid elements.

Feel free to let me know what else you want added via:

- Twitter [@PhilMarcuson](https://twitter.com/philmarcuson)
- [Issues](https://github.com/PhilMarcuson/business-catalyst-sublime-plugin/issues)


## What's included - contents
- [Installation](#installation)
- [IF](#if)
- [IF else](#ifelse)
- [UNLESS](#unless)
- [CASE](#case)
- [FOR](#for)
- [FORLOOP](#forloop)
- [CYCLE](#cycle)
- [INCLUDE](#include)
- [ASSIGN](#assign)
- [CAPTURE](#capture)
- [COMMENT](#comment)
- [RAW](#raw)
- [TABLEROW](#tablerow)
- [GLOBALS](#globals)
- [LICENSE](#license)


### Installation

There are 3 methods for installing this plugin.

1. Search for "Business Catalyst Liquid Snippets" via the "Package Control: Install Packages" menu.
**Note:** If you don't have Sublime Package Control installed, you can find out how to install it here [https://sublime.wbond.net/installation](https://sublime.wbond.net/installation)

2. Clone the repository into your Sublime Text 2/3 packages directory.
`git clone https://github.com/PhilMarcuson/business-catalyst-sublime-plugin.git

3. Download the .zip file and unzip it into your Sublime Text 2/3 packages directory.
**Note:** You can find your Sublime Text 2/3 packages directory by going to Preferences > Browse Packages.


### Usage

_all_ files: Start typing bcl- in any file along with the element name (see below) and then press 'Tab' to autocomplete the entry

_html_ files: Start typing `<bcl` in any html file and the autocomplete window opens. It matches fuzzily. So you can type `<bcl-i` to find the `bcl-ifelse` snippet.

Be sure you have enabled "<" in your Preferences.sublime-settings:

`"auto_complete_triggers": [ {"selector": "text.html", "characters": "<"} ],`

### If

| Description                    | Snippet code                   |
|------------------------------- | :-----------------------------:|
| Simple if decision block       | bcl-if                         |
| Help		     				 | bcl-if-help     			  	  |

### If Else

| Description                    | Snippet code					  |
|------------------------------- | :-----------------------------:|
| Just like a regular IF condition, the only difference is this adds another possible choice.  | bcl-ifelse					  |

### Templates

| Description                    | Snippet code                   |
|------------------------------- | :-----------------------------:|
| HTML5 Template Layout          | bs3-template:html5             |

### Forms

| Description     				 | Snippet code        			  |
|------------------------------- | :-----------------------------:|
| Form            				 | bs3-form            			  |
| Inline Form     				 | bs3-form:inline     			  |
| Horizontal Form 				 | bs3-form:horizontal 			  |

### Tables

| Description              		 | Snippet code                   |
|------------------------------- | :----------------------------: |
| Table                    		 | bs3-table                      |
| Bordered Table           		 | bs3-table:bordered             |
| Condensed Table          		 | bs3-table:condensed            |
| Hover Table              		 | bs3-table:hover                |
| Striped Table            		 | bs3-table:striped              |

### Input Fields (Form fields)

**Note:** you can add " :h " to the end of any input field snippet to make it compatible with Bootstrap 3 horizontal forms. **E.g.**
- bs3-input:text:h
- bs3-input:hidden:h


| Description              		 | Snippet code                   | Options |
|------------------------------- | :----------------------------: | :-----:	|
| Label		 					 | bs3-input:label   			  |    		|
| Text Input               		 | bs3-input:text 				  | :h 		|
| Email Input 					 | bs3-input:email   			  | :h 		|
| Password Input				 | bs3-input:password  			  | :h 		|
| Hidden Input					 | bs3-input:hidden  			  | :h 		|
| Url Input						 | bs3-input:url 	 			  | :h 		|
| Color Input 					 | bs3-input:color   			  | :h 		|
| Number Input 					 | bs3-input:number   			  | :h 		|
| Range Input 					 | bs3-input:range   			  | :h 		|
| Date Input 					 | bs3-input:date   			  | :h 		|
| Week Input 					 | bs3-input:week   			  | :h 		|
| Month Input 					 | bs3-input:month   			  | :h 		|
| Time Input 					 | bs3-input:time   			  | :h 		|
| Tel Input 					 | bs3-input:tel   	 			  | :h 		|
| Search Input 					 | bs3-input:search   			  | :h 		|
| Reset Input 					 | bs3-input:reset   			  | :h 		|
| Submit Input 					 | bs3-input:submit   			  | :h 		|
| Checkbox Input 				 | bs3-input:checkbox  			  | :h 		|
| Radio Box Input 				 | bs3-input:radio  			  | :h 		|
| Select Box 	 				 | bs3-select		  			  | :h 		|
| Textarea  	 				 | bs3-textarea		  			  | :h 		|

### Alerts

| Description              		 | Snippet code                   |
|------------------------------- | :----------------------------: |
| Alert Box (Default)			 | bs3-alert 					  |
| Danger Alert Box				 | bs3-alert:danger 			  |
| Info Alert Box				 | bs3-alert:info				  |
| Success Alert Box              | bs3-alert:success              |
| Warning Alert Box				 | bs3-alert:warning			  |

### Badges

| Description              		 | Snippet code                   |
|------------------------------- | :----------------------------: |
| Badge (Default) 				 | bs3-badge 					  |

### Breadcrumbs

| Description                    | Snippet code                   |
|------------------------------- | :----------------------------: |
| Breadcrumbs                    | bs3-breadcrumbs                |

### Carousel

| Description              		 | Snippet code                   |
|------------------------------- | :----------------------------: |
| Carousel	      				 | bs3-carousel	       			  |

### Buttons

**Note:** all button snippets below can have any of the following options append to the end of the snippet *.
- :danger
- :default
- :disabled
- :info
- :primary
- :success
- :warning

**An example:**
- bs3-button:success
- bs3-large-button:disabled
- bs3-block-button:warning

| Description              		 | Snippet code                   | Options |
|------------------------------- | :----------------------------: | :-----:	|
| Button		 				 | bs3-button					  |  *		|
| Block Button	 				 | bs3-block-button				  |  *		|
| Mini Button		 			 | bs3-xs-button				  |	 *		|
| Small Button		 			 | bs3-sm-button				  |	 *		|
| Large Button		 			 | bs3-lg-button				  |	 *		|

### Grid

**Note:** The bs3-col snippet can be used both on its own or with the addition of a colon followed by the number of columns required: **E.g.**

- bs3-col
- bs3-col:6
- bs3-col:12

| Description              		 | Snippet code                   | Options |
|------------------------------- | :----------------------------: | :-----:	|
| Column		 				 | bs3-col						  | :1-12	|
| Row			 				 | bs3-row						  |  		|
| Container		 				 | bs3-container				  |			|

### Icons

| Description                    | Snippet code                   |
|------------------------------- | :-----------------------------:|
| Glyphicon		                 | bs3-icon:glyphicon             |
| Icon (Font Awesome)		     | bs3-icon                       |

### Images

| Description              		 | Snippet code                   |
|------------------------------- | :----------------------------: |
| Thumbnail	 					 | bs3-thumbnail 				  |
| Thumbnail with content		 | bs3-thumbnail:content		  |

### Labels

| Description              		 | Snippet code                   |
|------------------------------- | :----------------------------: |
| Label		 					 | bs3-label 	 				  |
| Danger Label					 | bs3-label:danger				  |
| Info Label					 | bs3-label:info 				  |
| Success Label					 | bs3-label:success			  |
| Warning Label					 | bs3-label:warning			  |

### Pagination

| Description              		 | Snippet code                   |
|------------------------------- | :----------------------------: |
| Pager		 					 | bs3-pager	 				  |
| Aligned Pager             	 | bs3-pager:aligned 			  |
| Pagination					 | bs3-pagination				  |
| Pagination:small				 | bs3-pagination:sm			  |
| Pagination:large				 | bs3-pagination:lg			  |

### Navigation

| Description              		 | Snippet code                   |
|------------------------------- | :----------------------------: |
| Navbar (basic navbar)			 | bs3-navbar	 				  |
| Navbar Brand Element			 | bs3-navbar:brand				  |
| Navbar Button					 | bs3-navbar:button			  |
| Navbar Form 					 | bs3-navbar:form 				  |
| Navbar Link 					 | bs3-navbar:link 				  |
| Navbar Text 					 | bs3-navbar:text 				  |
| Navbar Fixed-Botton			 | bs3-navbar:fixed-bottom		  |
| Navbar Fixed-Top				 | bs3-navbar:fixed-top			  |
| Navbar Inverse				 | bs3-navbar:inverse			  |
| Navbar Responsive				 | bs3-navbar:responsive		  |
| Navbar Static-Top				 | bs3-navbar:static-top		  |

### Jumbotron

| Component                		 | Snippet code                   |
|------------------------------- | :----------------------------: |
| Jumbotron (ex Hero Unit)		 | bs3-jumbotron 				  |

### Panels

| Component                      | Snippet code                   |
|------------------------------- | :----------------------------: |
| Panel                          | bs3-panel                      |
| Panel (contextual)             | bs3-panel:{warning,success,info,danger,primary}                  |
| Panel (with heading)           | bs3-panel:heading              |
| Panel (with footer)            | bs3-panel:footer               |

### List-groups

| Component                      | Snippet code                   |
|------------------------------- | :----------------------------: |
| List group                     | bs3-list-group                 |
| List group (with badges)       | bs3-list-group:badges          |
| List group (linked list)       | bs3-list-group:linked          |
| List group (with content)      | bs3-list-group:content         |

### Media Objects

| Component                      | Snippet code                   |
|------------------------------- | :----------------------------: |
| Media Object                   | bs3-media-object               |

### Clearfix

| Component                      | Snippet code                   |
|------------------------------- | :----------------------------: |
| Clearfix                       | bs3-clearfix                   |

### Wells

| Component                      | Snippet code                   |
|------------------------------- | :----------------------------: |
| Well                           | bs3-well                       |
| Well (small)                   | bs3-well:sm                    |
| Well (large)                   | bs3-well:lg                    |

### Tabs

| Component                      | Snippet code                   |
|------------------------------- | :----------------------------: |
| Tabs pane                      | bs3-tabs				          |

### Input-groups

| Component                      | Snippet code                   |
|------------------------------- | :----------------------------: |
| Input group                    | bs3-input-group                |
| Input group(addon & text-field)| bs3-input-group:addon:text     |
| Input group (addon)            | bs3-input-group-addon          |
| Input group (button)           | bs3-input-group-btn            |
| Input group (text-field & btn) | bs3-input-group:text:btn       |

### License

Business Catalyst Liquid Snippets is open-sourced software licensed under the [MIT license](http://opensource.org/licenses/MIT).