#JS v. jQuery

<table>
<thead>
<tr><th>jQuery</th>
<th>JavaScript</th>
</tr>
</thead>
<tbody>
<tr><td>
<pre>
$(document).ready(function() {
	// code…
});
</pre>
</td>
<td>
<pre>
document.addEventListener("DOMContentLoaded", function() {
	// code…
});
</pre>
</td>
</tr>

<tr>
<td>
<pre>
var divs = $("div");
</pre>
</td>
<td>
<pre>
var divs = document.querySelectorAll("div");
</pre>
</td>
</tr>

<tr>
<td>
<pre>
var newDiv = $("&lt;div/>");
</pre>
</td>
<td>
<pre>
var newDiv = document.createElement("div");
</pre>
</td>
</tr>

<tr>
<td>
<pre>
newDiv.addClass("foo");
</pre>
</td>
<td>
<pre>
newDiv.classList.add("foo");
</pre>
</td>
</tr>

<tr>
<td>
<pre>
newDiv.toggleClass("foo");
</pre>
</td>
<td>
<pre>
newDiv.classList.toggle("foo");
</pre>
</td>
</tr>

<tr>
<td>
<pre>
$("a").click(function() {
	// code…
});
</pre>
</td>
<td>
<pre>
[].forEach.call(document.querySelectorAll("a"), function(el) {
	el.addEventListener("click", function() {
		// code…
	});
});
</pre>
</td>
</tr>

<tr>
<td>
<pre>
$("body").append($("&lt;p/>"));
</pre>
</td>
<td>
<pre>
document.body.appendChild(document.createElement("p"));
</pre>
</td>
</tr>

<tr>
<td>
<pre>
$("img").filter(":first").attr("alt", "My image");
</pre>
</td>
<td>
<pre>
document.querySelector("img").setAttribute("alt", "My image");
</pre>
</td>
</tr>

<tr>
<td>
<pre>
var parent = $("#about").parent();
</pre>
</td>
<td>
<pre>
var parent = document.getElementById("about").parentNode;
</pre>
</td>
</tr>

<tr>
<td>
<pre>
var clonedElement = $("#about").clone();
</pre>
</td>
<td>
<pre>
var clonedElement = document.getElementById("about").cloneNode(true);
</pre>
</td>
</tr>

<tr>
<td>
<pre>
$("#wrap").empty();
</pre>
</td>
<td>
<pre>
var wrap = document.getElementById("wrap");
while(wrap.firstChild) wrap.removeChild(wrap.firstChild);
</pre>
</td>
</tr>

<tr>
<td>
<pre>
if($("#wrap").is(":empty"))
</pre>
</td>
<td>
<pre>
if(!document.getElementById("wrap").hasChildNodes())
</pre>
</td>
</tr>

<tr>
<td>
<pre>
var nextElement = $("#wrap").next();
</pre>
</td>
<td>
<pre>
var nextElement = document.getElementById("wrap").nextSibling;
</pre>
</td>
</tr>
</tbody>
</table>