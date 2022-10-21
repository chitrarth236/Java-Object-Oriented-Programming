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
- **size** : int size();
- **emptyness check** : boolean isEmpty(); 
- **value contain check** : boolean contains(t);
- **get Index of value** : int indexOf(t);
- **Sorting** :
    Collections.sort(list, (a, b) -> a - b); // asc
    
    Collections.sort(list, (a, b) -> b - a); // desc
- **non premitive to premitive list** : toArray();
    

#### Queue
- **Define** : Queue<T> queue = new ArrayDeque<>();
- **Define** : Queue<T> queue = new LinkedList<>();
- **Define** : Queue<T> queue = new PriorityQueue<>();
- **insert** : boolean offer() / add();
- **remove** : T poll() / T remove();
- **size** : int size(); 
- **peak at head element** : T peek();
- **emptyness check** : boolean isEmpty(); 

#### Stack
- **Define** : Stack<T> stack = new Stack<>();
- **Define** : Deque<> stack = new ArrayDeque<>(); // better approach
- **insert** : boolean push();
- **remove** : T pop();
- **size** : int size(); 
- **peak at head element** : T peek();
- **emptyness check** : boolean isEmpty(); 

#### HashMap
- **Define** : HashMap<K, V> hashMap = new HashMap<>();
- **insert** : V put(k, v);
- **get** : V get(k);
- **remove** : V remove(k);
- **size** : int size(); 
- **contains** : boolean containsKey(k); 
- **clear all** : void clear();
- **emptyness check** : boolean isEmpty(); 

#### Set
- **Define** : Set set = new HashSet<>();
- **insert** : boolean add(Object O);
- **delete** : boolean remove(Object O);
- **clear all** : void clear();
- **size** : int size();
- **emptyness check** : boolean isEmpty(); 
- **value contain check** : boolean contains(t);

#### String

#### Array
