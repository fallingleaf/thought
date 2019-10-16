# Priority Queue

**Definition**

- Priority queue is data structure that process data based on its priority
- One popular implementation of priority queue is heap with runtime complexity
is O(nlogn).

**Usage**

- Find top K maximum values: use min heap of size K to store elements, when heap
size goes over K+1, pop the smallest element from heap to maintain its size,
e.g K frequent elements problems

- Meeting room problem: can re-use the room if start time > end time,
use priority queue to store end time of meetings to find earliest end time.

- Find median value in stream: maintain the middle value from stream by using 2
heaps, max heap for first half and min heap for second half. Median value can be
calculated by taking top value from each heap.

- Hire K workers: worker has wage and quality, we want to minimize wage while maintain
wage ratio based on quality. Sort list on wage/quality, use max heap to remove
higher quality when there're more than K workers.

- Min max distance to gas station: add K gas stations to current street to minimize
distance between gas stations, we could use max heap to store distance, adding one
more station in between reduce distance by half, adding 2 stations reduce distance by 3
 and so on.

- Cheapest flights within K stop: use min heap to store price, city and number of stop
each time pop the cheapest from heap, find next flights it can reach and increase price, stop
