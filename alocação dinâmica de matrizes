#include <stdio.h>
#include <stdlib.h>
int** alocarMatriz(int m, int n) {
 int** matriz = (int*)malloc(m * sizeof(int));
 for (int x = 0; x < m; x++) {
 matriz[x] = (int*)malloc(n * sizeof(int));
 }
 return matriz;
}
void liberarMatriz(int** matriz, int m) {
 for (int x = 0; x < m; x++) {
 free(matriz[x]);
 }
 free(matriz);
}
int main() {
 int m, n;
 printf("Digite o numero de linhas (m): ");
 scanf("%d", &m);
 printf("Digite o numero de colunas (n): ");
 scanf("%d", &n);
 int** matriz = alocarMatriz(m, n);
 for (int x = 0; x < m; x++) {
 for (int y = 0; y < n; y++) {
 matriz[x][y] = x + y;
 }
 }
 // Imprimir a matriz
 printf("Matriz:\n");
 for (int x = 0; x < m; x++) {
 for (int y = 0; y < n; y++) {
 printf("%d ", matriz[x][y]);
 }
 printf("\n");
 }
 // Liberar memória alocada pela matriz
 liberarMatriz(matriz, m);
 return 0;
}
