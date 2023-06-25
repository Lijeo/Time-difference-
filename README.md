import datetime
import pytz

def calculate_time_difference(country1, country2):
    # Get current time
    current_time = datetime.datetime.now()

    # Get time zone for country1
    tz_country1 = pytz.timezone(country1)
    time_country1 = current_time.astimezone(tz_country1)

    # Get time zone for country2
    tz_country2 = pytz.timezone(country2)
    time_country2 = current_time.astimezone(tz_country2)

    # Calculate time difference
    time_difference = time_country1 - time_country2

    # Return the time difference
    return time_difference

# Example usage
country1 = 'America/New_York'
country2 = 'Asia/Tokyo'

time_difference = calculate_time_difference(country1, country2)
print("The time difference between", country1, "and", country2, "is", time_difference)
