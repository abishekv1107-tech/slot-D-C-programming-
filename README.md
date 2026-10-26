# slot-D-C-programming-

QUESTION-1

#include <stdio.h>
#include <string.h>

int main() {
    double distance, fare = 100.0;
    char member[10];

    scanf("%lf %9s", &distance, member);

    if (distance > 10.0) {
        fare += (distance - 10.0) * 20.0;
    }

    if (strcmp(member, "true") == 0 || strcmp(member, "TRUE") == 0 ||
        strcmp(member, "1") == 0 || strcmp(member, "yes") == 0) {
        fare *= 0.90;
    }

    printf("Final Fare: Rs.%.2f\n", fare);
    return 0;
}
