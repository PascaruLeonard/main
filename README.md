# main
#include <stdio.h>
#include <stdlib.h>

int main(void)
void swap(int *left, int *right) {
    int temporary = *left; 
    *left = *right; 
    *right = temporary; 
}

#include <stdbool.h>
#include <stddef.h>

bool minmax(int first, int second, int *minimum, int *maximum) {
    if (minimum == NULL || maximum == NULL || minimum == maximum) {
        return false;
    }
    if (first <= second) {
        *minimum = first;
        *maximum = second;
    } else {
        *minimum = second;
        *maximum = first;
    }
    return true;
}


#include <stdbool.h>
#include <stddef.h>

bool clamp_range(int value, int lower, int upper, int *result) {
    if (result == NULL || lower > upper) {
        return false;
    }
    if (value < lower) {
        *result = lower; // Sub limita inferioară
    } else if (value > upper) {
        *result = upper; // Peste limita superioară
    } else {
        *result = value; // În interiorul intervalului
    }
    return true;
    }

#include <stdio.h>

int main() {
    // Exemplul 1: sensor_a = -12, sensor_b = 4, lower = -5, upper = 8
    int sensor_a = -12;
    int sensor_b = 4;
    int lower = -5;
    int upper = 8;

    int coldest = 0;
    int hottest = 0;
    int control = 8;

    if (minmax(sensor_a, sensor_b, &coldest, &hottest) && 
        clamp_range(sensor_a, lower, upper, &control)) {
        
        printf("Raport Valid:\n");
        printf("coldest = %d (Cea mai mica citire)\n", coldest);   // -12
        printf("hottest = %d (Cea mai mare citire)\n", hottest);   // 4
        printf("control = %d (sensor_a limitat la lower)\n", control); // -5
    } else 
    {
        printf("Eroare la procesarea citirilor!\n");
    }
    int control_santinela = 99;
    bool status = clamp_range(sensor_a, 8, -5, &control_santinela);
    
    printf("\nTest Interval Invalid: status=%s, control_santinela=%d\n", 
           status ? "true" : "false", control_santinela);

    return 0;
    }

