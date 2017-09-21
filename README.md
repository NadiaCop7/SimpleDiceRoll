# SimpleDiceRoll
//class project Dice Roll

using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace AssessmentNotes
{
    class Program
    {
        static Random rnd = new Random();
        static int userScore = 0;
        static int compScore = 0;
        static void Main(string[] args)
        {

 int winningScore = 20;
            Console.WriteLine("Lets roll some dice! Whoever rolls to " + winningScore + " wins!");

            while (userScore < winningScore && compScore < winningScore)
            {
                Console.WriteLine("Hit ENTER to roll");
                Console.ReadLine();
                Console.WriteLine("User's roll:" + diceRoll("user"));
                Console.WriteLine("Computer's roll:" + diceRoll("computer"));
            }
            if (userScore >= winningScore) {
                Console.WriteLine("User wins with a score of: " + userScore + " to " + compScore); 
            }
            else
                Console.WriteLine("User wins with a score of: " + compScore + " to " + userScore);
            Console.ReadLine();
                
        }

        static int diceRoll(string player)
        {
            int roll = rnd.Next(2, 13);

            if (player == "user")
            {
                userScore += roll;
            }

            else
                compScore += roll;

            return roll;    
        }
                
                

        

            
            
            
               
    }
}
