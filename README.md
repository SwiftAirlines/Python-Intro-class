# Python-Intro-class
For this week student were given an assignment that focuses on various aspects of data processing and manipulation using Python. It covers several key topics, including reading and parsing data from standard input, working with date and time objects, and understanding Entity-Relationship (ER) diagrams in database modeling. The tasks are broken down as follows:

1.Try the code below and revise it to current time. 
Code:

import sys

for line in sys.stdin:

    data = line.strip().split(“\t”)

    if len(data) == 6:

        date, time, store, item, cost, payment = data

        print(“{0}\t{1}”.format(item, cost))

2. Add the timedelta to the datetime and subtract 60 second and added 2 year . (Hit: timedelta(seconds=60))  For each condition, state the code and output

Code: 

from datetime import datetime, timedelta

# Get the current datetime

current_time = datetime.now()

# Add 1 day

one_day_later = current_time + timedelta(days=1)

print(“One day later:”, one_day_later)
# Add 2 years

two_years_later = current_time.replace(year=current_time.year + 2)

print(“Two years later:”, two_years_later)

# Subtract 60 seconds

minus_60_seconds = current_time – timedelta(seconds=60)

print(“Minus 60 seconds:”, minus_60_seconds)

Output:

One day later: 2024-06-25 06:10:41.778503

Two years later: 2026-06-24 06:10:41.778503

Minus 60 seconds: 2024-06-24 06:09:41.778503

3. Create a timedelta object representing 100 days, 10 hours, and 13 minutes.

Code:
from datetime import timedelta

time_delta = timedelta(days=100, hours=10, minutes=13)

print(time_delta)

Output:
100 days, 10:13:00

4. Write a function that takes two arguments (feet and inches) with this time object

Code :
from datetime import datetime

def current_time_with_height(feet, inches):

    datetime_object = datetime.now()

    height = f”{feet} feet {inches} inches”

    return datetime_object, height

# Example usage

feet = 5

inches = 8

datetime_object, height = current_time_with_height(feet, inches)

print(“Current datetime:”, datetime_object)

print(“Height:”, height)

Output:
Current datetime: 2024-06-24 06:13:33.150281

Height: 5 feet 8 inches

