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
