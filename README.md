# Loops
IS - First Course 2023
#include <iostream>
#include <cmath>
using namespace std;


int main()
{
	/*
	Task
	Да се напише програма,
	която въвежда размерите на геометрична фигура и пресмята лицето й.
	Фигурите са четири вида: квадрат (s), правоъгълник (r), кръг (c) и триъгълник (triangle).
	На първия ред на входа се чете вида на фигурата (square, rectangle, circle или triangle).
	char figure = ' ';
	cin >> figure;

	Ако фигурата е квадрат, на следващия ред се чете едно число – дължина на страната му.
	if (figure == 's')
	{
		double side = 0;
		cin >> side;
		double area = side * side;
		double area1 = round(area * 1000) / 1000;
		cout << area1;
	}
	Ако фигурата е правоъгълник, на следващите два реда четат две числа – дължините на страните му.
	if (figure == 'r')
	{
		double side1 = 0;
		double side2 = 0;
		cin >> side1 >> side2;
		double area = side1 * side2;
		double area1 = round(area * 1000) / 1000;
		cout << area1;
	}
	Ако фигурата е кръг, на следващия ред чете едно число – радиусът на кръга.
	if (figure == 'c')
	{
		const double pi = 3.14159265358979323846;
		double radius = 0;
		cin >> radius;
		double area = pi * (radius * radius);
		double area1 = round(area * 1000) / 1000;
		cout << area1;
	}
	Ако фигурата е триъгълник, на следващите два реда четат две числа
	– дължината на страната му и дължината на височината към нея.
	if (figure == 't')
	{
		double side = 0;
		double height = 0;
		cin >> side >> height;
		double area = (side * height) / 2;
		double area1 = round(area * 1000) / 1000;
		cout << area1;
	}
	Резултатът да се закръгли до 3 цифри след десетичната точка


	Task

	unsigned int n, k;
	cin >> n >> k;

	unsigned max = n > k ? n : k;
	unsigned lcmCandidate = max;

	while (lcmCandidate % n != 0 || lcmCandidate % k != 0)
	{
		lcmCandidate += max;
		cout << lcmCandidate;
	}


	Task

	int n, k;
	cin >> n >> k;
	if (n < k)
	{
		int temp = n;
		n = k;
		k = temp;
	}

	while (k != 0)
	{
		int mod = n % k;
		n = k;
		k = mod;
	}
	cout << n;


	Task

	unsigned int n = 0;
	cin >> n;

	if (n <= 1)
	{
		cout << "Not prime" << endl;
		return 0;
	}

	bool isPrime = true;
	double sqrtFromNumberToCheck = sqrt(n);

	for (int i = 2; i <= sqrtFromNumberToCheck; i++)
	{
		if( n % i == 0 )
		{
			isPrime = false;
			break;
		}
	}
	if(isPrime)
	{
		cout << "Prime";
	}
	else
	{
		cout << "Not prime";
	}


	Task

	int n = 0;
	cin >> n;
	for (int i = n; i > 1; i--)
	{
		bool isPrime = true;
		double temp = sqrt(i);
		for (int k = 2; k <= temp; k++)
		{
			if (i % k == 0)
			{
				isPrime = false;
				break;
			}
		}
		if (!isPrime)
			continue;

		int count = 0;
		while (n % i == 0)
		{
			count++;
			n /= i;
		}
		if (count >= 1)
		{
			cout << i;

			if (count >= 2)
			{
				cout << "^" << count << " ";
			}
		}
	}


	Task

	 int n = 0;
	 cin >> n;

for (int i = 2; i <= n; i++)
{
	int count = 0;

	while (n % i == 0) {
		count++;
		n /= i;
	}
	if (count >= 1)
	{
		cout << i;

		if (count >= 2)
		{
			cout << "^" << count << " ";
		}

}
    

	Task

	int n = 0;
	cin >> n;

	int mostCommonDigit = - 1;
	int mostCommonDigitOccurences = 0;

	for (int currentDigit = 0; currentDigit <= 9; currentDigit++)
	{
		int copyOfN = n;
		int currentDigitOccurences = 0;

		while (copyOfN != 0)
		{
			int lastDigit = copyOfN % 10;
			if (lastDigit == currentDigit)
			{
				currentDigitOccurences++;
				copyOfN /= 10;
			}
		}
		if (currentDigitOccurences>mostCommonDigitOccurences)
		{
			mostCommonDigit = currentDigit;
			mostCommonDigitOccurences = currentDigitOccurences;
		}
	}
	cout << mostCommonDigit;


	Task

	int n;
	int total = 0;

	while (true)
	{
		cin >> n;
		if (n == 0)
		{
			break;
		}

		total += n ;
		cout << total;
	}
	return 0;


	Task

	int n;
	int k;
	cin >> n >> k;

	if (k > n)
	{
		int temp = n;
		n = k;
		k = temp;

		while (k != 0)
		{
			int mod = n % k;
			n = k;
			k = mod;
		}

	}
	cout << n << endl;


	Task

	int z = 0;
	int x = round(3.14);

	cout << x;


	double a;
	double b;
	double c;

	cin >> a >> b;
	c = sqrt(pow(a, 2) + pow(b, 2));

	cout << c;


	Task 0 
Да се напише програма, която след въвеждане на 10 числа от потребителя пресмята тяхната сума!

	int n;
	int total = 0;

	for (int i = 0; i < 10; i++)
	{
		cin >> n;
		total += n;
	}
	cout << total;

	return 0;


	Task 
	 Да се напише програма,
	  която след въвеждане на положително реално число го принтира,
	  но със стойност 0.5 по - малко
	 докато числото не стане по - малко от 0

	double n;
	cin >> n;


	while (n >= 0)
	{
		cout << n << endl;;
		n -= 0.5;

	}
	return 0;


	Task
    Да се пресметне n! за въведено от потребителя число n.

	int n;
	cin >> n;
	int factorial = 1;

	for ( int i = 1; i <= n; i++)
	{
		factorial *= i;
	}
	cout << factorial;

	return 0;


	Task
	int number, sum = 0;

	do
	{
	cin >> number;
	sum += number;
	} while (number != 0);

	cout << sum << endl;

	return 0;


	Task

	int n = 0;
	int digit = 0;
	int total = 0;

	cin >> n;

	while (n > 0)
	{
		digit = n % 10;
		total += digit;
		n /= 10;
	}
	cout << total;

	return 0;


	Task

    int n = 0;
	cin >> n;

	if (n <= 1)
	{
		cout << "Not prime";
	}

	bool isPrime = true;
	double sqrtFromNToCheck = sqrt(n);

	for (int i = 2; i <= sqrtFromNToCheck; i++)
	{
		if (n % i == 0){
			isPrime = false;
			break;
		}
	}

	if (isPrime)
	{
		cout << "IsPrime";
	}
	else
	{
		cout << "Not prime";
	}


	Task

    int n;
    int y;
	cin >> n >> y;

	if (y == 0)
	{
		cout << 0;
	}
	if (y == 1)
	{
		cout << n;
	}

	for (int i = 2; i <= y; i++)
	{
		n *= i;
	}
	cout << n;


	Task

    double base, result = 1.0;
    int exponent;


    cin >> base;
    cin >> exponent;

    bool negativeExponent = false;

// Проверка за отрицателна степен
    if (exponent < 0) {
	    exponent = -exponent;
	    negativeExponent = true;
    }

// Изчисляване на степента
    for (int i = 0; i < exponent; i++) {
	    result *= base;
    }

// Ако степента е отрицателна, връщаме обратната стойност
    if (negativeExponent) {
	    result = 1.0 / result;
    }


    Task
    От клавиатурата се въвеждат произволен брой числа.Намерете сбора на всички числа до въвеждането на 0.

    int n = 0;
	int result = 0;
   

	while (true)
	{   
		cin >> n;
		if (n == 0)
			break;

		result += n;
	}
	cout << result;
	return 0;
    

	Task

    double n;
	double y; 
	double result = 1;
	cin >> n >> y;

	if (y == 0)
	{
		cout << 1;
	}
	else if (y > 0)
	{
        for (int i = 0; i < y; i++)
	    {
		    result *= n;
	    }
		cout << result;
	}
	else
	{
		for (int i = 0; i > y; --i) {
			result /= n;
		}
		cout << result;
	}
	
	return 0;*/

}
