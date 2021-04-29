```
```
# 簡答題
## (1)舉例說明 傳直呼叫(call by value)與參考呼叫(call by reference)


## 傳值呼叫(call by value)
```
ex05;
public class callByVal{
public static void main (String[] args){
  int a = 10, b = 15;
  System.out.println (" 傳值呼叫前\t a = " + a + "\t b = " + b );
  byVal(a, b);
  System.out.println (" 傳值呼叫後\t a = " + a + "\t b = " + b );
 }
 static void byVal(int x, int y) {
 int t; //以變數t作為暫存區，將引數互換
 t = x;
 x = y;
 y = t;
 System.out.println(" 傳值呼叫中\t x " + x + +'\t y = " = y  );
 }
}

```
```
結果：
傳值呼叫前 a = 10 b = 15
傳值呼叫中 x = 15 y = 10
傳值呼叫後 a = 10 b =15
```  
## 參考呼叫(call by reference)
```
package ex05;

class 0bj {
  int a, b;
  0bj() {
     a = 10;
     b = 15;
   } 
} 

public class CallByRef {
 public static void main(String[] args) {
   0bj = new 0bj();
   System.out.println(" 參考呼叫前\t a = " + obj.a + "\tb = " = obj.b);
   byRef(obj);
   System.out.println(" 參考呼叫後\t a = " + obj.a + "\tb = " = obj.b);
   }
   
   static void byRef(0bj p) {
   int t;
   t= p.a;
   p.a = p.b;
   p.b = t;
  }
}  

```
結果：
參考呼叫前 a = 10 b = 15
參考呼叫後 a = 15 b = 10
```
```
## 舉例說明 方法多載 

```
package ex05;

public class AddNum {
	public static void main(String[] args) {
		int total1, x=17, y=28;
		double total2, i=3.8, j=22.7, k=15.1;
		total1 = add(x, y);
		total2 = add(i, j, k);
		System.out.printf("%d%n",total1);
		System.out.printf("%f%n",total2);
	}
	static int add(int a, int b) {
		return a + b; // 傳回兩個整數相加的結果
	}
	static double add(double a, double b, double c) {
		return a + b + c; // 傳回三個倍精確度相加的結果
	}
}
```
## 程式設計題 
### (1)請使用靜態遞迴方法算出費氏序列。
``` 
public class MainClass {
 public static void main (String[] args {
  for(int counter : 0; counter < = 10; counter ++) {
   System.out.printf(" Fibonacci of %d is ; %d\n",counter,fibinacci(counter));
   }
  }
  
  public static long fibonacci(long number) {
        if ((number == 0) || (number == 1))
        return number;
        else
        return fibonacci(number - 1) + fibonacci(number - 2);
 }
}
```                                             
### (2)請使用 iterative方法算出費氏數列。
``` 
public class Iterative {
public static long Fibonacci(int n)
    {
        long v1 = 0;
        long v2 = 1;
        long result = n;
        for (int i = 2; i <= n; ++i)
{
             result = v2 + v1;
             v1 = v2;
             v2 = result;
}
                return result;
 }


``` 
