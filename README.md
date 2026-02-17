# Python-class-to-convert-an-integer-to-a-roman-numeral.
class RomanSolution:
    @staticmethod
    def int_to_Roman(num):
        if num < 1 or num > 3999:
            return "ENTER A GOOD VALUE!"
        
        val = [
            1000, 900, 500, 400,
            100, 90, 50, 40,
            10, 9, 5, 4,
            1
        ]
        syb = [
            "M", "CM", "D", "CD",
            "C", "XC", "L", "XL",
            "X", "IX", "V", "IV",
            "I"
        ]
        
        roman_num = ""        
        i = 0
        while num >0:
            while num >= val[i]:
                roman_num += syb[i]
                num -= val[i]
            i += 1
        
        return roman_num
n = int(input("ENTER A NUMBER: "))
print("Roman numeral of given number is:",
      RomanSolution.int_to_Roman(n))

Output
ENTER A NUMBER: 56
Roman numeral of given number is: LVI

