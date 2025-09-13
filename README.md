# CGPA-calculator
#include <iostream>
using namespace std;

int main() {
    int n;
    cout << "Enter the number of subjects: ";
    cin >> n;

    float gradePoints[n], credits[n], totalCredits = 0, weightedSum = 0;

    for (int i = 0; i < n; ++i) {
        cout << "Enter grade point for subject " << i + 1 << ": ";
        cin >> gradePoints[i];

        cout << "Enter credit for subject " << i + 1 << ": ";
        cin >> credits[i];

        weightedSum += gradePoints[i] * credits[i];
        totalCredits += credits[i];
    }

    if (totalCredits == 0) {
        cout << "Total credits cannot be zero." << endl;
        return 1;
    }

    float cgpa = weightedSum / totalCredits;
    cout << "Your CGPA is: " << cgpa
