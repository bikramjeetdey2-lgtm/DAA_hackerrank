Roads and Libraries

Determine the minimum cost to provide library access to all citizens of HackerLand.

There are n cities, numbered from 1 to n. Initially, there are no libraries and the cities are not connected.

You can:

Build a library in any city at cost c_lib.

Build a bidirectional road between two cities at cost c_road.

A citizen can access a library if:

Their city contains a library, or

They can travel by roads to another city that has a library.

You are given a list of cities that can be connected by roads.

Your task is to find the minimum cost required to ensure every citizen has access to a library.

Function Description

Complete the function:

roadsAndLibraries(int n, int c_lib, int c_road, int[][] cities)
Parameters

n : number of cities

c_lib : cost of building a library

c_road : cost of building a road

cities : list of pairs [u, v] representing roads that can be built between cities

Returns

long : the minimum cost required

Input Format

The first line contains an integer q, the number of queries.

For each query:

The first line contains four integers

n m c_lib c_road

where:

n = number of cities

m = number of possible roads

c_lib = library cost

c_road = road cost

Each of the next m lines contains two integers:

u v

representing a bidirectional road between cities u and v.

Constraints

1 ≤ q ≤ 10

1 ≤ n ≤ 10^5

0 ≤ m ≤ min(10^5 , n(n−1)/2)

1 ≤ c_lib , c_road ≤ 10^5

1 ≤ u , v ≤ n

Each road connects two different cities

Sample Input
2
3 3 2 1
1 2
3 1
2 3
6 6 2 5
1 3
3 4
2 4
1 2
2 3
5 6
Sample Output
4
12
Explanation
Query 1

Build 1 library in city 1 → cost = 2

Build roads:

1–2 → cost = 1

2–3 → cost = 1

Total cost = 2 + 1 + 1 = 4

Query 2

Here library cost < road cost, so it is cheaper to build a library in every city.

Total cost = 6 × 2 = 12
