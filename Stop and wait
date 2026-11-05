#include <stdio.h>
#include <conio.h>
#include <stdlib.h>
#include <dos.h>   // for delay()

void main() {
    int i, n;
    clrscr();
    randomize();

    printf("Enter number of frames: ");
    scanf("%d", &n);

    for (i = 1; i <= n; i++) {
        printf("\nSending frame %d...", i);
        delay(1000); // delay 1 second
        if (rand() % 2 == 0) {
            printf("\nFrame %d lost! Resending...", i);
            delay(1000);
        }
        printf("\nAcknowledgment for frame %d received.", i);
    }

    printf("\n\nAll frames sent successfully (Stop and Wait ARQ)\n");
    getch();
}
