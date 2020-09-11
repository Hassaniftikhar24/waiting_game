Task: Make a waiting game which gives the user a target time of 4.00 seconds to exit
Input: Using "ENTER" as the input
Output: Displays the elapsed time and shows if the user was slow/fast
Method: Creating a function to build this program

import time
def waiting_game():
    print("Your target time is 4.00 seconds ")
    x = input("Press enter to begin: ")
    if x == "":
        start_time: float = time.time() # Starting the game as soon as the user presses the enter
    y = input("Press enter again after 4.00 seconds: ")
    elapsed_time = 0 # Initializing elapsed_time
    if y == "":
        elapsed_time = time.time()-start_time # Calculating elapsed time
        print("Elapsed time is: ", elapsed_time)
    target_time = 4.00
    if elapsed_time == target_time: # Check for the perfect timing
        print("Hurrah, you are perfect on time \n")
    elif elapsed_time > target_time: # Check for being too slow
        time_difference = elapsed_time - target_time
        print(time_difference, "seconds too slow")
    else: # check for too fast
        diff_time = target_time-elapsed_time
        print(diff_time, "seconds too fast")
waiting_game()

