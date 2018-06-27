# Edmond-S-MST-Python

## Goal:
This project deals with the segmentation of  sentences into parts using syntactic analysis:
The setences are in the form of directed , weighted graphs stored in graphml format.Each node represents a word having the following  attributes : 
- chunk number 
- morph
- lemma 
- position id 
- starting index
- length of the word.
Words having the same chunk number represent sandhi which occur prominently in the phonology of Indian languages. 
A Sandhi is a cover term for a wide variety of phonological processes that occur at morpheme or word boundaries.
A sandhi can be identified from a list of nodes having the same chunk number whose starting or ending indices overlap with the one another,among which only one node has to be selected.
The Steiner tree algorithm aims at spanning only those set of selected nodes and forming a maximum spanning subtree using its adjacent edges.
Edmond's Chu Liu Algorithm spans the entire set of nodes in the graph to form a maximum spanning arborescence.

## Input: 
- `MST.py` finds out both minimum and  maximum spanning arborescence
- `Steiner_Tree.py` forms a maximum spannning arborescence of the subgraph on user choice:

 ```
 os.chdir('<pathname>')   #Add the pathname
 ch=input('Enter your choice:\n0->Maximum Spanning Arborescence\n1->Maximum Spanning Subtree using an Ad hoc method')  
 G=nx.read_graphml(x)   #reading a graph in graphml file from the path x
 G=weighted_graph(G)
 if(ch==0):
     smst(G,x)  #finds a maximum spanning arborescence
 elif(ch==1):
     submax(G,x)  #finds a maximum spanning subtree using an ad hoc method
 ```
 
 ## Sample Input:
 - A sample graphml file has been provided as `Sample Input`
 - A folder named `graph` contains a list of 53,984 graghs in graphml format
 
 
 
