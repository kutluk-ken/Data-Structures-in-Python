## Hash Map
Hash maps are efficient key-value stores. They are capable of assigning and retrieving data in the fastest way possible for a data structure. This is because the underlying data structure that they use is an array. A value is stored at an array index determined by plugging the key into a hash function.

In Python we don’t have an array data structure that uses a contiguous block of memory. We are going to simulate an array by creating a list and keeping track of the size of the list with an additional integer variable. This will allow us to design something that resembles a hash map. This is somewhat elaborate for the actual storage of a key-value pair, but it helps to remember that the purpose of this lesson is to gain a deeper understanding of the structure as it is constructed. For real-world use cases in which a key-value store is needed, Python offers a built-in hash table implementation with dictionaries.

* Compression Function
* Defining the Setter
* Defining the Getter
* Creating an Instance
* Handling Collisions in the Setter
* Handling Collisions in the Getter

### Open Addressing
Oen addressing system can help hash map resolve collisions. In open addressing systems, we check the array at the address given by our hashing function. One of three things can happen:

- The address points to an empty cell.
- The cell holds a value for the key we are getting/setting
- The cell holds a value for a different key.

In the first case, this means that the hash map does not have a value for the key and no collision resolution needs to happen. Notice that this does not work if we want to be able to delete keys in our hash map. There are strategies for deleting pairs from a hash map (see Lazy Deletion) but we will not be investigating these.

In the second case, we’ve found the value for our key-value pair!

In the third case, we need to use our collision addressing strategy to find if our key is somewhere else (it may or may not be) so we should recalculate the index of our array.

