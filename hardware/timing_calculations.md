# Timer Calculations

The NE555 timer in monostable mode generates a time delay determined by the RC time constant.

Formula:

T = 1.1 × R × C

Where:
T = time delay
R = resistance
C = capacitance

Timer A (UV exposure time):

R = 1 MΩ  
C = 10 µF

T = 1.1 × (1,000,000) × (10 × 10⁻⁶)

T ≈ 11 seconds

This duration ensures sufficient UV exposure for sterilization.

---

Timer B (buzzer notification):

R = 100 kΩ  
C = 10 µF

T = 1.1 × 100,000 × 10 × 10⁻⁶

T ≈ 1.1 seconds
