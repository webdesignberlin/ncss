NCSS
====

> NCSS is a paper about CSS naming conventions and best practices.


Why
---

Massive CSS on large scaled websites used to cause following issues:

- Multiple editors without a uniform concept
- Missing context to the website's layout and structure
- Lack of inline documentation


Getting started
---------------

Named Cascading Style Sheets are divided into:

- Structural classes
- Type classes
- Abstract classes
- Functional classes

There is no specification the use hyphen, underscore or camelcase for class names!


Structural classes
------------------

Syntax: <code>.context</code>

<table>
	<thead>
		<tr>
			<th>Name</th>
			<th>Tags</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td>.content</td>
			<td>article, div</td>
		</tr>
		<tr>
			<td>.footer</td>
			<td>div, footer</td>
		</tr>
		<tr>
			<td>.header</td>
			<td>div, header</td>
		</tr>
		<tr>
			<td>.navigation</td>
			<td>div, navi</td>
		</tr>
		<tr>
			<td>.section</td>
			<td>div, section</td>
		</tr>
		<tr>
			<td>.sidebar</td>
			<td>div, aside</td>
		</tr>
		<tr>
			<td>.wrapper</td>
			<td>div</td>
		</tr>
	</tbody>
</table>

<strong>Important:</strong>

Layout and structural classes should never contain a type prefix or abstract suffix.


Type classes
------------

Syntax: <code>.type</code> and <code>.type&#95;context</code>

<table>
	<thead>
		<tr>
			<th>Prefix</th>
			<th>Tags</th>
			<th>Example</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td>.box</td>
			<td>blockquote, div, span</td>
			<td>.box_content</td>
		</tr>
		<tr>
			<td>.button</td>
			<td>a, button</td>
			<td>.button_admin</td>
		</tr>
		<tr>
			<td>.field</td>
			<td>input, select, textarea</td>
			<td>.field_input</td>
		</tr>
		<tr>
			<td>.form</td>
			<td>form</td>
			<td>.form_contact</td>
		</tr>
		<tr>
			<td>.item</td>
			<td>dd, dt, li</td>
			<td>.item_active</td>
		</tr>
		<tr>
			<td>.label</td>
			<td>label, legend</td>
			<td>.label_search</td>
		</tr>
		<tr>
			<td>.link</td>
			<td>a</td>
			<td>.link_action</td>
		</tr>
		<tr>
			<td>.list</td>
			<td>dl, ol, ul</td>
			<td>.list_navigation</td>
		</tr>
		<tr>
			<td>.set</td>
			<td>div, fieldset</td>
			<td>.set_login</td>
		</tr>
		<tr>
			<td>.table</td>
			<td>table</td>
			<td>.table_result</td>
		</tr>
		<tr>
			<td>.text</td>
			<td>span, p</td>
			<td>.text_about</td>
		</tr>
		<tr>
			<td>.title</td>
			<td>h1, h2, h3, h4, h5, h6</td>
			<td>.title_content</td>
		</tr>
	</tbody>
</table>

<strong>Important:</strong>

Structural tags are rather unsuitable to contain a type prefix:

- article
- aside
- footer
- header
- nav
- section


Abstract classes
----------------

Extend with additional description:

Syntax: <code>.type&#95;description</code> and <code>.type&#95;context&#95;description</code>

Extend with current state:

Syntax: <code>.type&#95;state</code> and <code>.type&#95;context&#95;state</code>

Extend with position information:

Syntax: <code>.type&#95;position</code> and <code>.type&#95;context&#95;position</code>

<table>
	<thead>
		<tr>
			<th>Suffix</th>
			<th>Tags</th>
			<th>Example</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td colspan="3">Additional description</td>
		</tr>
		<tr>
			<td>_small</td>
			<td>*</td>
			<td>.item_small</td>
		</tr>
		<tr>
			<td>_large</td>
			<td>*</td>
			<td>.item_large</td>
		</tr>
		<tr>
			<td colspan="3">Current state</td>
		</tr>
		<tr>
			<td>_active</td>
			<td>*</td>
			<td>.item_active</td>
		</tr>
		<tr>
			<td>_idle</td>
			<td>*</td>
			<td>.item_idle</td>
		</tr>
		<tr>
			<td>_hover</td>
			<td>*</td>
			<td>.item_hover</td>
		</tr>
		<tr>
			<td>_touch</td>
			<td>*</td>
			<td>.item_touch</td>
		</tr>
		<tr>
			<td colspan="3">Position information</td>
		</tr>
		<tr>
			<td>_first</td>
			<td>*</td>
			<td>.item_first</td>
		</tr>
		<tr>
			<td>_second</td>
			<td>*</td>
			<td>.item_second</td>
		</tr>
		<tr>
			<td>_third</td>
			<td>*</td>
			<td>.item_third</td>
		</tr>
		<tr>
			<td>_last</td>
			<td>*</td>
			<td>.item_last</td>
		</tr>
		<tr>
			<td>_odd</td>
			<td>*</td>
			<td>.item_odd</td>
		</tr>
		<tr>
			<td>_even</td>
			<td>*</td>
			<td>.item_even</td>
		</tr>
	</tbody>
</table>

<strong>Important:</strong>

Proper handling of type and context should prevent the need of adjoining classes.


Functional classes
------------------

Pure functional classes, marked with the <code>has</code> prefix.

Syntax: <code>.has&#95;action</code> or <code>.has&#95;context</code>

Javascript related classes marked with the <code>js</code> prefix.

Syntax: <code>.js&#95;action</code> or <code>.js&#95;context</code>

<table>
	<thead>
		<tr>
			<th>Prefix</th>
			<th>Tags</th>
			<th>Example</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td>.has</td>
			<td>*</td>
			<td>.has_tooltip</td>
		</tr>
		<tr>
			<td>.js</td>
			<td>*</td>
			<td>.js_click</td>
		</tr>
	</tbody>
</table>

<strong>Important:</strong>

Functional classes should never have declarations for styling.


Example
-------

A class <code>.box&#95;content</code> provides the information of a styled <code>div</code> tag located inside a structural <code>.content</code> container.


HTML:

<pre>
&lt;div class="wrapper"&gt;

	&lt;div id="content" class="content"&gt;
		&lt;h1 class="title_content"&gt;Headline&lt;/h1&gt;
		&lt;div class="box_content"&gt;Content&lt;/div&gt;
	&lt;/div&gt;

	&lt;div id="sidebar" class="sidebar"&gt;
		&lt;h1 class="title_sidebar"&gt;Headline&lt;/h1&gt;
		&lt;div class="box_sidebar"&gt;
			&lt;ul class="list_sidebar"&gt;
				&lt;li&gt;Item&lt;/li&gt;
				&lt;li class="js_active item_active"&gt;Active item&lt;/li&gt;
				&lt;li&gt;Item&lt;/li&gt;
			&lt;/ul&gt;
		&lt;/div&gt;
	&lt;/div&gt;

&lt;/div&gt;
</pre>

CSS:

<pre>
/* boxes */

.box_content
{
	padding: 1em;
}

.box_sidebar
{
	padding: 0.5em;
}

/* titles */

.title_content
{
	color: #555;
}

.title_sidebar
{
	color: #777;
}
</pre>


Conclusion
----------

The goal of NCSS is to provide additional information just by reading unknown CSS.

- What elements, tags and sections are affected
- What is the relation of one CSS class to another
- Where to add related CSS declarations


Thanks
------

[Ronny Springer](https://github.com/ronny-springer) for contribution
