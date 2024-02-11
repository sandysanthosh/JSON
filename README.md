# JSON

->json local storage:

Json Visualization;

https://jsoncrack.com/


->array:

    var names=["santhosh","ranjith","yogi","rahul"];

->local storage set key and value pair:
->stringify:

      localstorage.setItem("belgian",Json.stringify(names));

->To retrieve we need to pass only key value:

      var movies=localstorage.getItem("belgian");

->TO test this:

        alert(movies);
