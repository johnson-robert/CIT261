  //Topic 1: Loops, Conditional Statements, Functions, Variables, Parameters, Arrays, Associative Arrays
        
        //For Loop
        for(var i = 0; i <= 10; i++){
            document.write(i);
        }
        document.write("<br/></br>");
        
        //Nested Loop
        for(var i = 0; i <= 10; i++){
            for(var x = 0; x <= i; x++){
                document.write(x);
            }
            document.write("<br/>");
        }
        
        //While Loop
        i = 0;
        x = 0;
        document.write("<br/>");
        while (i < 10) {
            document.write(i);
            i++;
        }
        
        //Do While Loop
        i = 0;
        x = 0;
        document.write("<br/><br/>");
        do {
            x = i * i; 
            document.write(x);
            document.write("<br/>");
            i++;
        }
        while(x < 100);
