# Gleb Kuzmin
## cv

### Contact Info
**phone:** +7-916-251-40-83
**email:** kuzmingn@mail.ru

### Summary
our goal, wishes, reveal what is important for you, what do you want and why.
Some kind of self-presentation. In case of lack of experience  Junior Developer sells his/her potential, his/her passion and ability to learn fast. You shouldn't think that everybody is going to teach you when you come to the workplace . Rather being a Junior means always
learning new things from everywhere etc.

### Skills 
- Programming languages:
  - R 
  - PHP 
  - C# 
- Database:
  - SQL
  - Postgres
  - MySQL
  - Postgres 
- Web:
  - HTML
  - CSS
- Version control:
  - GitHub 
- Other:
  - Google Spreadshhets
  - Microsoft Excel
  - TeX

### Code examples 

```csharp
using System;
					
public class Program
{
	public static void Main()
	{
		int n = Int32.Parse(Console.ReadLine());
            string line;
            bool[,] matrix = new bool[n,n];
            int[,] min_way = new int[n,n];
            string[,] min_path = new string[n,n];
            for (int i=0; i < n; i++)
            {
                line = Console.ReadLine();
                string[] row = line.Split(' ');
                for (int j=0; j < n; j++)
                {
                    if (row[j] == "1") 
                    {
                        matrix[i, j] = true;
                        min_way[i, j] = 1;
						if (i == j) {min_path[i, j] = (i+1).ToString();}
                        else {min_path[i, j] = (i+1) + " " + (j+1);}
                    }
                    else
                    {
                        matrix[i, j] = false;
                        min_way[i, j] = -1;
                        min_path[i, j] = "";
                    }
                }
            }
            
		int cur_way = 0;
		string cur_path = "";
		for (int k=0; k<n; k++)
		{
			for (int i=0; i < n; i++)
            {
                for (int j=0; j < n; j++)
                {
					if (min_way[i,j]>0)
					{
						cur_way = min_way[i,j];
						cur_path = min_path[i,j];
						for (int l=0; l<n; l++)
						{
							if (matrix[j,l])
							{
								if (((cur_way + 1) < min_way[i,l]) || (min_way[i,l] == -1))
								{
									min_way[i,l] = cur_way + 1;
									min_path[i,l] = cur_path + " " + (l+1);
								}
							}
						}
					}
				}
			}
		}
				
            string input = Console.ReadLine();
            string[] nums = input.Split(' ');
            int start = Int32.Parse(nums[0]);
            int finish = Int32.Parse(nums[1]); 

            Console.WriteLine(min_way[start-1, finish-1]);
            if (min_way[start-1, finish-1] > 0) {
                Console.WriteLine(min_path[start-1, finish-1]);
            }
	}
}
```


### Experience 
(for a Junior Dev it means all kinds of experience: coding tests, projects from courses,
freelance projects - wherever they had the opportunity to demonstrate skills they have.
Also it would be awesome if you add links to source code)

### Education 
__HSE__ _2018_ Data culture. Lecture  
__HSE__ _2015_ Econometrics. Online course  
__Specialist__ _2014_ Creating an effective presentations in  Microsoft PowerPoint. Course  
__HSE__ _2012_  English cources Upper-Intermidiate level. Course  
__PM Expert__ _2011_ Basic course of PMI PMBOK Guide 4th edition Управление проектами. Course  
__Mashav, Israel__ _2010_ Management of Higher Education,  Science and Innovations. Course  
__Moscow Aviation Institute__ _2007_ Applied mathematics. Degree

### English 
__UNIDO, Veinna, Austria__ _2019_ Internship. Work with international colleagues. Working language: English
