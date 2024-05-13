def next_day(day, month, year):
    days_in_month = [31, 28 + (year % 4 == 0 and (year % 100 != 0 or year % 400 == 0)), 31, 30, 31, 30, 31, 31, 30, 31, 30, 31]
    day += 1
    if day > days_in_month[month - 1]:
        day = 1
        month += 1
        if month > 12:
            month = 1
            year += 1
    return f"{day}/{month}/{year}"

# Test cases
print(next_day(3, 7, 2023))   # Output: 4/7/2023
print(next_day(31, 12, 2023))  # Output: 1/1/2024
print(next_day(28, 2, 2020))   # Output: 29/2/2020
