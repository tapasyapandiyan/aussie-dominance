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
    
    
    
## experiment 3: bowling average checker
just a quick tool to calculate a bowler's average for a series or match. lower averages mean they are taking wickets cheaply, which is the key to australian dominance.

```python
# simple math script to get the bowling average
# formula: runs allowed / total wickets taken

runs_given = 124
wickets_taken = 6

print("--- series bowling stats ---")
print("runs conceded:")
print(runs_given)
print("wickets taken:")
print(wickets_taken)

# simple check to avoid dividing by zero if a bowler didn't get a wicket
if wickets_taken == 0:
    print("bowling average: n/a (no wickets taken yet)")
else:
    bowling_avg = runs_given / wickets_taken
    final_avg = round(bowling_avg, 2)
    print("calculated average:")
    print(final_avg)
    
    # basic student thresholds for performance
    if final_avg <= 22.0:
        print("verdict: absolute peak glenn mcgrath tier.")
    if final_avg > 22.0 and final_avg <= 30.0:
        print("verdict: solid performance. doing a great job for the team.")
    if final_avg > 30.0:
        print("verdict: a bit expensive. need to work on line and length.")
        

## experiment 4: era comparison script (2000s vs modern era)
wanted to write a script to compare the legendary 2000s team under steve waugh/ricky ponting with the current team led by pat cummins. it tracks world cups, test championship maces, and ashes wins.

```python
# comparing the two greatest eras of australian cricket
# high school sports stats project

# data structure for the 2000s golden team
era_2000s = {
    "captain": "waugh and ponting",
    "odi_world_cups": 3,
    "wtc_maces": 0, # wtc didnt exist back then
    "ashes_series_won": 4
}

# data structure for the current modern team
era_modern = {
    "captain": "pat cummins",
    "odi_world_cups": 1,
    "wtc_maces": 1,
    "ashes_series_won": 2 # retained/won counts
}

print("--- ERA COMPARISON LAB ---")

print("checking stats for the 2000s era:")
print("captains:")
print(era_2000s["captain"])
print("odi world cups won:")
print(era_2000s["odi_world_cups"])

print("\nchecking stats for the modern era:")
print("captain:")
print(era_modern["captain"])
print("world test championship maces:")
print(era_modern["wtc_maces"])

print("\n--- final logical breakdown ---")

# messy human comparison logic based on trophies
if era_2000s["odi_world_cups"] > era_modern["odi_world_cups"]:
    print("odi summary: the 2000s team dominates the limited overs format with the hat-trick of world cups.")

if era_modern["wtc_maces"] > era_2000s["wtc_maces"]:
    print("test summary: cummins era secured the official world test championship mace which makes them global test kings.")

print("\nverdict: both eras are insane. 2000s was pure raw intimidation, but the cummins era wins everything across all formats under crazy pressure.")