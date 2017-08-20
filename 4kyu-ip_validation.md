# IP Validation

Write an algorithm that will identify valid IPv4 addresses in dot-decimal format. Input to the function is guaranteed to be a single string.

Examples of valid inputs: 1.2.3.4 123.45.67.89

Examples of invalid inputs: 1.2.3 1.2.3.4.5 123.456.78.90 123.045.067.089

"""python
def is_valid_IP(strng):
    elements = strng.split(".")
    #check if there are only 4 values
    if len(elements) != 4:
        return False
    
    for i in elements:
        #check if it has trailing whitespace  & 0s 
        if (len(i) > 1 and i[0] == "0") or (len(i.split(" ")) != 1):
            return False
        #see if element is a string and if its between 0 and 255
        try:
            if int(i) > 255 or int(i) < 0:
                return False     
        except:
            return False
    
    return True
"""
