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

