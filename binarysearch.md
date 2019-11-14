## Binary search
- Binary search is searching technique used for sorted array

1. Search exact match:
- Check if mid = key then return result
- Otherwise, increase left = mid + 1 or decrease right = mid - 1

2. Search for upper bound:
- Search for a point k where array split into [a1...ak-1] and [ak...an] where
a(k) will be greater than or equal key
- check if mid > target, right = mid - 1, otherwise left = mid,
because left set to mid, it can create infinite loop, calculate mid = (left + right + 1) / 2
to avoid this, return left

3. Search for lower bound (or insertion position)
- Search for point where all left side [a1...ak-1] < target, [ak...an] >= target
- Check if mid < target, set l = mid + 1, otherwise right = mid, return right

**Usage**
- Find peak element: array may be increasing or deceasing, use binary search,
we can check number at mid and mid + 1, if mid > mid + 1, decreasing slope,
search in left part to mid (because mid maybe a peak), otherwise search in mid + 1
to right

- Search range of element: find range of duplicate sorted array, we can use 2 methods of
search for lower bound and upper bound to find range of element

- Divide chocolate: divide chocolate bar to K bar, find max of sum of min array,
can use binary search (from 1 to sum/K), and check if it can split into K bar
or more, than set left = mid, otherwise right = mid - 1 (search for upper bound,
max sweetness can get by splitting K bar) return left

- Split array largest sum: similar to above problem, but it's to minimize the largest
sum, use binary search (from max value to sum), and check if it can split into M or
less array with sum < mid value, then set right = mid, otherwise set left = mid + 1,
(search for lower bound, min sum can get by splitting M) return right
