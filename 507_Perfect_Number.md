## 507. Perfect Number

class Solution:
    def checkPerfectNumber(self, num: int) -> bool:
        if num==1: return False
        val = 1
        i = 2
        while i**2 < num:
            if num%i==0: val+=i+num//i
            i+=1
        if i*i==num: val+=i
        return val==num
