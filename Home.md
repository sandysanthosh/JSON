Welcome to the Java-JSON wiki!


->JSON:

* java script object notation
* lightweight data interchange fomrat
* easy to read and write than xml
* language independetn
* supports array,object,string,number,values


xml:
* simple then json
* doesnt suppor array
* securedd
* less human readable

`{"employee":[`
`{"name":"vimal","email",},`
`{"name":santhosh","rahusl@email.com"},`
`]}`


`xml example:`
`<employees>`
`<employee>`
`<name>santohsh</name>`
`<email>sandssanthosh101</email>`
`</employee>`
`</employees>`

JSON:
* ->object 
* ->array

JSON object:
->key/values

{
"employe":{
"name":"sooo",
"maaired":true,
}
}

JSON ARRAY:
->["sunday","monday","wednesday","thrusday","friday"]

`package com.plural;`

`import org.json.simple.JSONObject;`

`public class JsonExample1{    `
`public static void main(String args[]){    `
`JSONObject obj=new JSONObject();    `
  `obj.put("name","sonoo");    `
  `obj.put("age",new Integer(27));    `
  `obj.put("salary",new Double(600000));    `
   `System.out.print(obj);    `
`}} `   

`import java.util.ArrayList;  `
`import java.util.List;  `
`import org.json.simple.JSONValue;  `
`public class JsonExample1{    `
`public static void main(String args[]){    `
  `List arr = new ArrayList();  `
  `arr.add("sonoo");    `
  `arr.add(new Integer(27));    `
  `arr.add(new Double(600000));   `
  `String jsonText = JSONValue.toJSONString(arr);  `
  `System.out.print(jsonText);  `
`}}    `


The org.json.simple package contains important classes for JSON API.

* JSONValue
* JSONObject
* JSONArray
* JsonString
* JsonNumber


AJAX JSON:

<html>  
<head>  
<meta content="text/html; charset=utf-8">  
<title>AJAX JSON by Javatpoint</title>  
<script type="application/javascript">  
function load()  
{  
   var url = "http://date.jsontest.com/";//use any url that have json data  
   var request;  
  
   if(window.XMLHttpRequest){    
    request=new XMLHttpRequest();//for Chrome, mozilla etc  
   }    
   else if(window.ActiveXObject){    
    request=new ActiveXObject("Microsoft.XMLHTTP");//for IE only  
   }    
   request.onreadystatechange  = function(){  
      if (request.readyState == 4  )  
      {  
        var jsonObj = JSON.parse(request.responseText);//JSON.parse() returns JSON object  
        document.getElementById("date").innerHTML =  jsonObj.date;  
        document.getElementById("time").innerHTML = jsonObj.time;  
      }  
   }  
   request.open("GET", url, true);  
   request.send();  
}  
</script>  
</head>  
<body>  
  
Date: <span id="date"></span><br/>  
Time: <span id="time"></span><br/>  
  
<button type="button" onclick="load()">Load Information</button>  
</body>  
</html> 




