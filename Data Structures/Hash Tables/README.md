##Hash Tables

A hash table is a data structure for storing key-value pairs. Unlike basic arrays, which use index numbers for accessing elements, a hash table uses keys to look up table entries. Thus, it is a data structure in which insertion and search operations are very fast irrespective of the size of the data.

####Hashing
Hashing is a technique to convert a range of keys into a range of table entries. The hash function decides where to store and retrieve items in a hash table. It takes in an item key as its parameter and returns and table location for that particular item. Generally, a hash function uses modulo arithmetic. 

####Collisions
Occasionally, different keys will generate the same hash function result. When two keys hash to the same index, we get a hash collision. To maximize the efficiency of storing and retrieving items in the hash table, we need to minimize the number of collisions.

If faced with a collision situation, the different methodologies are as follows:

* Linear Probing:    traversal through the table going by one element at a time until the next available spot is found.

* Quadratic Probing: traversal through the table always moving n^2 spots from the point of collision, where n is the number of attempts to 
                     resolve the collision.

* Chaining:          elements of the same hash key will be chained together using a linked list of all the elements with the same hash key.

* Double Hashing:    apply a second hash function to the key when a collision occurs. The result of the second hash function will be the 
                     number of positions from the point of collision to insert.

* Rehashing:         Once the hash table gets too full, the run time for operations will increase. To avoid this problem, a table at least                      twice the size of the original will be built and the elements will be transferred to the new table.

####C++ Implementation (unordered_map in STL)

```C++
int main()
{
    // Declaring umap to be of <string, double> type
    // key will be of string type and mapped value will
    // be of double type
    unordered_map<string, double> umap;
 
    // inserting values by using [] operator
    umap["PI"] = 3.14;
    umap["root2"] = 1.414;
    umap["root3"] = 1.732;
    umap["log10"] = 2.302;
    umap["loge"] = 1.0;
 
    // inserting value by insert function
    umap.insert(make_pair("e", 2.718));
 
    string key = "PI";
 
    // If key not found in map iterator to end is returned
    if (umap.find(key) == umap.end())
        cout << key << " not found\n\n";
 
    // If key found then iterator to that key is returned
    else
        cout << "Found " << key << "\n\n";
 
    key = "lambda";
    if (umap.find(key) == umap.end())
        cout << key << " not found\n";
    else
        cout << "Found " << key << endl;
 
    //  iterating over all value of umap
    unordered_map<string, double>:: iterator itr;
    cout << "\nAll Elements : \n";
    for (itr = umap.begin(); itr != umap.end(); itr++)
    {
        // itr works as a pointer to pair<string, double>
        // type itr->first stores the key part  and
        // itr->second stroes the value part
        cout << itr->first << "  " << itr->second << endl;
     }
}
```
