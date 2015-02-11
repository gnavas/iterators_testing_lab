##Descriptions of Iterators

###Instructions
Below you will find a list of methods. In the space provided below each, please provide a brief description of what this method does based upon your review of the Docs. 

###Array methods:
May be helpful to look in [Enumerable](http://ruby-doc.org/core-2.2.0/Enumerable.html) as well...

####select:Returns all elements that return true for a given condition. Returns an enumerator (a array like object that can be iterated through). If given a hash then .select returns a hash. 

####reject: Returns all elements that return false for a  given condition. Returns output as an enumerator. 

####map: (".collect") - iterates through a collection of elements and returns the result of the operation given in the block to each element iterated. (e.g. - in block I say num +2 - the new array will return each previous num+2)

####detect:iterates through enum looking for a non-false return. If all cases are false - then returns nil. For example, can check a condition to see if a set of numbers are divisible by 5 & divisible by 7. If no number in the set returns true then the method will return nil. Otherwise the method will return the first element that meets the condition. (e.g. 35 --> if the set of numbers is 1-100)

####inject: (*reduce*) Combines all elements of the enum by the binary operation given. Returns the object - Fore example, if given a set of numbers 1-10 and asked to add 1-10... the method will add 1+2, sum(1+2)_3,(sum of (sum 1+2)+3) +4, etc.

####partition: Iterates through enumerator and returns two arrays. The first array contains all elements that returned true, and the second array contains all elements that did not return true. Example of what .partition returns 
 --> [[elements that returned true],[elements that returned false]]


####sort:Sorts an array based on the condition passed in the block. It will return an array. Synax looks like the following: 
(1..10).sort { |a, b| b <=> a }  #=> [10, 9, 8, 7, 6, 5, 4, 3, 2, 1]
^ As seen above = the block tells the sort method to sort greatest to smallest. 

####one:Returns true or false(Remember the method will take a ? at the end as a result). Checks each element of the collection against the condition provided in the block. If exactly only ONE element returns true across the iteration the method will return true. Otherwise, the method will return false. 

####none: Returns true or false. Checks each element of a collection against the condition provided in a block. If no elements meet the condition (i.e. return true), then the method none will return true. If no block is given - it will still check against all the elements in the collection. 

####all: Returns true or false. Passes each element of a collection to the block. If no elements return false or nil for the given conditiond, then the method will return true. (i.e. All elements meet the condition.)Otherwise, the method will return false. 

####empty?: Returns true or false

.empty? can be used on strings, arrays and hashes and returns true if:
String length == 0
Array length == 0
Hash length == 0

####eql?: Essentially functions as == --> Except for the case of numbers. For exampel 1.eql?1.0 --> returns false. 1==1.0 --> returns true
1eql?1 --> returns true and 1==1 --> returns true

####include?: Returns true or False. Good example provided below. 
Returns true if the given object is present in self (that is, if any object == anObject), false otherwise.

a = [ "a", "b", "c" ]
a.include?("b")   #=> true
a.include?("z")   #=> false

####nil?:Returns true or false. Returns true if the object == nil. Otherwise will return false. 

###Hash methods:

####key?:Returns true or false. Returns true if the given parameter is present in the hash being checked against. 

####keys:
keys --> Will return an array. hash.keys: Will return the keys from the hash in teh form of an array. 

key --> Returns the key of a hash. Pass through a value and it will return the corresponding key. If value is not present then the method will return false. 

####delete: Returns a value, nil, or the value of optional block (Only if the key passed is not present.) Deletes the key_value pair of the given key in the hash. If the key is found, the method will return the value of that key. If the key is not found, the method will return nil or the result of the optional block. 

####delete_if:Returns a hash (minus the delted key_value pairs). Will return an enumerator if no block is given. Enumerates through the array and will delete all key_value pairs that meet the condition(return true) given within the block. 
Note - make sure that you are passing along two parameters to the condition (key,value) --> Make sure the condition that is set is referencing correctly either key or value. 





