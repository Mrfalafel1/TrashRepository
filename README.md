# TrashRepository
       function jsClock(){
            var time = new Date()
            var hour = time.getHours()
            var minute = time.getMinutes()
            //var second = time.getSeconds()
            var temp = ((hour > 12) ? hour - 12 : hour)
            if(hour==0) temp = "12"
               if(temp.length==1) temp = " " + temp
                  temp += ((minute < 10) ? ":0" : ":") + minute
                  //temp += ((second < 10) ? ":0" : ":") + second
                  temp += (hour >= 12) ? " PM" : " AM"
            //document.dateandtime.time.value = temp
            document.getElementById('time').innerHTML = temp;
            id = setTimeout("jsClock()",1000)
         }
