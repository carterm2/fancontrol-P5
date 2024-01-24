import time
from gpiozero import CPUTemperature, PWMOutputDevice

# Fan is connected to GPIO18 for PWM
FAN_PIN = 18

# Temperature thresholds
MIN_TEMP = 55.0  # The temperature at which the fan starts spinning (in Celsius)
MAX_TEMP = 80.0  # The temperature at which the fan spins at maximum speed (in Celsius)

# Create a CPU temperature sensor
cpu = CPUTemperature()

# Create a PWM output device for the fan control
fan = PWMOutputDevice(FAN_PIN)

try:
    while True:
        # Get the current CPU temperature
        temp = cpu.temperature

        # Calculate the fan speed
        if temp < MIN_TEMP:
            duty_cycle = 0
        elif temp > MAX_TEMP:
            duty_cycle = 1
        else:
            duty_cycle = ((temp - MIN_TEMP) / (MAX_TEMP - MIN_TEMP))

        # Set the fan speed
        fan.value = duty_cycle

        # Print the current status
        #print(f"CPU temperature: {temp}°C, Fan speed: {duty_cycle * 100}%")

        # Wait for 1 second
        time.sleep(1)

except KeyboardInterrupt:
    # Reset the fan speed to 0
    fan.value = 0
