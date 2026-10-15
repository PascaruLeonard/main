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
    // 1. Verificare de siguranță (Contract Guard)
    // Returnează false FĂRĂ modificări dacă un pointer e null sau indică aceeași adresă
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

