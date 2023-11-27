#include <stdio.h>
#include "pico/stdlib.h"

#include "display.h"

/**
* @brief Programa principal
*/
int main() {
  // Inicializo USB
  stdio_init_all();
  // Inicializo display
  display_init();
  
  while (true) {

    // Apago ambos digitos
    gpio_put_masked(DIGITS, DIGITS);
    // Escribo el cero en el digito 2
    gpio_put_masked(SEGMENTS, CERO);
    // Prendo el digito 2
    gpio_put(DIG_2, false);
    // Espero unos milisegundos
    sleep_ms(1000);


    // Escribo el uno en el digito 2
    gpio_put_masked(SEGMENTS, UNO);
    // Prendo el digito 2
    gpio_put(DIG_2, false);
    // Espero unos milisegundos
    sleep_ms(1000);


    // Escribo el dos en el digito 2
    gpio_put_masked(SEGMENTS, DOS);
    // Prendo el digito 2
    gpio_put(DIG_2, false);
    // Espero unos milisegundos
    sleep_ms(1000);


    // Escribo el tres en el digito 2
    gpio_put_masked(SEGMENTS, TRES);
    // Prendo el digito 2
    gpio_put(DIG_2, false);
    // Espero unos milisegundos
    sleep_ms(1000);


    // Escribo el cuatro en el digito 2
    gpio_put_masked(SEGMENTS, CUATRO);
    // Prendo el digito 2
    gpio_put(DIG_2, false);
    // Espero unos milisegundos
    sleep_ms(1000);


    // Escribo el cinco en el digito 2
    gpio_put_masked(SEGMENTS, CINCO);
    // Prendo el digito 2
    gpio_put(DIG_2, false);
    // Espero unos milisegundos
    sleep_ms(1000);


    // Escribo el seis en el digito 2
    gpio_put_masked(SEGMENTS, SEIS);
    // Prendo el digito 2
    gpio_put(DIG_2, false);
    // Espero unos milisegundos
    sleep_ms(1000);


    // Escribo el siete en el digito 2
    gpio_put_masked(SEGMENTS, SIETE);
    // Prendo el digito 2
    gpio_put(DIG_2, false);
    // Espero unos milisegundos
    sleep_ms(1000);


    // Escribo el ocho en el digito 2
    gpio_put_masked(SEGMENTS, OCHO);
    // Prendo el digito 2
    gpio_put(DIG_2, false);
    // Espero unos milisegundos
    sleep_ms(1000);


    
    // Escribo el nueve en el digito 2
    gpio_put_masked(SEGMENTS, NUEVE);
    // Prendo el digito 2
    gpio_put(DIG_2, false);
    // Espero unos milisegundos
    sleep_ms(1000);
    //se repite la secuencia
  }
}
#include <stdio.h>
#include "pico/stdlib.h"

#include "display.h"
bool repeating_timer_callback(struct repeating_timer *t) {
  int val1=0;
    for(val1;val1<=9;val1++){
      switch (val1){
        case 0:
    gpio_put_masked(SEGMENTS, CERO);
    gpio_put(DIG_2, false);
    sleep_ms(1000);
        break;
        case 1:
    gpio_put_masked(SEGMENTS, UNO);
    gpio_put(DIG_2, false);
    sleep_ms(1000);
        break;
        case 2:
    gpio_put_masked(SEGMENTS, DOS);
    gpio_put(DIG_2, false);
    sleep_ms(1000);
        break;
        case 3:
    gpio_put_masked(SEGMENTS, TRES);
    gpio_put(DIG_2, false);
    sleep_ms(1000);
        break;
        case 4:
    gpio_put_masked(SEGMENTS, CUATRO);
    gpio_put(DIG_2, false);
    sleep_ms(1000);
        break;
        case 5:
    gpio_put_masked(SEGMENTS, CINCO);
    gpio_put(DIG_2, false);
    sleep_ms(1000);
        break;
        case 6:
    gpio_put_masked(SEGMENTS, SEIS);
    gpio_put(DIG_2, false);
    sleep_ms(1000);
        break;
        case 7:
    gpio_put_masked(SEGMENTS, SIETE);
    gpio_put(DIG_2, false);
    sleep_ms(1000);
        break;
        case 8:
    gpio_put_masked(SEGMENTS, OCHO);
    gpio_put(DIG_2, false);
    sleep_ms(1000);
        break;
        case 9:
    gpio_put_masked(SEGMENTS, NUEVE);
    gpio_put(DIG_2, false);
    sleep_ms(1000);
    
        break;
      }
    }
    
    return true;
}

/**
* @brief Programa principal
*/
int main() {
  // Inicializo USB
  stdio_init_all();
  // Inicializo display
  display_init();
  gpio_put_masked(DIGITS, DIGITS);
  struct repeating_timer timer;
  // Apago ambos digitos
   add_repeating_timer_ms(0, repeating_timer_callback, NULL, &timer);
  while (true) {
  }
}
#ifndef _DISPLAY_H_
#define _DISPLAY_H_

// GPIOs para segmentos
#define A   0
#define B   1
#define C   2
#define D   3
#define E   4
#define F   5
#define G   6

// GPIOs para cada digito
#define DIG_1   16
#define DIG_2   17

// Macros para hacer mas facil la inicializacion

// Hace referencia a todos los GPIO
#define SEGMENTS  ((1 << A) | (1 << B) | (1 << C) | (1 << D) | \
                  (1 << E) | (1 << F) | (1 << G))

// Hace referencia a los GPIO que controlan los digitos
#define DIGITS    ((1 << DIG_1) | (1 << DIG_2))

// Hace referencia a todos los GPIO que usamos
#define ALL_GPIO  (SEGMENTS | DIGITS)

// Valores que se escriben en cada segmento

#define CERO    ((1 << A) | (1 << B) | (1 << C) | (1 << D) | (1 << E) | (1 << F) | (0 << G))
#define UNO     ((0 << A) | (1 << B) | (1 << C) | (0 << D) | (0 << E) | (0 << F) | (0 << G))
#define DOS     ((1 << A) | (1 << B) | (0 << C) | (1 << D) | (1 << E) | (0 << F) | (1 << G))
#define TRES    ((1 << A) | (1 << B) | (1 << C) | (1 << D) | (0 << E) | (0 << F) | (1 << G))
#define CUATRO  ((0 << A) | (1 << B) | (1 << C) | (0 << D) | (0 << E) | (1 << F) | (1 << G))
#define CINCO   ((1 << A) | (0 << B) | (1 << C) | (1 << D) | (0 << E) | (1 << F) | (1 << G))
#define SEIS    ((1 << A) | (0 << B) | (1 << C) | (1 << D) | (1 << E) | (1 << F) | (1 << G))
#define SIETE   ((1 << A) | (1 << B) | (1 << C) | (0 << D) | (0 << E) | (0 << F) | (0 << G))
#define OCHO    ((1 << A) | (1 << B) | (1 << C) | (1 << D) | (1 << E) | (1 << F) | (1 << G))
#define NUEVE   ((1 << A) | (1 << B) | (1 << C) | (1 << D) | (0 << E) | (1 << F) | (1 << G)) 

/**
* @brief Inicializa los GPIO que estan conectados al display 
*/
static inline void display_init(void) {
  // Inicializo todos los GPIO
  gpio_init_mask(ALL_GPIO);
  // Los pongo como salida
  gpio_set_dir_out_masked(ALL_GPIO);
}

#endif
