# Ejercicios 2019/05/29 - II

## Merge Sort
```javascript
function mergeSortHelper (arr1, arr2) {
  let result = [];
  let indexL1 = 0;
  let indexL2 = 0;

  while (indexL1 < arr1.length && indexL2 < arr2.length) {
    if (arr1[indexL1] < arr2[indexL2]) {
      result.push(arr1[indexL1]);
      indexL1++;
    }else {
      result.push(arr2[indexL2]);
      indexL2++;
    }
  }

  return result.concat(arr1.slice(indexL1)).concat(arr2.slice(indexL2));
}

function mergeSort(arr){
  if(arr.length === 1 || arr.length === 0) return arr;

  let list1 = arr.splice(0, Math.floor(arr.length / 2));
  let list2 = arr.splice(0, arr.length);

  return mergeSortHelper(mergeSort(list1), mergeSort(list2)); 
}
```


## Ejercicio de la Fila y los sobornos
```javascript





```
