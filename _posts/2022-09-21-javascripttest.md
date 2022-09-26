---
toc: true
layout: post
title: Javascript Practice
description: Practicing using javascript
image: https://www.ikea.com/us/en/images/products/ingo-table-pine__0737092_pe740877_s5.jpg
permalink: /week5/js-table
---

## Javascript Practice
- Testing input of javascript and converting to table / JSON

### Table Output

<br>

<input id="termvalue1" type="text" placeholder="Enter a name">
<input id="termvalue2" type="text" placeholder="Enter an age">
<input id="termvalue3" type="text" placeholder="Enter a grade">
<button id="enterterm" type="submit" onclick="enterterm()">Enter Value</button>

<table id="mainTable">
    <tr>
        <th> ID </th>
        <th> Name </th>
        <th> Age </th>
        <th> Grade </th>
    </tr>


</table>

<br>

### Raw JSON Output

<div id="rawJSON"></div>


<script>

    // Get each box for the dictionary
    var iBox = document.getElementById("termvalue1");
    var jBox = document.getElementById("termvalue2");
    var kBox = document.getElementById("termvalue3");
    var mainTable = document.getElementById("mainTable");
    var rawTable = document.getElementById("rawJSON");

    // Add enter key event listeners
    iBox.addEventListener('keyup', function(event) {

        if (event.keyCode === 13) {
            event.preventDefault();
            document.getElementById("enterterm").click();
        }
    });
    jBox.addEventListener('keyup', function(event) {

        if (event.keyCode === 13) {
            event.preventDefault();
            document.getElementById("enterterm").click();
        }
    });
    kBox.addEventListener('keyup', function(event) {

        if (event.keyCode === 13) {
            event.preventDefault();
            document.getElementById("enterterm").click();
        }
    });


    var counter = 0
    
    var iBody = []

    var list = "";

    function enterterm() {
            // Set values the first time an input happens
            var tempBody = {id: counter, name: iBox.value, age: jBox.value, grade: kBox.value};
            counter++;
            iBody.push(tempBody);
            appendTable(tempBody);
            jsonval = JSON.stringify(iBody);
            rawTable.innerHTML = jsonval;
        }

    function appendTable(row) {
        var trdiv = document.createElement("tr");
        var td1 = document.createElement("td"); td1.innerHTML = row["id"]; trdiv.appendChild(td1);
        var td2 = document.createElement("td"); td2.innerHTML = row["name"]; trdiv.appendChild(td2);
        var td3 = document.createElement("td"); td3.innerHTML = row["age"]; trdiv.appendChild(td3);
        var td4 = document.createElement("td"); td4.innerHTML = row["grade"]; trdiv.appendChild(td4);

        mainTable.appendChild(trdiv);
    }

</script>

## Code 
- Here is the raw code if you would like to take a look
```javascript

    // Get each box for the dictionary
    var iBox = document.getElementById("termvalue1");
    var jBox = document.getElementById("termvalue2");
    var kBox = document.getElementById("termvalue3");
    var mainTable = document.getElementById("mainTable");
    var rawTable = document.getElementById("rawJSON");

    // Add enter key event listeners
    iBox.addEventListener('keyup', function(event) {

        if (event.keyCode === 13) {
            event.preventDefault();
            document.getElementById("enterterm").click();
        }
    });
    jBox.addEventListener('keyup', function(event) {

        if (event.keyCode === 13) {
            event.preventDefault();
            document.getElementById("enterterm").click();
        }
    });
    kBox.addEventListener('keyup', function(event) {

        if (event.keyCode === 13) {
            event.preventDefault();
            document.getElementById("enterterm").click();
        }
    });


    var counter = 0
    
    var iBody = []

    var list = "";

    function enterterm() {
            // Set values the first time an input happens
            var tempBody = {id: counter, name: iBox.value, age: jBox.value, grade: kBox.value};
            counter++;
            iBody.push(tempBody);
            appendTable(tempBody);
            jsonval = JSON.stringify(iBody);
            rawTable.innerHTML = jsonval;
        }

    function appendTable(row) {
        var trdiv = document.createElement("tr");
        var td1 = document.createElement("td"); td1.innerHTML = row["id"]; trdiv.appendChild(td1);
        var td2 = document.createElement("td"); td2.innerHTML = row["name"]; trdiv.appendChild(td2);
        var td3 = document.createElement("td"); td3.innerHTML = row["age"]; trdiv.appendChild(td3);
        var td4 = document.createElement("td"); td4.innerHTML = row["grade"]; trdiv.appendChild(td4);

        mainTable.appendChild(trdiv);
    }
```