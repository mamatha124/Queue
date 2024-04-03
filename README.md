# Queue in python
# Get the inputs
n, m = map(int, input().split())
a = list(map(int, input().split()))
# Initialize the bus count and the remaining seats
bus_count = 0
remaining_seats = m
# Loop through the groups
for i in range(n):
    # If the current group is larger than the remaining seats
    if a[i] > remaining_seats:
        # Increase the bus count and reset the remaining seats
        bus_count += 1
        remaining_seats = m
    # Deduct the number of people in the current group from the remaining seats
    remaining_seats -= a[i]
# Check if there are still people left after the loop
if remaining_seats < m:
    # Increase the bus count
    bus_count += 1
# Print the bus count
print(bus_count)
