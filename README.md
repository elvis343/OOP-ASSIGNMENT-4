# OOP-ASSIGNMENT-4
Question One

import java.util.Scanner;

public class StudentResults {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Enter student's full name: ");
        String fullName = scanner.nextLine();
        String[] subjects = new String[5];
        int[] marks = new int[5];
        for (int i = 0; i < 5; i++) {
            System.out.print("Enter subject " + (i + 1) + " name: ");
            subjects[i] = scanner.nextLine();

            System.out.print("Enter marks for subject " + (i + 1) + ": ");
            marks[i] = Integer.parseInt(scanner.nextLine());
        }

        scanner.close();

        System.out.println("\nStudent's Name: " + fullName);
        System.out.println("Subject\t\tMarks\tGrade");
        System.out.println("-------\t\t-----\t-----");

        for (int i = 0; i < 5; i++) {
            String grade = calculateGrade(marks[i]);
            System.out.println(subjects[i] + "\t\t" + marks[i] + "\t" + grade);
        }
    }

    private static String calculateGrade(int marks) {
        if (marks >= 90) {
            return "A+";
        } else if (marks >= 80) {
            return "A";
        } else if (marks >= 70) {
            return "B";
        } else if (marks >= 60) {
            return "C";
        } else if (marks >= 50) {
            return "D";
        } else {
            return "F";
        }
    }
}

Question Two

public class BreakStatements {
    public static void main(String[] args) {
        outerLoop: 
        for (int i = 1; i <= 3; i++) {
            for (int j = 1; j <= 3; j++) {
                System.out.println("i = " + i + ", j = " + j);
                if (i == 2 && j == 2) {
                    break outerLoop;
                }
            }
        }

        System.out.println(); // Print a new line for clarity
        for (int i = 1; i <= 3; i++) {
for (int j = 1; j <= 3; j++) {
                System.out.println("i = " + i + ", j = " + j);

                if (i == 2 && j == 2) {
                    break;
                }
            }
        }
    }
}

Question Three

Branching statements are used to  to control the flow of execution within a program based on certain conditions. 
Branching statements in Java provide different ways to control the flow of execution based on conditions or iterations.
They improve the flexibility and efficiency of programming by allowing programs to adapt to different scenarios and handle
various cases in different ways. 

Question Four

import java.util.Scanner;

public class MaxNumber {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Enter the first number: ");
        int num1 = scanner.nextInt();

        System.out.print("Enter the second number: ");
        int num2 = scanner.nextInt();

        int maxNum;
        switch (num1 > num2 ? 1 : (num1 < num2 ? 2 : 0)) {
            case 1:
                max = num1;
                break;
            case 2:
                max = num2;
                break;
            default:
                System.out.println("Both numbers are equal.");
                return;
        }

        System.out.println("The maximum number is: " + maxNumber);
    }
}

Question Five

public class StudentGradeProgram {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Enter the full name of the student: ");
        String fullName = scanner.nextLine();

        System.out.print("Enter the score: ");
        int score = scanner.nextInt();

        String grade;

        if (score >= 70) {
            grade = "A";
        } else if (score >= 60) {
            grade = "B";
        } else if (score >= 50) {
            grade = "C";
        } else if (score >= 40) {
            grade = "D";
        } else if (score >= 0 && score < 40) {
            grade = "F";
        } else {
            grade = "Invalid";
        }

        System.out.println("Full Name: " + fullName);
        System.out.println("Grade: " + grade);

        scanner.close();
    }
}

Question Six

public class LoopExample {
    public static void main(String[] args) {
        for (int i = 12; i <= 28; i += 2) {
            System.out.print(i+" ");
            if (i < 28) {
                System.out.print(", ");
            }
        }
    }
}

Question Seven

public class TotalNumbers {
    public static void main(String[] args) {
        int start = 20;
        int end = 25;
        int sum = 0;

        for (int i = start; i <= end; i++) {
            sum += i;
        }

        System.out.println("The Total of numbers between " + start + " and " + end + " is: " + sum);
    }
}

Question Eight

public class EvenNumbers {
    public static void main(String[] args) {
        int number = 12;
        
        System.out.println("Even numbers from 12 to 50:");
        
        do {
            if (number % 2 == 0) {
                System.out.print(number + " ");
            }
            number++;
        } while (number <= 50);
        
        System.out.println(); 
    }
}

Question Nine

public class SumBetweenNumbers {
    public static void main(String[] args) {
        int start = 20;
        int end = 25;
        int sum = 0;
        int currentNumber = start;

        do {
            sum += currentNumber;
            currentNumber++;
        } while (currentNumber <= end);

        System.out.println("The sum of numbers between " + start + " and " + end + " is: " + sum);
    }
}

Question Ten

import java.util.Scanner;

public class SumOfIntegers {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        
        int sum = 0;
        int num;

        do {
            System.out.print("Enter a number (enter 0 to stop): ");
            num = scanner.nextInt();
            
            sum += num;
        } while (num != 0);

        System.out.println("The sum of the entered numbers is: " + sum);
    }
}

Question Eleven

public class PrimeNumbers {
    public static void main(String[] args) {
        int number = 2;

        while (number <= 100) {
            boolean isPrime = true;

            for (int i = 2; i <= Math.sqrt(number); i++) {
                if (number % i == 0) {
                    isPrime = false;
                    break;
                }
            }

            if (isPrime) {
                System.out.print(number + " ");
            }

            number++;
        }
    }
}


Question Twelve

public class SumOfOddNumbers {
    public static void main(String[] args) {
        int number = 1; 
        int sum = 0;   
        while (number <= 50) {
            if (number % 2 != 0) {
                sum += number;
            }
            number++;
        }

        System.out.println("The sum of odd numbers from 1 to 50 is: " + sum);
    }
}
