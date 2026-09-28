# Solar-power-generation-monitor
# Solar Power Generation Monitor
# Python Simulation Program

print("======================================")
print("       SOLAR POWER GENERATION MONITOR")
print("======================================")

# Input values
voltage = float(input("Enter solar panel voltage (V): "))
current = float(input("Enter solar panel current (A): "))
hours = float(input("Enter operating time (hours): "))

# Calculate power and energy
power = voltage * current
power_kw = power / 1000
energy = power_kw * hours

print("\n----------- SOLAR STATUS -----------")
print("Solar Voltage :", voltage, "V")
print("Solar Current :", current, "A")
print("Power Output  :", round(power_kw, 2), "kW")
print("Energy Generated:", round(energy, 2), "kWh")

# System status
if voltage <= 0 or current <= 0:
    print("\n🔴 No solar power generation detected.")

elif power_kw < 1:
    print("\n🟡 LOW POWER GENERATION")

elif power_kw <= 5:
    print("\n🟢 NORMAL POWER GENERATION")

else:
    print("\n🟢 HIGH POWER GENERATION")

print("\n☀️ Solar monitoring completed.")
