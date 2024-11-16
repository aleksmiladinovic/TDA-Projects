# Topological text analysis - similarity of movie descriptions

**TDA** in **text analysis** is a relatively new branch with some promissing results. In this notebook, we demonstrate one of it's methods.

Given a file containing the titles and descriptions of various films we want to find the ones most similar to the description of the movie *"Harry Potter and the Philosopher's Stone"*.

The main idea of **TDA** is to represent a given dataset as a set of points. These points are then subject to the **Vietoris-Rips filtration** (or other..) based on which we can compute the **presistence classes** of the filtration. These classes serve as to extract **topological information** of the given dataset. That being said, the biggest chalenge of **TDA** in text analysis would be how to obtain points i.e. numerical values from text. For this purpose, we will use the **TfIdf** method. Each movie description will be partitioned into blocks. The set of points represented by the given description is then obtained from the **TfIdf** values of these blocks.  
From there on we proceed the following way: we calculate the **persistence classes** of each set of points. By using the **bottleneck distance** of **persistence diagrams** we can find which movies produce diagrams closest to the diagram of the description of *"Harry Potter and the Philosopher's Stone"*.
