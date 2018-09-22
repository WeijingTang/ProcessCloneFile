# ProcessCloneFile
Answer Three Questions below:

Given this information, use Python to:
- Print the clone that occurs in the most samples
- Print the clone with the highest total total_cnt (the sum of all total_cnts with that clone_id)
- Find any cdr3_aa that occurs in more than one clone.  For each of them print the cdr3_aa and how many clones it occurs in.

function clones_mostoccin_samples(f) use hashmap(dictionary), store clone_id as key, the count of the same clone_id as values, then sort the count, return the key(clone_id) map to the largest value(count). 

function cdr3_occ_multi_clone(f) build hashmap, still use clone_id as key, sum total_cnt to the same clone_id as values, sort the total_cnt, return the key(clone_id) map to the largest value(sum total_cnt). 

function cdr3_occ_multi_clone(f) build hashmap, store the sequence(cdr3_aa) as key, the list of the clones(clone_id) the same sequence shows up as value. Then build a new hashmap to store all the sequence(cdr3_aa) that occurs in more than one clone, store the sequence(cdr3_aa) as key, the lenth of each list the sequence(cdr3_aa) map to as value, return the new hashmap.
