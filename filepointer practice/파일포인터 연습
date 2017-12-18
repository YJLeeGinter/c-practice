#include <stdio.h>
#include <stdlib.h>
void clear_keyboard(void); // 사용자 정의 함수
void main() {
       FILE *fp; // 파일 포인터 선언
       float data[5]; // 실수형 배열 선언
       int count; // for 함수의 반복 횟수를 위한 정수 count 선언
       char filename[20]; // 문자형 배열. 크기 20 선언
       puts("Enter 5 floating-point numerical values. ");
       for (count = 0; count < 5; count++) {
             scanf_s("%f", &data[count]); // 실수 5개 입력
       }
       clear_keyboard(); // 함수 호출
       puts("Enter a name for the file.");
       gets(filename);
       if ((fp = fopen(filename, "w")) == NULL) { // 파일이 제대로 안 열렸으면 이것을 출력하고 종료
             fprintf(stderr, "Error opening file %s.", filename);
             exit(1);
       }
       for (count = 0; count < 5; count++) {
             fprintf(fp, "\n data[%d] = %f", count, data[count]); // 입력 받은 값을 차례대로 파일포인터가 가리키는 위치에 저장한다.
       }
       fclose(fp);
       printf("\n");
}
void clear_keyboard(void) { // 왜 이것을 선언하는 지 고민중임.
       char junk[80]; // 쓰레기 값 입력 받기 위한 배열 선언
       gets(junk);
}
