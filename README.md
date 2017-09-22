# differAarray
  
#copy paste in html and run or download differAarray.html

<h2>Diff Two Arrays</h2>

<p>Compare two arrays and return a new array with any items only found in one of the two given arrays, but not both. In other words, return the symmetric difference of the two arrays.</p>

<p>
<ul>
<li>diffArray(["diorite", "andesite", "grass", "dirt", "pink wool", "dead shrub"], ["diorite", "andesite", "grass", "dirt", "dead shrub"]);</li>
<li>diffArray([1, 2, 3, 5], [1, 2, 3, 4, 5]) should return an array.</li>
<li>["diorite", "andesite", "grass", "dirt", "pink wool", "dead shrub"], ["diorite", "andesite", "grass", "dirt", "dead shrub"] should return ["pink wool"].</li>
<li>["andesite", "grass", "dirt", "pink wool", "dead shrub"], ["diorite", "andesite", "grass", "dirt", "dead shrub"] should return ["diorite", "pink wool"].</li>
<li>["andesite", "grass", "dirt", "dead shrub"], ["andesite", "grass", "dirt", "dead shrub"] should return [].</li>
<li>[1, 2, 3, 5], [1, 2, 3, 4, 5] should return [4].</li>
<li>[1, "calf", 3, "piglet"], [1, "calf", 3, 4] should return ["piglet", 4].</li>
<li>[], ["snuffleupagus", "cookie monster", "elmo"] should return ["snuffleupagus", "cookie monster", "elmo"].</li>
<li>[1, "calf", 3, "piglet"], [7, "filly"] should return [1, "calf", 3, "piglet", 7, "filly"].</li>

</ul>
</p><br/>
<p>======================================================</p>
  
function diffArray(arr1, arr2) {
  var newArr = [];
  // Same, same; but different.
  newArr= arr1.concat(arr2);
  var diffarray= newArr.filter(function(x){
    
    if(arr1.indexOf(x)<0 || arr2.indexOf(x)<0)
      {
        return x;
      }
    
  });
  
  return diffarray;
}  
diffArray(arr1, arr2);  