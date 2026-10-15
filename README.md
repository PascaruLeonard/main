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

