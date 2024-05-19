#include "mbed.h"

DigitalIn button1(p13);
DigitalIn button2(p16);
DigitalOut led1(p23);
DigitalOut led2(p25);

int main() {
    // Initialize the state of LEDs
    led1 = 0; // Turn off LED1
    led2 = 0; // Turn off LED2

    while (1) {
        if (button1 == 1) {
            led1 = 1; // Turn on LED1
            led2 = 0; // Turn off LED2
        } else if (button2 == 1) {
            led1 = 0; // Turn off LED1
            led2 = 1; // Turn on LED2
        } else {
            led1 = 0; // Turn off LED1
            led2 = 0; // Turn off LED2
        }
    }
}
