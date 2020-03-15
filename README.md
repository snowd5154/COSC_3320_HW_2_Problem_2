package TimingAlgorithm

public class values {

public static void main(string[] args){

//n-values to be used

int n[6] = { 16, 64, 256, 1024, 4096, 16384 };
int next = 0;
while (next < 6) {
int a, b, x;
//initialize M
int** M = new int *[n[next]];
//for loop
for(int i = 0; i < n[next]; i++)
{
M[i] = new int[i];
}
// Initialize Matrix to 0
//For Loop

for(int i = 0; i < n[next]; i++){
for(int j = 0; j < n[next]; j++){
M[i][j] = 0;
}
}
size_t m = 1677721600;
size_t m = 13421772800;
time_t timer;
timer = clock();
//Calculation by adding random numbers from 1-100
for(int i = 0; i < m; i++) {
x = rand() % 100 + 1;
b = rand() % n[next];
a = rand() % n[next];
M[a][b] = M[a][b] + x;
}
timer = clock() - timer
System.out.println("Clock time for n size %d: %.2f seconds" + n[next], ((float)timer)/CLOCKS_PER_SECOND);
System.out.println("\n\n");
next++; //increment
}
