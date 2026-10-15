# main
#include <stdio.h>
#include <stdlib.h>

int main(void)
void swap(int *left, int *right) {
    // 1. Salvăm valoarea indicată de 'left' într-o variabilă temporară locală
    int temporary = *left; 
    
    // 2. Copiem valoarea de la adresa 'right' la adresa 'left'
    *left = *right; 
    
    // 3. Punem valoarea temporară la adresa 'right'
    *right = temporary; 
}
