# wind-chill
import math

temperature = 0
def celsius_convertion(temperature):
    temperatura_conver = (9/5 * temperature_choice) + 32
    return temperatura_conver 

temperature_choice = float(input("what is the temperature?"))
temperature_choice_conver = celsius_convertion(temperature_choice)
#print(temperature_choice_conver)

f_or_c = input("Farenheight or Celcius (F/C)?")


if f_or_c.lower() == "c":
    for i in range(5, 65, 5):
        wind_chill = 35.74 + 0.6215*temperature_choice_conver  - 35.75*(i**0.16) + 0.4275*((temperature_choice_conver) *(i**0.16))
        print(f"At a temperature of {temperature_choice_conver}F, and a wind speed of {i} mp, the windchill is: {wind_chill:.2f}F ") 
        
if f_or_c.lower() == "f":
    for i in range(5, 65, 5):
        wind_chill2 = 35.74 + 0.6215*temperature_choice  - 35.75*(i**0.16) + 0.4275*((temperature_choice) *(i**0.16))
        print(f"At a temperature of {temperature_choice}F, and a wind speed of {i} mp, the windchill is: {wind_chill2:.2f}F ")
