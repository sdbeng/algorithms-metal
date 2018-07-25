# algorithms-metal

## Resources
https://repl.it/@UCBXBootcamp/StrictBestBrains

https://visualgo.net/

## code

### direct graph problem - check png ex. description
```
var graph = [
  // define 1
  [1, 2],    
  [1, 3],
  [1, 4],
  
  // define 2
  [2, 5],
  
  // define 3
  [3, 6],
  
  // define 4
  [4, 3],
  [4, 6],
  
  // define 5
  [5, 6],
  
  // define 6 
  
];



var graph = {
  // define 1
  1: [2, 3, 4],
  
  // define 2
  2: [5],
  
  // define 3
  3: [6],
  
  // define 4
  4: [3, 6],
  
  // define 5
  5: [6],
  
  // define 6 
  6: [],
 
};

/*  add a vertex with name */
function addVertex (name) {
  graph[name] = [];
}

/*  Make edge from a -> b */
function addEdge (a, b) {
  checkForPath(a, b);
  graph[a].push(b);
}

function checkForPath(a, b) {
  // Any way to from B back to A
}

addVertex(7);
addEdge(6, 7);
addEdge(7, 1); // THIS WILL BE A CYCLE
```
## selection sorting
```function selectionSort(items) {

  // Everything to the left of this index is sorted
  var sortedIndex = 0;
  
  while (sortedIndex < items.length) {
  
    // Step 1: Find minimum
    var minimumItem = items[sortedIndex];
    var minimumIndex = sortedIndex;
    
    // When finding minimum, only consider items to the right of sortedIndex
    for (var i = sortedIndex; i < items.length; i++) {
      if (items[i] < minimumItem) {
        minimumIndex = i;
        minimumItem = items[i];
      }
    }
    
    // Step 2: Swap minimum with leftmost of the items we are considering
    swap(items, sortedIndex, minimumIndex);
    
    // Now, go back to Step 1, except considering one fewer item
    sortedIndex++;    
  }
  
  return items;
}
```
## foo
