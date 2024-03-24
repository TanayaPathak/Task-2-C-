# Task-2-C-

#include <iostream>

float add(float x, float y) {
    return x + y;
}

float subtract(float x, float y) {
    return x - y;
}

float multiply(float x, float y) {
    return x * y;
}

float divide(float x, float y) {
    if (y != 0) {
        return x / y;
    } else {
        return "Error: Division by zero";
    }
}

int main() {
    std::cout << "Select operation:" << std::endl;
    std::cout << "1. Addition" << std::endl;
    std::cout << "2. Subtraction" << std::endl;
    std::cout << "3. Multiplication" << std::endl;
    std::cout << "4. Division" << std::endl;

    int choice;
    while (true) {
        try {
            std::cout << "Enter choice (1/2/3/4): ";
            std::cin >> choice;
            if (choice == 1 || choice == 2 || choice == 3 || choice == 4) {
                break;
            } else {
                std::cout << "Invalid input! Please enter a valid choice." << std::endl;
            }
        } catch (std::exception& e) {
            std::cout << "Invalid input! Please enter a valid choice." << std::endl;
        }
    }

    float num1, num2;
    std::cout << "Enter first number: ";
    std::cin >> num1;
    std::cout << "Enter second number: ";
    std::cin >> num2;

    if (choice == 1) {
        std::cout << "Result: " << add(num1, num2) << std::endl;
    } else if (choice == 2) {
        std::cout << "Result: " << subtract(num1, num2) << std::endl;
    } else if (choice == 3) {
        std::cout << "Result: " << multiply(num1, num2) << std::endl;
    } else if (choice == 4) {
        std::cout << "Result: " << divide(num1, num2) << std::endl;
    }

    return 0;
}

