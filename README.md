# income-calc
// Ivanna Giordano, COP2805, Advanced Java
// this code helps you list the income that would be earned based on the sales amount 

package COP2805;

public class Homework1 {

    public static void main(String[] args) {
        System.out.println("Sales            \t\tIncome");
       
        for (double salesAmount = 1000; salesAmount <= 20000; salesAmount += 1000) {
            double totalIncome = computeIncome(salesAmount);
            System.out.printf("$%.2f\t\t\t$%.2f\n", salesAmount, totalIncome);
        }
    }

    public static double computeIncome(double salesAmount) {
        double baseSalary = 5000;
        double commission = 0;

        if (salesAmount <= 5000) {
            commission = salesAmount * 0.08;
        } else if (salesAmount <= 10000) {
            commission = 5000 * 0.08 + (salesAmount - 5000) * 0.10;
        } else {
            commission = 5000 * 0.08 + 5000 * 0.10 + (salesAmount - 10000) * 0.12;
        }

        return baseSalary + commission;
    }
}
