#include <stdio.h>
#include <conio.h>
#include <stdlib.h>
#include <dos.h>   // for delay()

void main() {
    int i, j = 0, n, window = 4;
    clrscr();
    randomize();

    printf("Enter total number of frames: ");
    scanf("%d", &n);

    while (j < n) {
        printf("\nSending frames: ");
        for (i = j + 1; i <= j + window && i <= n; i++)
            printf("%d ", i);

        delay(1000);   // simulate 1-second delay

        if (rand() % 3 == 0) {
            printf("\nSome frames lost! Resending...");
            delay(1000);
        } else {
            j += window;
            if (j > n)
                j = n;
            printf("\nAcknowledgment received up to frame %d", j);
        }
    }

    printf("\n\nAll frames sent successfully (Sliding Window ARQ)\n");
    getch();
}
