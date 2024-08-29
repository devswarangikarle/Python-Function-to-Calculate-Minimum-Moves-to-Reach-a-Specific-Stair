# Python-Function-to-Calculate-Minimum-Moves-to-Reach-a-Specific-Stair

This repository contains a Python function, min_moves_to_reach_stair, which calculates the minimum number of moves required for a character to reach a specific stair number from the starting point (stair 0). The character can either take a larger step of size Y or a smaller step of size 1 in each move.
Features:
Input: The function takes multiple test cases, where each test case consists of two integers X and Y:
X is the target stair number.
Y is the number of stairs the character can climb in one move.
Output: For each test case, the function returns the minimum number of moves required to reach stair X.
Efficient Computation: The solution efficiently calculates the result using integer division and modulus operations.
Example:
For an input of X = 8 and Y = 3, the function will calculate that 4 moves are required (two full 3-step moves and two 1-step moves).

def min_moves_to_reach_stair(T, test_cases):
    results = []
    for i in range(T):
        X, Y = test_cases[i]
        full_steps = X // Y
        remainder_steps = X % Y
        moves = full_steps + remainder_steps
        results.append(moves)
    return results

T = int(input())
test_cases = [tuple(map(int, input().split())) for _ in range(T)]

results = min_moves_to_reach_stair(T, test_cases)
for result in results:
    print(result)
