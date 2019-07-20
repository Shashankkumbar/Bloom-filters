# Bloom Filters and its applications
## Problem Statement
What is the fastest and space efficient way
to search for a word that is present or not?

* HashTable?
* Tries?
Above two data structure optimised in time complexity but comprimise in space.
To overcome all these problems and to do it effective time and space we use Bloom filters

## Introduction 
A Bloom filter is a space-efficient probabilistic data
structure, that is used to test whether an element
is a member of a set.
Bloom filter options
➢ Insert
➢ Search

### Insertion
* An empty Bloom filter is a bit array of m bits, all set to 0. There
must also be k different hash functions defined, each of which
maps or hashes some set element to one of the m array
positions, generating a uniform random distribution.
* To add an element, feed it to each of the k hash functions to get
k array positions. Set the bits at all these positions to 1.

### Search
* To search an element, feed it to each of the k hash functions to get k
array positions
* If any of the bits at these positions is 0, the element is definitely not in
the set – if it were, then all the bits would have been set to 1 when it
was inserted
* If all are 1, then either the element is in the set, or the bits have by
chance been set to 1 during the insertion of other elements, resulting
in a false positive.
## Delete in Bloom filters
Deleting elements from filter is not possible because, if
we delete a single element by clearing bits at indices
generated by k hash functions, it might cause deletion
of few other elements.
Bloom filters do not permit deletion of items

## Application of Bloom filters
### 1.Password :
Whenever you are trying to set password for something , it should be strong
enough and be harder to guess.Here we are doing a small approach using
bloom filters which avoid users keeping easy passwords.
### 2.Intersection :
When you are given two huge sets of data and is asked to find the common
data between them. We can easily find them using Bloom filters.
