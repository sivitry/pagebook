// ==UserScript==
// @name         pagebook3
// @namespace    http://tampermonkey.net/
// @version      0.3
// @description  try to take over the world!
// @author       You
// @match        http://*/*
// @match        https://*/*
// @grant        none
// ==/UserScript==

window.onload = function() {
    document.onkeydown = pagebook;    
};


function pagebook(e) {
    var lefturl="", righturl="";
    var leftvalue, rightvalue;
    console.log(window.location.href);
    var url = window.location.href;
    var an = document.querySelectorAll('a[href]');
    var surl = url;
    var svalue = 0;
    var eloc = 0;
    eloc = url.lastIndexOf("=");
    surl = url.substring(0, eloc+1);
    svalue = url.substring(eloc+1, url.length);
    //console.log(surl+"\n"+svalue);
    leftvalue = svalue-1;
    rightvalue = svalue-(-1);
    //console.log(leftvalue, rightvalue);
    
    var i;
    for(i =0; i<an.length;i++ ){
        if(an[i].href.startsWith(surl)){
            //console.log(an[i].href);
        }
        if(an[i].href===surl+rightvalue){
            righturl=an[i].href;
            //console.log(an[i].href);
        }
        if(an[i].href===surl+leftvalue){
            lefturl=an[i].href;
            //console.log(an[i].href);
        }
    }
    console.log(righturl);
    console.log(lefturl);

    e = e || window.event;
    switch (e.keyCode) {
        case 37:
            //alert('left');
            if(lefturl!=="")
                location.href = lefturl;
            break;
        case 38:
            //alert('up');
            break;
        case 39:
            if(righturl!=="")
                location.href = righturl;
            break;
        case 40:
            //alert('down');
            break;
    }
}
