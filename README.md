# aussie-dominance
just tracking some data on how dominant the australian cricket team is across different formats.

## experiment 1: win streak and percentage calculator
wrote a quick loop to calculate win percentages from a raw list of match results because i wanted to see the exact stats.

```python
# rough script to calculate team win percentages
# 1 = win, 0 = loss

# dummy data from a recent match streak
match_results = [1, 1, 0, 1, 1, 1, 0, 1, 1, 1] 

print("--- Aussie Dominance Streak Tracker ---")

total_matches = len(match_results)
wins = 0

# basic loop to count up the wins
for outcome in match_results:
    if outcome == 1:
        wins = wins + 1

# doing the basic math
win_percentage = (wins / total_matches) * 100

print("total games tracked:")
print(total_matches)
print("total wins:")
print(wins)

print("\nfinal win percentage calculated:")
print(win_percentage)

# casual human logic to print a funny comment based on the stat
if win_percentage >= 75:
    print("status: absolute god tier team. unstoppable.")
elif 50 <= win_percentage < 75:
    print("status: pretty decent run but need to fix the middle order.")
else:
    print("status: rare slump. uncharacteristic.")
    
    
    
    
## experiment 2: raw strike rate calculator
wanted to write a quick tool to check a batsman's strike rate during a specific innings to see who is pushing the tempo.

```python
# high school cricket stats project
# calculation: (runs / balls) * 100

runs_scored = 137
balls_faced = 120

print("--- Player Innings Performance ---")
print("runs:")
print(runs_scored)
print("balls faced:")
print(balls_faced)

# basic calculation step
raw_strike_rate = (runs_scored / balls_faced) * 100
final_strike_rate = round(raw_strike_rate, 2)

print("calculated strike rate:")
print(final_strike_rate)

# messy if statement to check the intent of the innings
if final_strike_rate > 120.0:
    print("intent: excellent. playing aggressive cricket.")
if final_strike_rate >= 80.0 and final_strike_rate <= 120.0:
    print("intent: solid anchoring innings. building partnerships.")
if final_strike_rate < 80.0:
    print("intent: too slow for modern limited overs. under pressure.")