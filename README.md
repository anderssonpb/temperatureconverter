# Temperature Converter
Temperature converter using Python

 - Code to practice python skills

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------

# Temperature Converter

This project is a simple temperature converter in Python that allows conversions between Celsius, Fahrenheit, and Kelvin.

## Features
- Convert Celsius to Fahrenheit
- Convert Fahrenheit to Celsius
- Convert Celsius to Kelvin
- Convert Kelvin to Celsius
- Convert Fahrenheit to Kelvin
- Convert Kelvin to Fahrenheit

## How to Use
1. Run the Python script.
2. Choose one of the conversion options presented in the menu.
3. Enter the desired temperature.
4. The program will display the converted temperature.

## Example Usage
```
Temperature Converter
1. Celsius to Fahrenheit
2. Fahrenheit to Celsius
3. Celsius to Kelvin
4. Kelvin to Celsius
5. Fahrenheit to Kelvin
6. Kelvin to Fahrenheit
Choose an option (1-6): 1
Enter temperature in Celsius: 25
25.0°C is 77.0°F
```

## Requirements
- Python 3.x

## How to Run
1. Save the code in a file, for example, `converter.py`.
2. In the terminal or command prompt, navigate to the directory where the file is saved.
3. Run the command:
   ```
   python converter.py
   ```

## Author
Developed by Andersson Barbosa



def celsius_to_fahrenheit(celsius):
    return (celsius * 9/5) + 32

def fahrenheit_to_celsius(fahrenheit):
    return (fahrenheit - 32) * 5/9

def celsius_to_kelvin(celsius):
    return celsius + 273.15

def kelvin_to_celsius(kelvin):
    return kelvin - 273.15

def fahrenheit_to_kelvin(fahrenheit):
    celsius = fahrenheit_to_celsius(fahrenheit)
    return celsius_to_kelvin(celsius)

def kelvin_to_fahrenheit(kelvin):
    celsius = kelvin_to_celsius(kelvin)
    return celsius_to_fahrenheit(celsius)

def temperature_converter():
    print("Temperature Converter")
    print("1. Celsius to Fahrenheit")
    print("2. Fahrenheit to Celsius")
    print("3. Celsius to Kelvin")
    print("4. Kelvin to Celsius")
    print("5. Fahrenheit to Kelvin")
    print("6. Kelvin to Fahrenheit")
    
    choice = input("Choose an option (1-6): ")
    
    if choice == '1':
        celsius = float(input("Enter temperature in Celsius: "))
        print(f"{celsius}°C is {celsius_to_fahrenheit(celsius)}°F")
    elif choice == '2':
        fahrenheit = float(input("Enter temperature in Fahrenheit: "))
        print(f"{fahrenheit}°F is {fahrenheit_to_celsius(fahrenheit)}°C")
    elif choice == '3':
        celsius = float(input("Enter temperature in Celsius: "))
        print(f"{celsius}°C is {celsius_to_kelvin(celsius)}K")
    elif choice == '4':
        kelvin = float(input("Enter temperature in Kelvin: "))
        print(f"{kelvin}K is {kelvin_to_celsius(kelvin)}°C")
    elif choice == '5':
        fahrenheit = float(input("Enter temperature in Fahrenheit: "))
        print(f"{fahrenheit}°F is {fahrenheit_to_kelvin(fahrenheit)}K")
    elif choice == '6':
        kelvin = float(input("Enter temperature in Kelvin: "))
        print(f"{kelvin}K is {kelvin_to_fahrenheit(kelvin)}°F")
    else:
        print("Invalid choice. Please select a valid option.")

# Run the temperature converter
temperature_converter()
