__Difficulty__: Easy

class solution():
    def Twosum(self,number_list,target):
        hashtable={}
        for index, element in enumerate(number_list):
            difference = target - element
            if difference in hashtable:
                return [hashtable[difference], index]
            else:
                hashtable[element]= index

number = [2,7,11,15]
target = 9
case_one=solution()
case_one.Twosum(number,target)

# This methods uses hash table to improve the TC to O(n), while brute force method nees O(n^2)
