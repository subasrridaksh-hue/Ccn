#include<stdio.h>
#include<conio.h>

void main()
{
 int d[4], r[7], i, s;
 clrscr();

 printf("Enter 4 data bits:\n");
 for(i=0;i<4;i++) scanf("%d",&d[i]);

 r[2]=d[0]; r[4]=d[1]; r[5]=d[2]; r[6]=d[3];

 r[0]=(r[2]+r[4]+r[6])%2;
 r[1]=(r[2]+r[5]+r[6])%2;
 r[3]=(r[4]+r[5]+r[6])%2;

 printf("Hamming code: ");
 for(i=0;i<7;i++) printf("%d",r[i]);

 printf("\nEnter received 7 bits:\n");
 for(i=0;i<7;i++) scanf("%d",&r[i]);

 s=(r[0]+r[2]+r[4]+r[6])%2
  +2*((r[1]+r[2]+r[5]+r[6])%2)
  +4*((r[3]+r[4]+r[5]+r[6])%2);

 if(s==0)
    printf("\nNo error in received code");
 else
 {
    printf("\nError at position %d",s);
    r[s-1]^=1;
    printf("\nCorrected code: ");
    for(i=0;i<7;i++) printf("%d",r[i]);
 }

 getch();
}
