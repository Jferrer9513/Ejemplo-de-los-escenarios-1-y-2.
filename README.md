public class MathUtils {

    /**
     * Determines whether a number is even or odd without using conditional statements.
     * @param number The integer to check.
     * @return "even" if the number is even, "odd" otherwise.
     */
    public static String checkEvenOdd(int number) {
        String[] result = {"even", "odd"};
        return result[number % 2];
    }

    /**
     * Determines whether a number is prime.
     * @param number The integer to check (must be >= 2 and <= 2000000).
     * @return "prime" if the number is prime, "not prime" otherwise.
     */
    public static String checkPrime(int number) {
        if (number < 2) return "not prime";
        if (number == 2) return "prime";
        if (number % 2 == 0) return "not prime";

        for (int i = 3; i * i <= number; i += 2) {
            if (number % i == 0) {
                return "not prime";
            }
        }
        return "prime";
    }

    public static void main(String[] args) {
        // Example usage with number 17
        int testNumber = 17;

        System.out.println("The number " + testNumber + " is " + checkEvenOdd(testNumber));
        System.out.println("The number " + testNumber + " is " + checkPrime(testNumber));
    }
}
