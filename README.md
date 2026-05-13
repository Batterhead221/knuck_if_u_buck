# knuck_if_u_buck (12v→5v_buck_converter)

Custom LMR51430 buck converter PCB (12V → 5V @ ~0.5A, designed with ~1A headroom).

CONCEPT DESIGN - WILL NOT FAB

Key features
	•	Optimized SW node geometry
	•	Tight input loop placement (VIN decoupling kept close)
	•	Clean feedback routing with isolation from noisy nodes
	•	Short switching loops for better EMI behavior
	•	Clear grounding strategy (return paths kept compact)
	•	Debug-friendly access (VIN, SW, FB, EN, 5V)

Hardware design
	•	Converter: TI LMR51430
	•	Input: 12V
	•	Output: 5V (target 0.5A, with ~1A headroom)
	•	Inductor: 6.8µH power inductor (500 kHz design choice)
	•	Feedback divider: 100k / 13.7k (sets 5V output)
	•	Output caps: 2×22µF + local decoupling
	•	Input caps: 22µF + 0.1µF placed close to VIN/GND 

Layout priorities
	•	Tight high-current loop: VIN → SW → L → COUT → GND
	•	Keep SW copper small (short + compact)
	•	Solid ground reference near power stage

Early project for learning and and gaining a better understanding of a buck converter.
 
