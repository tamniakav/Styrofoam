using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Exam2
{
    class Exam2
    {
        static void Main(string[] args)
        {
            double budget = double.Parse(Console.ReadLine());
            double area = double.Parse(Console.ReadLine());
            int windols = int.Parse(Console.ReadLine());
            double styrofoam = double.Parse(Console.ReadLine());
            double price = double.Parse(Console.ReadLine());

            area = area - (windols * 2.4);
            area = area + (area * 0.1);

            double neededPack = area / styrofoam;
            neededPack = Math.Ceiling(neededPack);
            double moneyNeed = neededPack * price;

            double money = budget - moneyNeed;
            money = Math.Abs(money);

            if (budget > moneyNeed)
            {
                Console.WriteLine("Spent: {0:f2}", moneyNeed);
                Console.WriteLine("Left: {0:f2}", money);
            }
            else
            {
                Console.WriteLine("Need more: {0:f2}", money);
            }
        }
    }
}
