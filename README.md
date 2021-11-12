#define _CRT_SECURE_NO_WARNINGS

#include<stdio.h>

int main()

{

    float money = 0;
    int m = 0;
    int d = 0;
    int h = 0;
    float p = 0;
    scanf("%.1f %d %d %d", &money, &m, &d, &h);
    if (11 == m && 11 == d)
    {
        if (0 == h)
        {
            p = money * 0.7;
            printf("%.2f\n", p);
        }
        else
        {
            p = money * 0.7 - 50;
            printf("%.2f\n", p);
        }
    }
    else if (12 == m && 12 == d)
    {
        if (0 == h)
        {
            p = money * 0.8;
            printf("%.2f\n", p);
        }
        else
        {
            p = money * 0.8 - 50;
            printf("%.2f\n", p);
        }
    }
    else
        printf("%.2f\n");
    return 0;
    
}

int main()

{

    int i = 0;
    for (i = 10000; i <= 99999; i++)
    {
        int a1, b1, a2, b2, a3, b3, a4, b4, sum1, sum2, sum3, sum4;
        a1 = i / 10000;//万位
        b1 = i - a1 * 10000;//后四位
        sum1 = a1 * b1;

        a2 = i / 1000;//万千位
        b2 = i - a2 * 1000;//后三位
        sum2 = a2 * b2;

        a3 = i / 100;//万千百位
        b3 = i - a3 * 100;//十个位
        sum3 = a3 * b3;

        a4 = i / 10;//前四位
        b4 = i - a4 * 10;//个位
        sum4 = a4 * b4;
        if (sum1 + sum2 + sum3 + sum4 == i)
            printf("%d ", i);
    }
    return 0;
    
}


#include<stdio.h>

int main()

{

    int arr[40] = { 0 };
    int num = 0;
    scanf("%d", &num);//输入几名
    for (int k = 0; k <= num; k++) {//输入成绩
        scanf("%d", &arr[k]);
    }
    int temp = 0;
    for (int i = 0; i < num; i++) {//第i位为最大数
        for (int j = i + 1; j < num; j++) {//从第i+1位开始遍历剩余数
            if (arr[j] > arr[i]) {//存在大于最大数的数
                temp = arr[i];//把最大数和比较数进行交换
                arr[i] = arr[j];
                arr[j] = temp;
            }

        }
    }
    for (int k = 0; k < 5; k++)
        printf("%d ", arr[k]);

    return 0;
    
}


int main()

{

    int i = 0;
    scanf("%d", &i);
    if (i >= 140)
            printf("Genius\n");
    return 0;
    
}


#include <stdio.h>

int main()

{

    int g;
    while ((scanf("%d", &g)) != EOF)
    {
        if (g >= 60)
            printf("Pass\n");
        else
            printf("Fail\n");
    }
    return 0;
    
}


int main()

{

    char i = 0;
    
    while (scanf("%c ", &i)!=EOF)
    {
        switch (i)
        {
        case 'A':
        case 'a':
        case 'E':
        case 'e':
        case 'I':
        case 'i':
        case 'O':
        case 'o':
        case 'U':
        case 'u':
            printf("Vowel\n");
            break;
        default:
            printf("Consonant\n");
            break;
        }
    }
    return 0;
    
}


int main()

{

    char i = 0;
    while (scanf("%c ", &i) != EOF)
    {
        if (65 <= i && i <= 90 || 97 <= i && i <= 122)
            printf("%c is an Alphabet.\n", i);
        else
            printf("%c is not an alphabet.\n", i);
    }
    return 0;
    
}


int main()

{

    char i = 0;
    while (scanf("%c ", &i) != EOF)
    {
        if (i <= 90 && i >= 65)
        {
            i += 32;
            printf("%c\n", i);
        }
        else if (i >= 97 && i <= 122)
        {
            i -= 32;
            printf("%c\n", i);
        }
        else
            ;
    }
    return 0;
    
}


int main()

{

    int t = 0;
    while (scanf("%d", &t) != EOF)
    {
        if (t > 0)
            printf("1\n");
        else if (t = 0)
            printf("0.5\n");
        else
            printf("0\n");
    }
    return 0;
    
}


#include <stdio.h>

int main()

{

    int a = 1, b = 1, c = 1;

    while (scanf("%d %d %d", &a, &b, &c) != EOF)
    {
        if (a + b > c && a + c > b && b + c > a)
        {
            if (a == b && b == c)
            {
                printf("Equilateral triangle!\n");
            }
            else if (a == b || b == c || a == c)
            {
                printf("Isosceles triangle!\n");
            }
            else
            {
                printf("Ordinary triangle!\n");
            }
        }
        else
        {
            printf("Not a triangle!\n");
        }
    }
    return 0;
    
}


int main()

{

    float w = 0;
    float h = 0;
    while (scanf("%f %f", &w, &h) != EOF)
    {
        float h1 = h / 100;//w/(h1*h1)
        float BMI = w / (h1 * h1);
        if (BMI < 18.5)
            printf("Underweight\n");
        else if (BMI >= 18.5 && BMI <= 23.9)
            printf("Normal\n");
        else if (BMI > 23.9 && BMI <= 27.9)
            printf("Overweight\n");
        else
            printf("Obese\n");
    }
    return 0;
    
}


