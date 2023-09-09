# Codeforces-1527C-Sequence-Pair-Weight
Link: https://codeforces.com/problemset/problem/1527/C
## Logic behind 'mp.put(a[i], mp.getOrDefault(a[i], 0L) + (i + 1));'
```
sample input:
1
11
1 1 1 1 2 3 4 5 1 1 1

sample output:
182

0 1 2 3 4 5 6 7 8 9 10 (indices)
1 1 1 1 2 3 4 5 1 1  1 (elements)

(i+1) refers to the total no. of subarrays ending at i

- Check index 8, mp[1] would be equal to i+1 = 9, which means that
if we encounter '1' again in the sequence, the total no. of subsegments
ending at '1' would be equal to 9

- The previous date from index 8 would only take effect now at index 9

- This is the reason why we update it only after the mp[1] has been
added to the final answer
```
## Helpful Comment
![image](https://github.com/mgalang229/Codeforces-1527C-Sequence-Pair-Weight/assets/51401355/1cca1016-ea63-4796-b987-4891f761aea5)
