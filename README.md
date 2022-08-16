# sort
<!DOCTYPE html>
<html>
<body>


<input type="number" id="demo">
<button  onclick ="addelement()" > +</button>
<p id="numbers"></p>
<button   onclick ="calculer()" > calculer </button>
<p id="min"></p>
<p id="max"></p>
<p id="sum"></p>
<script>
 let tab=[];
 let nb=0;
 function addelement()
 {
 console.log("test");
   	document.getElementById('numbers').innerHTML+=" "+   					document.getElementById('demo').value ;
   	tab[nb]=parseInt(document.getElementById('demo').value);
   	nb++;
 }

 function calculer()
 {
 	let s=0;
	let min=0;
 	let max=0;
 	for ( let i=0;i<nb;i++)
    { 
    	s=s+tab[i] ;
    } 
   
 	for ( let i=0;i<nb-1;i++)
 	{
      for ( let j=i+1;j<nb;j++)
      {
      	if (tab[i]<tab[j])
        {
           let temp=tab[i];
           tab[i]=tab[j];
           tab[j]=temp;
         }
      }
   } 
 document.getElementById('min').innerHTML="min : " + tab[0];
   document.getElementById('max').innerHTML="max : "+tab[nb-1];
   document.getElementById('sum').innerHTML="somme : "+s;
   
 }

</script>


</body>
</html>

