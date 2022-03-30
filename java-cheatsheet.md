### Copy arrays:

int[] src  = new int[]{1,2,3,4,5};

int[] dest = new int[5];

System.arraycopy( src, 0, dest, 0, src.length );

src - the source array.
srcPos - starting position in the source array.
dest - the destination array.
destPos - starting position in the destination data.
length - the number of array elements to be copied.


Or simply 

int[] src = ...
int[] dest = src.clone();

### SORTING
Arrays.sort(arr, optionallambda);

### List<Integer> to int[]
  
 cannot do list.toArray() -> because Integer is not int[]
 
  use int[] example1 = list.stream().mapToInt(i->i).toArray();

  
  ### Array to List
  
 Arrays.asList(arr) turns array type to list type. It creates a list wrapper on the array, changing the list will change the underlying array (arr) as well.
  
  new ArrayList<Integer>(Arrays.asList(ia)) Arrays.aslist is used to create the list wrapper os list can be pass as constructor to creates new ArrayList.
 The structure of this new ArrayList is completely independent of the original array. It contains the same elements (both the original array and this new ArrayList reference the same integers in memory), but it creates a new, internal array, that holds the references.

  
  
