from assign4_stack import ArrayStack


def findRightFirstLargeNum(l):
    """ find the first large Num and record the index
    >>> findRightFirstLargeNum([2,6,0,1,7,3,5,8,4,9])
    [1,4,3,4,7,6,7,9,9,-1]
    """ 
    outlist = []

    stack = ArrayStack()
    # stack.push()

    for index in range(len(l)):
        print(stack)
        print(outlist)
        outlist.append(-1)
        current_value = l[index]
        while not stack.is_empty():
            stacktop = stack.peek()
            stacktop_value = tuple(stacktop.keys())[0]
            if stacktop_value < current_value:
                data_index = stacktop[stacktop_value]
                outlist[data_index] = index
                stack.pop()
            else:
                break
        if not stack.is_empty():
            stacktop = stack.peek()
            stacktop_value = tuple(stacktop.keys())[0]
            if stacktop_value > current_value:
                stack.push({current_value:index})
                # data_index = stacktop[stacktop_value]
        else:
            stack.push({current_value:index})
        
    return outlist
