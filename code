using System;

namespace Bineva_L_Loops{

    class Program
    {
        static void Main(string[] args)
        {
            Console.WriteLine("Hello! Welcome to the Credit Risk Calculator! Please input some data so we can help you manage your credit!");
            Console.WriteLine("Input your name");
            string user_name = Console.ReadLine();
            Console.WriteLine("Input the amount of money you want to take");
            var credit_amount = Console.ReadLine();
            double.TryParse(credit_amount, out double valid_credit);
            Console.WriteLine("Input the year in which you want to take the credit. This year should be between 2023 and 2000");
            var year = Console.ReadLine();
            int.TryParse(year, out int valid_year);
            General person = new General(user_name, valid_credit, valid_year);
            if(person.Credit_year == 1) 
            {
                Console.WriteLine("Your credit year is wrong ");
            }

            IDictionary<int, int> PD_values = new Dictionary<int, int>();
            PD_values.Add(2000, 50);
            PD_values.Add(2001, 40);

            //Console.WriteLine("tell us more about your credit history. Have you taken any credits before? Answer with a Yes or a No");
            //string answer = Console.ReadLine();
            //if (answer == "Yes" || answer == "yes")
            //{
            //    Past_Credit_LGD();
            //}
            //else if (answer == "No" || answer == "no")
            //{
            //    //method regarding no
            //}

            //double Past_Credit_LGD()
            //{
            //    double LGD_yes;
            //    Console.WriteLine("Tell us the year in which you took the credit. It has to be a year before the one you want to take the credit in");
            //    int past_credit_year = int.Parse(Console.ReadLine());
            //    if (past_credit_year < valid_year)
            //    {
            //        Console.WriteLine("How much money did you take back then");
            //        double past_credit = double.Parse(Console.ReadLine());
            //        Console.WriteLine("For how long did you pay the credit");
            //        int months_paid = int.Parse(Console.ReadLine());
            //        LGD_yes = (past_credit / months_paid) * (valid_year - past_credit_year);
            //    }
            //    else
            //    {
            //        while (past_credit_year >= valid_year)
            //        {
            //            Console.WriteLine("Please enter a valid year");
            //            var past_credit_year1 = Console.ReadLine();
            //            int.TryParse(past_credit_year1, out int past_credit_year_valid);
            //        }
            //        Console.WriteLine("How much money did you take back then");
            //        double past_credit = double.Parse(Console.ReadLine());
            //        Console.WriteLine("For how long did you pay the credit");
            //        int months_paid = int.Parse(Console.ReadLine());
            //        LGD_yes = (past_credit / months_paid) * (valid_year - past_credit_year);
            //    }
            //    return LGD_yes;
        }
    }
    class General
    {
        public string name { get; set; }
        public double credit { get; set; }

        public int credit_year;
        public int Credit_year
        {
            get
            {
                return credit_year;
            }
            set
            {
                if (credit_year > 2000 && credit_year <= 2023)
                {
                    Console.WriteLine("Your credit year is valid");
                    credit_year = value;
                }
                else
                {
                    Credit_year = -1;
                }
            }
        }
        //public int Incorrect()
        //{
        //    bool a = true;
        //    if (credit_year == -1)
        //    {
        //        a = false;
        //    }
        //    while (a == false)
        //    {
        //        Console.WriteLine("Your credit year is incorrect. Please enter a new one!");
        //        int new_year = int.Parse(Console.ReadLine());
        //        if (new_year > 2000 && new_year <= 2023)
        //        {
        //            a = true;
        //            return new_year;
        //        }
        //        return new_year;
        //    }
        //    return 0;
        //}
        public General(string user_name, double valid_credit, int valid_year)
        {
            this.name = user_name;
            this.credit = valid_credit;
            this.credit_year = valid_year;
        }
    }
    class Probability_Of_Default : General
    {
        public int year { get; set; }
        public int probability { get; set; }

        public Probability_Of_Default(string user_name, double valid_credit, int valid_year, int year, int probability) : base(user_name, valid_credit, valid_year)
        {
            this.year = year;
            this.probability = probability;
        }
    }
}

