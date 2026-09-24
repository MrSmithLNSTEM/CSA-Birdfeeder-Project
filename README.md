# Birdfeeder-Project
AP CSA Project: "Birdfeeder" [UNITS 1 &amp; 2 COVERED]


SHOW ALL YOUR WORK. REMEMBER THAT PROGRAM SEGMENTS ARE TO BE WRITTEN IN JAVA.
Assume that the classes listed in the Java Quick Reference have been imported where appropriate.
Unless otherwise noted in the question, assume that parameters in method calls are not null and that
methods are called only when their preconditions are satisfied.
In writing solutions for each question, you may use any of the accessible methods that are listed in
classes defined in that question. Writing significant amounts of code that can be replaced by a call to one
of these methods will not receive full credit.
This question simulates birds or possibly a bear eating at a bird feeder. The following Feeder class
contains information about how much food is in the bird feeder and simulates how much food is eaten.
You will write two methods of the Feeder class.

public class Feeder
{
/**
* The amount of food, in grams, currently in the bird feeder;
initialized in the constructor and
* always greater than or equal to zero
*/
private int currentFood;
/**
* Simulates one day with numBirds birds or possibly a bear at the
bird feeder,
* as described in part (a)
* Precondition: numBirds > 0
*/
public void simulateOneDay(int numBirds)
{ /* to be implemented in part (a) */ }
/**
* Returns the number of days birds or a bear found food to eat at
the feeder in this simulation,
* as described in part (b)
* Preconditions: numBirds > 0, numDays > 0
*/
public int simulateManyDays(int numBirds, int numDays)
{ /* to be implemented in part (b) */ }
// There may be instance variables, constructors, or methods that
are not shown.
}

(a) Write the simulateOneDay method, which simulates numBirds birds or possibly a bear at the
feeder for one day. The method determines the amount of food taken from the feeder on this day and
updates the currentFood instance variable. The simulation accounts for normal conditions, which
occur 95% of the time, and abnormal conditions, which occur 5% of the time.

Under normal conditions, the simulation assumes that on any given day, only birds visit the feeder and
that each bird at the feeder consumes the same amount of food. This standard amount consumed is
between 10 and 50 grams of food, inclusive, in 1-gram increments. That is, on any given day, each bird
might eat 10, 11, . . . , 49, or 50 grams of food. The amount of food eaten by each bird on a given day is
randomly generated and each integer from 10 to 50, inclusive, has an equal chance of being chosen.
For example, a run of the simulation might predict that for a certain day under normal conditions, each
bird coming to the feeder will eat 11 grams of food. If 10 birds come to the feeder on that day, then a
total of 110 grams of food will be consumed.
If the simulated food consumed is greater than the amount of food in the feeder, the birds empty the
feeder and the amount of food in the feeder at the end of the day is zero.
Under abnormal conditions, a bear empties the feeder and the amount of food in the feeder at the end of
the day is zero.
The following examples show possible results of three calls to simulateOneDay.

Example 1: If the feeder initially contains 500 grams of food, the call simulateOneDay(12) could
result in 12 birds eating 20 grams of food each, leaving 260 grams of food in the feeder.

Example 2: If the feeder initially contains 1,000 grams of food, the call simulateOneDay(22) could
result in a bear eating all the food, leaving 0 grams of food in the feeder.

Example 3: If the feeder initially contains 100 grams of food, the call simulateOneDay(5) could
result in 5 birds attempting to eat 30 grams of food each. Since the feeder initially contains less than 150
grams of food, the feeder is emptied, leaving 0 grams of food in the feeder.

Complete the simulateOneDay method.
/**
* Simulates one day with numBirds birds or possibly a bear at the
bird feeder,
* as described in part (a)
* Precondition: numBirds > 0
*/
public void simulateOneDay(int numBirds)
