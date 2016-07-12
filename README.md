# teste
# Function that receives a multidimensional list and calculates the maximum total
def HellTriangle(triangle):

    prior_line_position = 0
    total_sum = 0

    # Navigating through the lines
    for line in triangle:
    #-----
        greater_position = 0
        greater_value = 0

        # Navigating through positions of the line
        for position in range(len(line)):
        #-----
            # Verify allowed positions
            if position in [prior_line_position, prior_line_position + 1]:
            #-----
                # Verify greater value
                if greater_value <= line[position]:
                #-----
                    greater_position = position
                    greater_value = line[position]
                #-----
            #-----
        #-----
        # Hold the prior line position
        prior_line_position = greater_position

        # Summarize greater values
        total_sum += greater_value
    #-----
    return total_sum
# def - end


# Testing the function
print HellTriangle([[6], [3,5], [9,7,1], [4,6,8,4]])
