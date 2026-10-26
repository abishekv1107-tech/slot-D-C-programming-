# slot-D-C-programming-

QUESTION-1



#include<stdio.h>
#include<stdbool.h>

int main() {
    float distance, fare = 100;
    bool member;

    printf("Distance: ");
    scanf("%f", &distance);

    printf("Member (1 for true, 0 for false): ");
    scanf("%d", (int *)&member);

    if (distance > 10) {
        fare = fare + (distance - 10) * 20;
    }

    if (member) {
        fare = fare - (fare * 0.10);
    }

    printf("Final Fare: ₹%.0f\n", fare);

    return 0;
}

QUESTION-2

#include <stdio.h>

int main() {
    int questionsAnswered, remainingTime, alreadySubmitted;

    printf("Questions Answered: ");
    scanf("%d", &questionsAnswered);

    printf("Remaining Time: ");
    scanf("%d", &remainingTime);

    printf("Already Submitted: ");
    scanf("%d", &alreadySubmitted);

    if (questionsAnswered >= 1 && remainingTime > 0 && alreadySubmitted == 0) {
        printf("Submission Allowed");
    } else {
        printf("Submission Not Allowed");
    }

    return 0;
}

QUESTON-3

#include <stdio.h>

int main() {
    int gold, x, y;
    int remaining, blackbeardShare, pirateShare;

    scanf("%d", &gold);
    scanf("%d", &x);
    scanf("%d", &y);

    remaining = gold - (gold * x / 100);
    blackbeardShare = remaining * y / 100;
    remaining = remaining - blackbeardShare;

    pirateShare = remaining / 3;

    printf("%d", pirateShare);

    return 0;
}

QUESTION-4

#include <stdio.h>

int main() {
    int dollar1, cent1, dollar2, cent2;
    int totalCents, totalDollars;

    scanf("%d %d %d %d", &dollar1, &cent1, &dollar2, &cent2);

    totalCents = cent1 + cent2;
    totalDollars = dollar1 + dollar2 + totalCents / 100;

    printf("%d", totalDollars);

    return 0;
}

QUESTION-5

#include <stdio.h>

int main() {
    float mileage;
    int petrol, distance;

    scanf("%f", &mileage);
    scanf("%d", &petrol);
    scanf("%d", &distance);

    if (mileage * petrol >= distance) {
        printf("Can reach");
    } else {
        printf("Cannot reach");
    }

    return 0;
}

QUESTION-6

#include <stdio.h>

int main() {
    int A, B, C, car;

    scanf("%d", &A);
    scanf("%d", &B);
    scanf("%d", &C);
    scanf("%d", &car);

    if (car <= A) {
        printf("Car 1 goes into road A");
    } else if (car <= A + B) {
        printf("Car 1 goes into road B");
    } else if (car <= A + B + C) {
        printf("Car 1 goes into road C");
    } else {
        printf("No path exists");
    }

    return 0;
}

QUESTION-7

int main() {
    int principal, rate, years;
    float interest, amount, discount, settlement;

    scanf("%d", &principal);
    scanf("%d", &rate);
    scanf("%d", &years);

    interest = (principal * rate * years) / 100.0;
    amount = principal + interest;
    discount = interest * 2 / 100.0;
    settlement = amount - discount;

    printf("%.2f\n", interest);
    printf("%.2f\n", amount);
    printf("%.2f\n", discount);
    printf("%.2f\n", settlement);

    return 0;
}

QUESTION-8

 int main() {
    int experience, performance;

    printf("Experience: ");
    scanf("%d", &experience);

    printf("Performance: ");
    scanf("%d", &performance);

    if (experience > 7 && performance >= 85) {
        printf("Level: Senior");
    } 
    else if (experience >= 3 && performance >= 80) {
        printf("Level: Mid-Level");
    } 
    else {
        printf("Level: Junior");
    }

    return 0;
}

QUESTION-9

#include <stdio.h>

int main() {
    int year, month, days;

    scanf("%d", &year);
    scanf("%d", &month);

    if (year < 1900 || year > 9999) {
        printf("0");
    }
    else {
        switch (month) {
            case 1: case 3: case 5: case 7:
            case 8: case 10: case 12:
                days = 31;
                break;

            case 4: case 6: case 9: case 11:
                days = 30;
                break;

            case 2:
                if ((year % 400 == 0) ||
                    (year % 4 == 0 && year % 100 != 0)) {
                    days = 29;
                } else {
                    days = 28;
                }
                break;

            default:
                printf("0");
                return 0;
        }

        printf("%d Days", days);
    }

    return 0;
}

QUESTION-10

#include <stdio.h>

int main() {
    int units;
    float bill;

    scanf("%d", &units);

    if (units <= 200) {
        bill = units * 0.5;
    }
    else if (units <= 400) {
        bill = units * 0.65 + 100;
    }
    else if (units <= 600) {
        bill = units * 0.80 + 200;
    }
    else {
        bill = units * 1.25 + 425;
    }

    printf("Rs.%.0f", bill);

    return 0;
}

