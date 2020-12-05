# Data_Structures-Hashing-
Abt hashing and tables

# Hashing Table!!!

Def : Hashing is a data structure in which it maps keys to values ! 

DEF(Hash Function) : A function that converts a given big number to a small practical integer value. 
The mapped integer value is used as an index in the hash table.
In simple terms, a hash function maps a big number or string to a small integer that can be used as an index in the hash table. 



#Applications of Hash Table ! 
1) Password Verification. 
2)Login and Logouts for accounts!
3)Linking file name and path together!



#Advantages of hash table !

1)access time of element is average. O(1) 
2)Easy data retrievals. 
3)INsertion/Deletion is also average. O(1)

#Disadvantages of Hashing!!!

1)They accuse collisions , in which we need to perform operations to not to make it happen !
2)Does  not allows null values !
3)They become quite inefficient, if they are more collisions!
4)Space wastage!

#############################################################################################

#Why not list!

1)If list/array is taken, then we can't make them to map its absolute data. Dictionary works in it
2)Dictionary is used for Hashing.

##################################################################################################

#Collisions Handling,

1) Collisions are type, where a value and another value are being mapped to same index. 

Types of Collision handling !
1)  Linear probing.

   *) The  resultant number can be inserted in a stack after performing (key%size) , it provides a result which is resultant number! 
    
    
    
    
    
2)  Double hashing.

    Double hashing is a collision resolving technique in Open Addressed Hash tables. 
    Double hashing uses the idea of applying a second hash function to key when a collision occurs.

          Double hashing can be done using :
          (hash1(key) + i * hash2(key)) % TABLE_SIZE
          Here hash1() and hash2() are hash functions and TABLE_SIZE
          is size of hash table.
          (We repeat by increasing i when collision occurs)

          First hash function is typically hash1(key) = key % TABLE_SIZE

          A popular second hash function is : hash2(key) = PRIME – (key % PRIME) where PRIME is a prime smaller than the TABLE_SIZE.


3)  Random hashing.
4)  Separate chaining.
5)  Quadratic Probing. 
    
    *) Quadratic probing is an open-addressing scheme where we look for i2‘th slot in i’th iteration if the given hash value x collides in the hash table. 
    
   How Quadratic Probing is done? 
   
     Let hash(x) be the slot index computed using the hash function.

     If the slot hash(x) % S is full, then we try (hash(x) + 1*1) % S. 
     If (hash(x) + 1*1) % S is also full, then we try (hash(x) + 2*2) % S.
     If (hash(x) + 2*2) % S is also full, then we try (hash(x) + 3*3) % S.
     This process is repeated for all the values of i until an empty slot is found.