#include<math.h>

int main()

{

    double a, b, c, x1, x2;
    while (scanf("%lf %lf %lf", &a, &b, &c)!=EOF)
    {
        double D = b * b - 4 * a * c;
        if (0 != a)
        {
            if (D == 0)
            {
                x1 = -b / (2 * a);
                x2 = x1;
                printf("x1=x2=%.2lf\n", x1);
            }
            else if (D > 0)
            {
                x1 = -b / (2 * a) - sqrt(D) / (2 * a);
                x2 = -b / (2 * a) + sqrt(D) / (2 * a);
                if (x1 >= x2)
                {
                    printf("x1=%.2lf;x2=%.2lf\n", x2, x1);
                }
                else
                {
                    printf("x1=%.2lf;x2=%.2lf\n", x1, x2);
                }
            }
            else//D<0
            {
                double s, x;
                s = -b / (2 * a);
                x = sqrt(-D) / (2 * a);
                printf("x1=%.2lf-%.2lfi;x2=%.2lf+%.2lfi\n", s, x, s, x);
            }
        }
        else//0==a
        {
            printf("Not quadratic equation\n");
        }
    }
    return 0;
    
}


int main()

{

    int y, m;
    while (scanf("%d %d", &y, &m) != EOF)
    {
        if (y % 4 == 0 && y % 100 != 0 || y % 400 == 0)
        {
            switch (m)
            {
            case 1:
            case 3:
            case 5:
            case 7:
            case 8:
            case 10:
            case 12:
                printf("31\n");
                break;
            case 4:
            case 6:
            case 9:
            case 11:
                printf("30\n");
                break;
            default:
                printf("29\n");
                break;
            }
        }
        else
        {
            switch (m)
            {
            case 1:
            case 3:
            case 5:
            case 7:
            case 8:
            case 10:
            case 12:
                printf("31\n");
                break;
            case 4:
            case 6:
            case 9:
            case 11:
                printf("30\n");
                break;
            default:
                printf("28\n");
                break;
            }
        }
    }
    
    return 0;
    
}



int main()

{

    double a, b;
    char ch;
    scanf("%lf %c %lf", &a, &ch, &b);
    if (ch == '+' || ch == '-' || ch == '*' || ch == '/')
    {
        if (ch == '+')
            printf("%.4lf%c%.4lf=%.4lf\n", a, ch, b, a + b);
        else if (ch == '-')
            printf("%.4lf%c%.4lf=%.4lf\n", a, ch, b, a - b);
        else if (ch == '*')
            printf("%.4lf%c%.4lf=%.4lf\n", a, ch, b, a * b);
        else
        {
            if (b == 0.0)
                printf("Wrong!Division by zero!\n");
            else
                printf("%.4lf%c%.4lf=%.4lf\n", a, ch, b, a / b);
        }
    }
    else
    {
        printf("Invalid operation!\n");
    }
    return 0;
    
}


int main()

{

    int g = 0;
    int i = 0;
    int s = 0;
    while (scanf("%d", &g) != EOF)
    {
        for (s = 1; s <= g; s++)
        {
            for (i = 1; i <= g; i++)
            {
                printf("* ");
            }
            printf("\n");
        }
    }
    return 0;
    
}


int main()

{

    int a = 0;
    int b = 0;
    int g = 0;
    while (scanf("%d", &g)!=EOF)
    {
        for (b = g; b > 0; b--)
        {
            for (a = b; a > 0; a--)
            {
                printf("* ");
            }
            printf("\n");
        }
    }
    return 0;
    
}


int main()

{

    int a = 0;
    int b = 0;
    int c = 0;
    int g = 0;
    scanf("%d", &g);//5
    for (a = 1; a <= g - 1; a++)
    {
        printf("  ");
    }
    for (c = 1; c <= g; c++)
    {
        printf("* ");
    }
    return 0;
    
}


int main()

{

    int a = 0;
    int b = 0;
    int c = 0;
    int g = 0;
    while (scanf("%d", &g)!=EOF)
    {
        for (b = 1; b <= g; b++)
        {
            for (a = 1; a <= g - b; a++)
            {
                printf(" ");
            }
            for (c = 1; c <= b; c++)
            {
                printf("* ");
            }
            printf("\n");
        }
    }
    return 0;
    
}


int main()

{

    int H = 0;
    while (scanf("%d", &H) != EOF)
    {
        switch (H)
        {
        case 200:
            printf("OK\n");
            break;
        case 202:
            printf("Accepted\n");
            break;
        case 400:
            printf("Bad Request\n");
            break;
        case 403:
            printf("Forbidden\n");
            break;
        case 404:
            printf("Not Found\n");
            break;
        case 500:
            printf("Internal Server Error\n");
            break;
        case 502:
            printf("Bad Gateway\n");
            break;
        }
    }
    
    return 0;
    
}
