Lamba Expression / Method Refereces / Streams
===

### Method references
All other types of method refereces are obvious, but 
unbound non-static method refereces:
ArrayList<Integer>::add  -> add operation works with an object, but ArrayList is a class, so which object will it applied to.

This is equivalent to the lambda ->
(ArrayList a, int i) -> { a.add(i) }
so this can be assigned to 
`BiConsumer<ArrayList<Integer>, Integer> c = ArrayList<Integer>::add

### Streams.collect(supplier, accumulator, combiner)
supplier -> fn creating new result container
accumulator -> fn to create add elements to result container
combiner -> fn to combine 2 result container, used when || streams are used

### Parallel operations in streams
All || operations in streams use ForkJoinPool.commonPool(),
This default commonPool can be changed to a specific pool for a task.

Criticism
http://www.coopsoft.com/ar/CalamityArticle.html


