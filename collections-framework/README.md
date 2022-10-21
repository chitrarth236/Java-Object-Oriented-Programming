### Collection vs Collections
Collection is an Interface, which helps to represent group of object as a single entity.

Collections is a class which has some utility methods for collection objects.


#### ArrayList
- **Define** : ArrayList<T> list = new ArrayList<>();
- **insert** : boolean add(t)
- **insert** at index : add(int index, T)
- **update** index value : T set(int index, T);
- **delete** : T remove(int index);
- **clear all** : void clear();
- **get element at index** : T get(int index);
- **size** : int list.size();
- **emptyness check** : boolean isEmpty(); 
- **value contain check** : boolean contains(t);
- **get Index of value** : int indexOf(t);
- **Sorting** :
    Collections.sort(list, (a, b) -> a - b); // asc
    Collections.sort(list, (a, b) -> b - a); // desc
- **non premitive to premitive list** : toArray();
