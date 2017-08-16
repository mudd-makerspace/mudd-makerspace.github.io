#Makerspace Supplies

Below is a list of all of our supplies! If there is anything you would like that you don't see listed, submit a suggestion at the bottom. If we are out of anything that's listed here, let us know by clicking the "We're out!" button. If you use the last of the supplies, please click the we're out button, so we can get more as soon as possible. If you want to use a lot of some supply, please fill out a project request form.

##Supplies List
| Part | Location | Are we out? |
--- | --- | ---


<h2>The XMLHttpRequest Test</h2>


<table id="demo"></table>

<script>
var xhttp = new XMLHttpRequest();
xhttp.onreadystatechange = function() {
if (this.readyState == 4 && this.status == 200) {
  myFunction(this);
}
};
xhttp.open("GET", "cd_catalog.xml", true);
xhttp.send();

function myFunction(xml) {
  var i;
  var xmlDoc = xml.responseXML;
  var table="<tr><th>Artist</th><th>Title</th></tr>";
  var x = xmlDoc.getElementsByTagName("CD");
  for (i = 0; i <x.length; i++) { 
    table += "<tr><td>" +
    x[i].getElementsByTagName("ARTIST")[0].childNodes[0].nodeValue +
    "</td><td>" +
    x[i].getElementsByTagName("TITLE")[0].childNodes[0].nodeValue +
    "</td></tr>";
  }
  document.getElementById("demo").innerHTML = table;
}
</script>