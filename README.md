# TreeMap in Java

This is a simple demonstration of using the `TreeMap` class in Java to store key-value pairs, modify them, and perform basic operations like replacing and removing entries.

## What is a TreeMap?

A `TreeMap` is a part of the `java.util` package and implements the `Map` interface. It is a NavigableMap that stores key-value pairs in a sorted order based on the natural ordering of its keys or by a comparator provided at the time of creation.

### Key Features of TreeMap:
- **Sorted Order**: Unlike `HashMap`, which does not maintain any order, `TreeMap` stores its keys in a sorted order. The default sorting is ascending, based on the natural order of the keys (for strings, it’s lexicographical order).
- **Key-Value Pair**: Each element in a `TreeMap` is a key-value pair, where keys must be unique, but values can be duplicated.
- **Efficient Operations**: The basic operations like `get`, `put`, `replace`, and `remove` are performed in logarithmic time, O(log n), due to the underlying Red-Black Tree structure.
- **Navigable**: `TreeMap` provides additional methods like `firstKey()`, `lastKey()`, and `ceilingKey()` to efficiently navigate through the map.

## Code Explanation

In the provided Java code, we perform several operations on a `TreeMap` object named `values`:

1. **Creating the TreeMap**:
   - A new `TreeMap` is initialized where the key type is `String` and the value type is `Integer`.

2. **Adding Entries**:
   - The `put()` method is used to add key-value pairs to the `TreeMap`. We add `"Second"` with value `2` and `"First"` with value `1`.

3. **Printing the TreeMap**:
   - The contents of the `TreeMap` are printed. Since `TreeMap` automatically sorts the keys, the output will show the key-value pairs in ascending order of the keys (i.e., `"First"` before `"Second"`).

4. **Replacing Values**:
   - The `replace()` method is used to modify the values associated with existing keys. We replace the value of `"First"` with `11` and `"Second"` with `22`.

5. **Printing the Updated TreeMap**:
   - The updated `TreeMap` is printed after the values have been replaced.

6. **Removing an Entry**:
   - The `remove()` method is used to remove the entry associated with the key `"First"`. The method returns the value associated with the removed key, which is printed.

### Code
```Java
import java.util.Map;
import java.util.TreeMap;

public class TreeMapDemo {
    public static void main(String[] args) {

        Map<String, Integer> values = new TreeMap<>();
        values.put("Second",2);
        values.put("First", 1);
        System.out.println("Map using TreeMap: " + values);
        values.replace("First", 11);
        values.replace("Second", 22);
        System.out.println("New Map:" + values);
        int removedValue = values.remove("First");
        System.out.println("Removed value:" + removedValue);
    }
}
```
### Output
```
Map using TreeMap: {First=1, Second=2}
New Map:{First=11, Second=22}
Removed value:11
```

As shown in the output:
- The `Map using TreeMap: {First=1, Second=2}` shows the original map, where the keys are sorted in ascending order (`"First"` before `"Second"`).
- The `New Map:{First=11, Second=22}` shows the map after the values associated with `"First"` and `"Second"` have been replaced.
- The `Removed value: 11` indicates that the value associated with the key `"First"` was removed, and the value `11` was returned.

## Key Methods in TreeMap:

- **put(K key, V value)**: Adds the specified key-value pair to the map. If the key already exists, the value is updated.
- **replace(K key, V value)**: Replaces the value associated with the specified key if the key exists.
- **remove(Object key)**: Removes the key-value pair associated with the specified key and returns the value.
- **get(Object key)**: Retrieves the value associated with the specified key.
- **keySet()**: Returns a `Set` of all the keys in the map.
- **values()**: Returns a collection of all the values in the map.
- **entrySet()**: Returns a `Set` of all the key-value pairs (entries) in the map.
- **firstKey()**: Returns the first (lowest) key in the map.
- **lastKey()**: Returns the last (highest) key in the map.
- **ceilingKey(K key)**: Returns the least key greater than or equal to the specified key.

## Conclusion

`TreeMap` is an efficient and versatile map implementation when you need to store key-value pairs in a sorted order. It automatically sorts the keys and provides additional methods for navigation. This makes it useful for scenarios where order matters and you need efficient searching, insertion, and removal.

Feel free to modify the code and experiment with different TreeMap operations, such as navigating through the keys or checking if a key exists!


