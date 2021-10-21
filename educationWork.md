# Education & Work
**Schools Attended**
1. Mill Creek Elementary School
2. Jefferson Middle School
3. Rock Bridge High School
4. University of Missouri

At Rock Bridge I began developing an interest for the IT field by taking some computer networking classes at Career Center along with an intro level programming class, below you can find an example of a program I made while in that class. At Mizzou I currently plan on majoring in Information Technology

**Places of Employment**
1. HyVee
2. Pickleman's
3. Gravity

I am working at Gravity right now as an iOS technician.

- [Home Page](https://github.com/LoganCockrell/midtermProject/blob/main/README.md)
- [Growing Up](https://github.com/LoganCockrell/midtermProject/blob/main/growingUp.md)
- [Hobbies](https://github.com/LoganCockrell/midtermProject/blob/main/hobbies.md)
- [this is a page filled exclusively with capybara images on my computer (WARNING: there are a lot.)](https://github.com/LoganCockrell/midtermProject/blob/main/capys.md)

```
#include <iostream>
using namespace std;
void primeCheck(int number, bool prime, int div);
void primeCheck2(int number, bool prime, int div); 
int main()
{
    cout << "Logan Cockrell\n4th Block\n";
    int number, div, option;        
    bool prime = true;    
    cout << "Enter a number: ";
    cin >> number;
    div = number - 1;
    cout << "Would you like to test part 1 or part 2? (1 for part 1, 2 for part 2): \n";
    cin >> option;
    if (option == 1)
        primeCheck(number, prime, div);
    if (option == 2)
    {
        cout << "Prime numbers less than " << number << " are: \n";
        primeCheck2(number, prime, div);
    }
}
void primeCheck(int number, bool prime, int div)  //part 1
{
    if (div == 1)
    {
        if (prime == true)
            cout << number << " is prime. \n";
        if (prime == false)                      //part 2: remove lines 40 and 41
            cout << number << " is not prime \n";

        div = number;
    }
    else
    {
        if (number % div == 0 && number >= div)
            prime = false;
        primeCheck(number, prime, div - 1);
    }
}
void primeCheck2(int number, bool prime, int div) //part 2
{
    if (number == 2)
        cout << "complete. \n";
    else
    {
        primeCheck(number - 1, prime, div - 1);
        primeCheck2(number - 1, prime, div - 1);
    }
}
```
