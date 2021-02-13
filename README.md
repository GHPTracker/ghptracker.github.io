![GHPTracker](https://avatars.githubusercontent.com/u/78993645?s=200&v=4){:height="100" width="100" style="float: left; padding: 10px"}

# ghptracker.github.io

Make sure you update [Your GHP Repo Name] in the code with your Git Hub Pages repo name.

GHPTracker is powered by [DataStax Astra](https://astra.datastax.com).

## Add Tracker Snippet
```js
<!-- start GHP Listener -->
<script type="text/javascript">
var GHP_siteid='[Your GHP Repo Name]'; 
var GHP_refer = encodeURIComponent(document.referrer);
var GHP_url = encodeURIComponent(document.URL);
var ghpscript_url = ("https:" == document.location.protocol ? "https://" : "http://") + "ghptracker.site/track/" + "?siteid=" + GHP_siteid + "&refer=" + GHP_refer + "&url=" + GHP_url;
var GHP_object = new XMLHttpRequest();
GHP_object.open("GET", ghpscript_url, false);
GHP_object.send(null);
</script>
<!-- end GHP Listener -->
```
## First Widget: Counter
![CounterExample](https://img.shields.io/badge/views-870-blue)
```js
<!-- end GHP Counter -->
<div id="GHP_counter"></div>
<script type="text/javascript">
var GHP_siteid='[Your GHP Repo Name]';
var GHP_url = ("https:" == document.location.protocol ? "https://" : "http://") + "ghptracker.site/counter/?siteid=" + GHP_siteid;
var GHP_object = new XMLHttpRequest();
GHP_object.open("GET", GHP_url, false);
GHP_object.send(null);
var obj = JSON.parse(GHP_object.response);
document.getElementById("GHP_counter").innerHTML += '<img src="//img.shields.io/badge/views-' + obj.counter.value + '-blue">';
</script>
<!-- end GHP Counter -->
```
