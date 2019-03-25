```C#
// Mark Byers

/*
 * You must design a database application that is to keep track of inventory items. You may use any standard C# programming language feature to complete the project.

The program must be able to complete the following tasks:

Add an item
Change an item (by giving its item number not array index). You should be able to change all field values except the item number.
Delete an item (by giving its item number not array index)
List all items in the database
Quit
The database must be able to hold at least 10 items and at most 100 items.

No file I/O is necessary.

No fancy screen I/O is necessary (just System.Console functionality).

Each item must have the following information associated with it (Hint: A array of structs might work well here.):

Item # (string such as ABC101)
Description
Price per item
Quantity on hand
Our cost per item
Value of item (price * quantity on hand)
The program should have some sort of menu to select which option and display the results to the screen.
*/

// Write a program to keep track of some inventory items as shown below.
// Hint: when creating arrays, as you get or read items into
// your array, then initialize each array spot before its use
// and place a counter or use your own Mylength to keep track
// of your array length as it is used.

using System;

struct ItemData
{
    public int ItemNumber;
    public string Description;
    public double PricePerItem;
    public int QuantityOnHand;
    public double OurCostPerItem;
    public double ValueOfItem;
}

class Program
{
    public static void Main()
    {
        var items = new ItemData[100]; // Construct the ItemData class with proper initialization
        var countOfItems = items.Length; // Total items in database
        int itemNumber = 0;
        items[itemNumber].ItemNumber = countOfItems - 1; // last item as the current one

        // use an interger to keep track of the count of items in your inventory                    
        // create an array of your ItemData struct
        // use a never ending loop that shows the user what options they can select 
        // as long as no one Quits, continue the inventory update
        // in that loop, show what user can select from the list
        // read the user's input and then create what case it falls

        Console.WriteLine("This application is a repository of inventory items. The database application keeps track of inventory items ");
        Console.WriteLine("Please select one of the choices below by entering the corresponding option number.");
        Console.Write("1. Add an Item | 2. Change an Item | 3. Delete an Item | 4. List all Items | 5. Quit");
        string strx = Console.ReadLine(); // read user's input    

        var optx = int.Parse(strx); // convert the given string to integer to match our case types shown below
        var numberOfItems = 0; 
        Console.WriteLine(); // provide an extra blank line on screen

        switch (optx)
        {
            case 1: // add an item to the list if this option is selected
                {
                    itemNumber = numberOfItems;
                    Console.Write("Item Description :");
                    var description = Console.ReadLine();
                    Console.Write("Item Price :");
                    var price_ = Console.ReadLine();
                    var price = double.Parse(price_);
                    Console.Write("Item Quantity :");
                    var quantity = Console.ReadLine();
                    var qty = int.Parse(quantity);
                    Console.Write("Item Cost :");
                    var cost_ = Console.ReadLine();
                    var cost = double.Parse(cost_);
                    double value = price * qty;

                    items[itemNumber].Description = description;
                    items[itemNumber].PricePerItem = price;
                    items[itemNumber].QuantityOnHand = qty;
                    items[itemNumber].OurCostPerItem = cost;
                    items[itemNumber].ValueOfItem = value;

                    numberOfItems++;
                    itemNumber = 0;
                    break;
                }

            case 2: //change items in the list if this option is selected
                {
                    Console.Write("Please enter an item ID No:");
                    string input = Console.ReadLine();
                    int changeItemNumber = int.Parse(input);
                    bool fFound = false;

                    for (int x = 0; x < countOfItems; x++)
                    {
                        if (items[x].ItemNumber == changeItemNumber)
                        {
                            fFound = true;
                            // code to show what has to happen if the item in the list is found
                            // reset the count to show a new count for your list 
                            // (Note: your list is now increased by one item)
                        }
                    }

                    if (!fFound) // and if not found
                    {
                        Console.WriteLine("Item {0} not found", changeItemNumber);
                    }

                    break;
                }

            case 3: //delete items in the list if this option is selected
                {
                    Console.Write("Please enter an item ID No:");
                    string input = Console.ReadLine();
                    int deleteItemNumber = int.Parse(input);
                    bool deleted = false;

                    for (int x = 0; x < countOfItems; x++)
                    {
                        if (items[x].ItemNumber == deleteItemNumber)
                        {
                            deleted = true;
                            // delete the item if you found it
                            // reset the count to show a new count for your list 
                            // (Note: your list is now reduced by one item)                              
                        }
                    }

                    if (deleted) // hint the user that you deleted the requested item
                    {
                        Console.WriteLine("Item deleted");
                    }
                    else // if did not find it, hint the user that you did not find it in your list
                    {
                        Console.WriteLine("Item {0} not found", deleteItemNumber);
                    }

                    break;
                }

            case 4:  //list all items in current database if this option is selected
                {
                    //Console.WriteLine("Item#  ItemID  Description           Price  QOH  Cost  Value");
                    Console.WriteLine("{0,-5} {1,5} {2,-10} {3,-10} {4,-4} {5,-10} {6,-10}","Item#", "ItemID", "Description", "Price", "QTY", "Cost", "Value");
                    Console.WriteLine(""); // Insert 1 blank line

                    // code in this block. Use the above line format as a guide for printing or displaying the items in your list right under it
                    for (int index = 0; index < numberOfItems; index++)
                    {
                        Console.WriteLine("{0,-5} {1,5} {2,-10} {3,-10:C} {4,-4} {5,-10:C} {6,-10:C}", index + 1, items[numberOfItems].ItemNumber, items[numberOfItems].Description, items[numberOfItems].PricePerItem, items[numberOfItems].QuantityOnHand, items[numberOfItems].OurCostPerItem, items[numberOfItems].ValueOfItem);
                    }

                    break;
                }


            case 5: //quit the program if this option is selected
                {
                    Console.Write("Are you sure that you want to quit(y/n)?");
                    string input = Console.ReadLine();

                    if ((input == "N") || (input == "n"))
                    {
                        optx = 0; //as long as it is not 5, the process is not breaking   
                    }
                    break;
                }

            default:
                {
                    Console.Write("Invalid Option, try again");
                    break;
                }
        }
    }
}
```
