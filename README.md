# Interface

## Aim:
To write a C# program using interface concept

## Algorithm:


## Program:

```
using System;
using System.Reflection.Metadata.Ecma335;

namespace abhi
{
    
    public interface bank
    {
        public int deposit(int amount);
        public int withd(int amount);
        

    }
    public class Program : bank
    {
        public int amount, amt = 30000;
        public int deposit(int amount)
        {
            this.amount = amount;
            return amt + amount;

        }
        public int withd(int amount)
        {
            this.amount = amount;
            return amt - amount;

        }
        public static void Main(string[] args)
        {
            
            
            Program b = new Program();
            Console.WriteLine("Enter the option \n 1. WITHDRAWL \n 2. DEPOSIT");
            int a = Convert.ToInt32(Console.ReadLine());
            Console.WriteLine("\nAccount Balance : "+b.amt);
            if (a == 1)
            {
                Console.WriteLine("Enter the amount to be withdrawled:");
                b.amount = Convert.ToInt32(Console.ReadLine());
                int c = b.withd(b.amount);
                Console.WriteLine("Bank Balance : " + c);

            }
            if (a == 2)
            {
                Console.WriteLine("Enter the amount to be deposited:");
                b.amount = Convert.ToInt32(Console.ReadLine());
                int d= b.deposit(b.amount);
                Console.WriteLine("Bank Balance : "+d);
                
            }
            
        }
    }
}
```

## Output:
### WITHDRAWL :
![image](https://user-images.githubusercontent.com/66360846/203898482-0089b3ca-253c-416a-ac5e-0a1fcacffeed.png)

### DEPOSIT:
![image](https://user-images.githubusercontent.com/66360846/203898536-8ead4335-fed8-4911-a378-3f8e6001999e.png)


## Result:
