//# Pharmacy-Management-System
//Pharmacy Management System A Java-based app to manage pharmacy inventory &amp; sales. Features: medicine info storage, display, selling, restocking, and exit. User-friendly interface. //Benefits: efficient inventory management, easy sales tracking, and improved customer service.

import java.util.Scanner;

public class PharmacyManagementSystem {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        String[][] medicines = new String[20][3]; // array to store 20 medicines
        String contractName;
        String managerName;

        // initialize contract name and manager name
        System.out.println("Enter contract name: ");
        contractName = scanner.nextLine();
        System.out.println("Enter manager name: ");
        managerName = scanner.nextLine();

        // initialize medicines array
        for (int i = 0; i < 20; i++) {
            medicines[i][0] = "Medicine " + (i + 1); // medicine name
            medicines[i][1] = "10"; // quantity
            medicines[i][2] = "50"; // price
        }

        int choice;
        boolean exit = false;

        while (!exit) {
            System.out.println("Pharmacy Management System");
            System.out.println("Contract Name: " + contractName);
            System.out.println("Manager Name: " + managerName);
            System.out.println("1. Display Medicines");
            System.out.println("2. Sell Medicine");
            System.out.println("3. Restock Medicine");
            System.out.println("4. Exit");
            System.out.print("Enter your choice: ");

            choice = scanner.nextInt();

            switch (choice) {
                case 1:
                    System.out.println("Medicine Names\tQuantities\tPrices");
                    for (String[] medicine : medicines) {
                        System.out.println(medicine[0] + "\t\t" + medicine[1] + "\t\t" + medicine[2]);
                    }
                    break;
                case 2:
                    System.out.println("Sell Medicine");
                    // implement sell medicine logic here
                    break;
                case 3:
                    System.out.println("Restock Medicine");
                    // implement restock medicine logic here
                    break;
                case 4:
                    exit = true;
                    break;
                default:
                    System.out.println("Invalid choice. Please try again.");
            }
        }

        scanner.close();
    }
}




/* OUTPUT

Enter contract name: 
Enter manager name: 
Pharmacy Management System
Contract Name: LATHA PHARMACY PRODUCTS
Manager Name: KRITHVICK V.L.
1. Display Medicines
2. Sell Medicine
3. Restock Medicine
4. Exit
Enter your choice: Medicine Names	Quantities	Prices
Medicine 1		10		50
Medicine 2		10		50
Medicine 3		10		50
Medicine 4		10		50
Medicine 5		10		50
Medicine 6		10		50
Medicine 7		10		50
Medicine 8		10		50
Medicine 9		10		50
Medicine 10		10		50
Medicine 11		10		50
Medicine 12		10		50
Medicine 13		10		50
Medicine 14		10		50
Medicine 15		10		50
Medicine 16		10		50
Medicine 17		10		50
Medicine 18		10		50
Medicine 19		10		50
Medicine 20		10		50
Pharmacy Management System
Contract Name: LATHA PHARMACY PRODUCTS
Manager Name: KRITHVICK V.L.
1. Display Medicines
2. Sell Medicine
3. Restock Medicine
4. Exit
Enter your choice: Sell Medicine
Pharmacy Management System
Contract Name: LATHA PHARMACY PRODUCTS
Manager Name: KRITHVICK V.L.
1. Display Medicines
2. Sell Medicine
3. Restock Medicine
4. Exit
Enter your choice: Restock Medicine
Pharmacy Management System
Contract Name: LATHA PHARMACY PRODUCTS
Manager Name: KRITHVICK V.L.
1. Display Medicines
2. Sell Medicine
3. Restock Medicine
4. Exit
Enter your choice:
*/
