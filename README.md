def find_duplicates(nums):
	seen = set()
	duplicates = set()
	for num in nums:
		if num in seen:
			duplicates.add(num)
		else:
			seen.add(num)
	return list(duplicates)

list = [1, 3, 5, 7, 1, 2, 9, 2, 3]

duplicates = find_duplicates(list)

print("Original list: " + str(list))

print("Duplicate Integers: " + str(duplicates))

Describe the two different ways to figure out all of the duplicate values of a list of integers in english. The first solution is the nested loop solution. The second solution is to use a dictionary or a map (similar to the containsPair method we wrote in class.) Describe both in as much detail as you can (with no code) and describe the trade-offs between the two solutions.

- The two solutions to scanning lists of integers for duplicates are to use Nested Loops and to use Hash Maps. The nested loop solution uses a list called duplicates to hold any additional numbers scanned in. They scan these lists by using two for loops to check through an entered list and return any number that appears more than once in the given list. If they scan a number that is a duplicate, they will then add that integer to the duplicates list, and then the function returns the duplicates list at the end of execution. The Hash Map solution uses a list and a map to increment through the lists and add any numbers to the duplicate list, similar to that of the nested loops. The key difference between these two solutions is that the HashMap solution uses two for loops instead of a nested loop to complete the same task. The first for loop in the HashMap solution specifies the countMap and allocates the numbers entered to it. It also initializes the count to 0. The second for loop looks at the entries on the countMap and checks the map for any duplicate integers. If it finds one, it will add it to list containing the duplicates and then return the list of duplicates once the function is executed fully. In terms of runtime complexity, the HashMap solution is faster because it uses two separate loops instead of a loop inside of a loop like in the Nested Loop solution.   In terms of trade offs, the readability of the Nested Loop is overall easier to comprehend compared to the HashMap, but the runtime complexity of the HashMap makes it run more efficiently than the Nested Loop in exchange for a more complex setup (The readibility may just be an issue for me because we barely talked about HashMaps in 201/202).