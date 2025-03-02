# lab1-insurance-policy

package assignments;

public class auto {

private String firstName;

private String lastName;

private String make;

private String model;

private double liability;

private double collision;

private double commission;

public auto(String firstName, String lastName, String make, String model, double liability, double collision) {

this.firstName = firstName;

this.lastName = lastName;

this.make = make;

this.model = model;

this.liability = liability;

this.collision = collision;

}


public void computeCommission() {

commission = (liability + collision) * 0.30;

}

public String toString() {

return "Auto Policy\n-----------\nName: " + firstName + " " + lastName +

"\nMake: " + make + "\nModel: " + model +

"\nLiability: $" + String.format("%.2f", liability) +

"\nCollision: $" + String.format("%.2f", collision) +

"\nCommission: $" + String.format("%.2f", commission) + "\n";

}

}

this is home portion

package assignments;

public class home {

private String firstName;

private String lastName;

private int footage;

private double dwelling;

private double contents;

private double liability;

private double commission;

public home() {}

public void setFirstName(String firstName) { this.firstName = firstName; }

public void setLastName(String lastName) { this.lastName = lastName; }

public void setFootage(int footage) { this.footage = footage; }

public void setDwelling(double dwelling) { this.dwelling = dwelling; }

public void setContents(double contents) { this.contents = contents; }

public void setLiability(double liability) { this.liability = liability; }

public void computeCommission() {

commission = (liability * 0.30) + ((dwelling + contents) * 0.20);

}

public String toString() {

return "Home Policy\n-----------\nName: " + firstName + " " + lastName +

"\nFootage: " + footage +

"\nDwelling: $" + String.format("%.2f", dwelling) +

"\nContents: $" + String.format("%.2f", contents) +

"\nLiability: $" + String.format("%.2f", liability) +

"\nCommission: $" + String.format("%.2f", commission) + "\n";

}

}

this is life insurance

package assignments;

public class life {

private String firstName;

private String lastName;

private int age;

private double term;

private double commission;

public life(String firstName, String lastName, int age, double term) {

this.firstName = firstName;

this.lastName = lastName;

this.age = age;

this.term = term;

}

public void computeCommission() {

commission = term * 0.20;

}

public String getFirstName() { return firstName; }

public String getLastName() { return lastName; }

public int getAge() { return age; }

public double getTerm() { return term; }

public String toString() {

return "Life Policy\n-----------\nName: " + firstName + " " + lastName +

"\nAge: " + age +

"\nTerm: $" + String.format("%.2f", term) +

"\nCommission: $" + String.format("%.2f", commission) + "\n";

}

}


package assignments;

public class test {

public static void main(String[] args) {

// Create and set an Auto policy object

auto a = new auto("Jerry", "Seinfed", "Chevy", "Malibu", 10000.0, 50000.0);

a.computeCommission();

System.out.println(a);

// Create and set a Home policy object

home h = new home();

h.setFirstName("Elaine");

h.setLastName("Benes");

h.setFootage(4000);

h.setDwelling(32000);

h.setContents(5000);

h.setLiability(10000);

h.computeCommission();

System.out.println(h);

// Create and set a Life policy object

life l = new life("Cosmo", "Kramer", 35, 50000);

l.computeCommission();

System.out.println(l);

// Test getters

System.out.println("Get life firstName: " + l.getFirstName());

System.out.println("Get life lastName: " + l.getLastName());

System.out.println("Get life age: " + l.getAge());

System.out.println("Get life term: " + l.getTerm());

}

}
