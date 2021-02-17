# Huffman Encoding

### What is huffman encoding? 

Huffman encoding is developed by David A. Huffman in 1951 that is used for lossless data compression. The base idea is to variable length codes to the input variables, length of the assigned codes are based on the frequencies of the corresponding characters. Highest showing character will get the smallest/shortest code while least frequent characters will get longer/larger code. 

#### Algorithm 

Main parts in writing huffman encoding:
1. Preprocess the input variable to find unique characters along with their frequncy count.
2. Create a huffman tree based on the input variables
3. Traverse through the tree and assign codes to the individual character from the input variables 

We can obtain unique characters and their respective count for a string by using hashmap/dictionary, once the preprocessing step is completed we will do the following to build a huffman tree. <br />

First we create a leaf node for each and every characters in the dictionary, next we sort the node list to make sure the least frequent characters is always at root. <br />

Take the top two root nodes from node list, then we will combine the two nodes into an internal node where its frequency is the sum of the two nodes, first node will be assign as left child and second will be the right child (Smaller frequency will be assigned to the left and larger for the right), we will also assign the code for all nodes 0 for left child and 1 for right child. <br />

Next, we will add the new internal node back to node list, and we will repeat the above steps until the list only contains one node. <br />

Once the tree is created we can get the codes for each character by tracersing through the huffman tree.

In our test, we will use the example used in wikipedia.

You can check out the code in [action](https://github.com/MingSheng92/HuffmanEncoding/blob/main/HuffmanEncoding.ipynb).

### Future works

Now that we know how huffman encoding works, it will be interesting it we can try to apply this algorithm to more complex problems, eg. encode a black and white image with huffman encoding.

### Reference & reading materials
1. [Huffman coding, Wikipedia](https://en.wikipedia.org/wiki/Huffman_coding)
2. [Huffman coding](http://homes.sice.indiana.edu/yye/lab/teaching/spring2014-C343/huffman.php)
