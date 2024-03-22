public class ThreadDemo1 {
 public static void main(String[] args) {
 System.out.println("Start of main");
 MyThread1 mt1 = new MyThread1();
 MyThread2 mt2 = new MyThread2();
 mt1.start();
 mt2.start();
 System.out.println("End of main");
 }
}
class MyThread1 extends Thread{
 public void run(){
 for(int i=1;i<=10;i++) {
 System.out.println("MyThread-1."+i);
 }
 }
}
class MyThread2 extends Thread{
 public void run(){
 for(int i=1;i<=10;i++) {
 System.out.println("MyThread-2."+i);
 }
 }
}
