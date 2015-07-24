#JS v. jQuery

Here is a list of common jQuery tasks with their JS counterparts.

## Seeing if the Document is ready

### jQuery

<pre>
$(document).ready(function() {
	// code…
});
</pre>

### JS

<pre>
document.addEventListener("DOMContentLoaded", function() {
	// code…
});
</pre>

## Selecting Divs

### jQuery

var divs = $("div");
</pre>

### JS

<pre>
var divs = document.querySelectorAll("div");
</pre>

## Creating Divs

### jQuery

<pre>
var newDiv = $("&lt;div/>");
</pre>

### JS

<pre>
var newDiv = document.createElement("div");
</pre>

## Adding a Class

### jQuery

<pre>
newDiv.addClass("foo");
</pre>

### JS

<pre>
newDiv.classList.add("foo");
</pre>

## Toggling a Class

### jQuery

<pre>
newDiv.toggleClass("foo");
</pre>

### JS

<pre>
newDiv.classList.toggle("foo");
</pre>

## On Click

### jQuery

<pre>
$("a").click(function() {
	// code…
});
</pre>

### JS

<pre>
[].forEach.call(document.querySelectorAll("a"), function(el) {
	el.addEventListener("click", function() {
		// code…
	});
});
</pre>

## Appending Divs

### jQuery

<pre>
$("body").append($("&lt;p/>"));
</pre>

### JS

<pre>
document.body.appendChild(document.createElement("p"));
</pre>

## Setting Attributes

### jQuery

<pre>
$("img").filter(":first").attr("alt", "My image");
</pre>

### JS

<pre>
document.querySelector("img").setAttribute("alt", "My image");
</pre>

## Setting Parent

### jQuery

<pre>
var parent = $("#about").parent();
</pre>

### JS

<pre>
var parent = document.getElementById("about").parentNode;
</pre>

## Cloning Element

### jQuery

<pre>
var clonedElement = $("#about").clone();
</pre>

### JS

<pre>
var clonedElement = document.getElementById("about").cloneNode(true);
</pre>

## Emptying an Element

### jQuery

<pre>
$("#wrap").empty();
</pre>

### JS

<pre>
var wrap = document.getElementById("wrap");
while(wrap.firstChild) wrap.removeChild(wrap.firstChild);
</pre>

## Testing if an Element is Empty

### jQuery

<pre>
if($("#wrap").is(":empty"))
</pre>

### JS

<pre>
if(!document.getElementById("wrap").hasChildNodes())
</pre>

## Next Element

### jQuery

<pre>
var nextElement = $("#wrap").next();
</pre>

### JS

<pre>
var nextElement = document.getElementById("wrap").nextSibling;
</pre>
