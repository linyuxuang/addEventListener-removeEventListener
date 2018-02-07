# js_addEventListener-removeEventListener
js_addEventListener与removeEventListener用于处理指定和删除事件处理程序操作



      addEventListener和removeEventListener 用于处理指定和删除事件的操作
		  所有的DOM节点都包含这两个方法，
      
        并且他们都接受3个参数：
        
         参数1：要处理的事件名
         参数2：作为事件处理的函数名
         参数3：布尔值，如果是true：表示在捕获阶段调用事件处理程序，
                                   如果是false：表示在冒泡阶段调用事件处理程序



     例子（这样做是无效的）
     
      
         	<input type="button" name="" id="btn1" value="click888"/>

		    	var btn =document.getElementById("btn1");
	        	btn.addEventListener("click",function(){
		        	alert(this.value);
      		  },false)
	        	
	       btn.removeEventListener("click",function(){
	       				alert(this.value);
	        },false)
	       
	       

   （这样做才是有效的）
   
       
       
          var btn =document.getElementById("btn1");
		    	   function handler(){
		    	  	alert(this.id);
		    	  }
	        btn.addEventListener("click",handler,false)
	        	
	        btn.removeEventListener("click",handler,false)











