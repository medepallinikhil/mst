<html>
    <head>
    <title>TicketsBooking</title>
    <script>
    var x;
    var y;
    var z;
    fun=()=>
    {
        var a=prompt("Enter the number of tickets:");
        if(a<6)
        {
            document.getElementById("id").innerHTML="Total amount you need to pay:";
            document.getElementById("id1").innerHTML="Rs."+calculateCost(a);
            document.getElementById("id2").innerHTML="Discount Amount is:Rs."+calculateDiscount(a);
        }
        else
        {
            document.getElementById("id").innerHTML="Sorry! You can book upto 5 tickets only in online!!";
            document.getElementById("id1").innerHTML="";
            document.getElementById("id2").innerHTML="";
        }
    }
    const p=150;
    calculateCost=(a)=>
    {
        var i=1;
        s=0;
        j=0;
        k=0.03;
        if(a>2 && a<6)
        {
            do
            {
                j=p-(p*k);
                s+=j; j=0;
                k+=0.02;
                i+=1
            }
            while(i<=a);
        }
        else if(a<=2)
        {
            s=p*a; 
        }
        else
        {
            s=0;
        }
        return s;
    }
    calculateDiscount=(a)=>
    {
        var g=calculateCost(a);
        var z=a*p;
        return z-g;
    }
    </script>
    </head>
    <body bgcolor="cyan">
        <center><h1><i>ShopTime</i></h1></center>
        <h2 align="center"><i>One stop for all your needs<i></h2>
        <header>
        <nav align="center">
        <h3><a>Home</a> || Login || Register || Wishlist || MyOrders || Help</h3>
        </nav>
            <center>
            </header>
                <h2>Book your tickets now</h2>
                <br>
                <input type="button" value="BOOK TICKETS" onclick="fun()">
                <p id="id"></p>
                <p id="id1"></p>
                <p id="id2"></p>
    </body> 

</html>
