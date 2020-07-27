<!DOCTYPE html>
<html>
<body>
<h1>Hello, World</h1>
<script type="text/javascript">
var d = new Date(); 
var n = d.getTime(); //gets the number of milliseconds since 1970-01-01 00:00

var s = n/1000;
var m = s/60;
var h = m/60;
var d = h/24;

var y = Math.floor(1970+(d/365.25));
var D = Math.floor(d%365.25);
var H = Math.floor((h+2)%24); //at the time of writing this my local time was GMT+2
var M = Math.floor(m%60);
var S = Math.floor(s%60);

if(H<10) {  //I don't know a better way than using three layers of if else statements. If you do, please contact unsmokedweed@gmail.com
  if(M<10) {
    if(S<10) {
      console.log(y+'/'+D+' 0'+H+':0'+M+':0'+S); 
    } else {
      console.log(y+'/'+D+' 0'+H+':0'+M+':'+S);
    };
  } else {
    if(S<10) {
      console.log(y+'/'+D+' 0'+H+':'+M+':0'+S);
    } else {
      console.log(y+'/'+D+' 0'+H+':'+M+':'+S);
    };
  };
} else {
  if(M<10) {
    if(S<10) {
      console.log(y+'/'+D+' '+H+':0'+M+':0'+S); 
    } else {
      console.log(y+'/'+D+' '+H+':0'+M+':'+S);
    };
  } else {
    if(S<10) {
      console.log(y+'/'+D+' '+H+':'+M+':0'+S);
    } else {
      console.log(y+'/'+D+' '+H+':'+M+':'+S);
    };
  };
};
</script>
</body>
