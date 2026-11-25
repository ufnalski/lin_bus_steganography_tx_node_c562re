# LIN bus break field steganography TX node [STM32C562RE]

Steganography: [IrDA SIR steganography demo](https://github.com/ufnalski/irda_steganography_tx_node_l432kc)

Wiper drive: [MITSUBA WM23B front wiper module with brushless motor and LIN bus interface](https://github.com/ufnalski/mazda_cx30_wiper_actuator_c562re)

Stego-slave RX node: [LIN bus break field steganography RX node](https://github.com/ufnalski/lin_bus_steganography_rx_node_c5a3zg)

![LIN bus short break field steganography TX node in action](/Assets/Images/stego_frame_short_break.JPG)
![LIN bus long break field steganography TX node in action](/Assets/Images/stego_frame_long_break.JPG)

> [!NOTE]
> A standard LIN master sends a break field of at least 13 dominant (low) bits, followed by a break delimiter of at least 1 recessive (high) bit. A standard LIN slave detects that break after 11 dominant bits. A stego LIN master modulates the length of the break field to hide additional bits of information. The stego LIN slave not only reads the regular payload using a UART peripheral but also measures the length of the break field using a TIM peripheral in the input capture mode. In this demo only one hidden bit per frame is sent. One more bit can be hidden in the break delimiter. In fact more than two bits can be hidden if you introduce more than two different duration times. This would increase the throughput of the stego-channel. Remember to account for oscillator frequency tolerance.

# Missing files?
Don't worry. Just open the .ioc2 file in STM32CubeMX2 and hit the yellow button to generate the IDE project. Then open the project in STM32CubeIDE for Visual Studio Code and build it.

# Call to action
Create your own [home laboratory/workshop/garage](http://ufnalski.edu.pl/control_engineering_for_hobbyists/2027_fun_with_electric_motors_and_control_systems/Fun_with_Electric_Motors_and_Control_Systems_2027.pdf)! Get inspired by [ControllersTech](https://www.youtube.com/@ControllersTech), [DroneBot Workshop](https://www.youtube.com/@Dronebotworkshop), [Andreas Spiess](https://www.youtube.com/@AndreasSpiess), [GreatScott!](https://www.youtube.com/@greatscottlab), [bitluni's lab](https://www.youtube.com/@bitluni), [ElectroBOOM](https://www.youtube.com/@ElectroBOOM), [Phil's Lab](https://www.youtube.com/@PhilsLab), [atomic14](https://www.youtube.com/@atomic14), [That Project](https://www.youtube.com/@ThatProject), [Paul McWhorter](https://www.youtube.com/@paulmcwhorter), [Max Imagination](https://www.youtube.com/@MaxImagination), [Nikodem Bartnik](https://www.youtube.com/@nikodembartnik), [Stuff Made Here](https://www.youtube.com/@StuffMadeHere), [Mario's Ideas](https://www.youtube.com/@marios_ideas), [Aaed Musa](https://www.aaedmusa.com/), [Haase Industries](https://www.youtube.com/@h1tec), [Marcin Plaza](https://www.youtube.com/MarcinPlaza), [Predictable Designs with John Teel](https://www.youtube.com/@PredictableDesigns), [Mr Carlson's Lab](https://www.youtube.com/@MrCarlsonsLab), [Piotr Gorecki](https://www.youtube.com/@piotrgorecki_ZE), and many other professionals and professional hobbyists sharing their awesome projects and tutorials! Shout-out/kudos to all of them! Promote [README-driven learning](https://pe.org.pl/wp-content/uploads/2026/06/10_15199_48_2026_06_9.pdf).

> [!WARNING]
> Steganography - do try this with your spouse :grey_exclamation:

230+ challenges to start from: [Control Engineering for Hobbyists at the Warsaw University of Technology](http://ufnalski.edu.pl/control_engineering_for_hobbyists/Control_Engineering_for_Hobbyists_list_of_challenges.pdf).

Stay tuned!

0xBU
