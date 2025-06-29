def calculate_bmi(weight, height_cm):
    height_m = height_cm / 100
    return weight / (height_m ** 2)

def check_bmi_level(bmi):
    if bmi < 18.5:
        return "Underweight"
    elif bmi < 25:
        return "Normal"
    elif bmi < 30:
        return "Overweight"
    else:
        return "Obese"

print("BMI Calculator")
weight = float(input("Weight (kg): "))
height = float(input("Height (cm): "))
age = int(input("Age: "))

bmi = calculate_bmi(weight, height)
level = check_bmi_level(bmi)

print(f"\nBMI: {bmi:.2f}")
print(f"Level: {level}")

if age < 18:
    print("You are under 18. BMI may not be exact.")
elif age > 60:
    print("Over 60. Talk to a doctor for advice.")
