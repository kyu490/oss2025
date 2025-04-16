#include <stdio.h>

//유클리드 호제법으로 최대공약수 구하기
int gcd(int a, int b){
  while (b !=0){
    int temp = a;
    b = a % b;
    a = temp;
  }
  return a;
}

int lcm(int a, int b){
  return (a / gcd(a ,b) ) * b;
}

int main(){
  int n, m;
  scanf("%d %d", &n, &m);
  
  printf("%d %d", gcd(m, n), lcm(n, m));

  return 0;
}

  
