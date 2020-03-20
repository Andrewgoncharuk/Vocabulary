# Vocabulary
Exam C#
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;


namespace Vocabulary
{

    class Program
    {
        class Word
        {
            public string name;
            public string[] meanings;
            public string show()
            {
                string b = meanings[0];
                for(int i =1; i<meanings.Length;i++) 
                { 
                    b +=", " + meanings[i]; 
                }
                return b;
            }
        }
        public void showMenu()
        {
            Console.WriteLine("Выберите один из пунктов меню:");
            Console.WriteLine("Создать новый словарь                - 1");
            Console.WriteLine("Добавить слово в словарь             - 2");
            Console.WriteLine("Удалить слово или перевод из словаря - 3");
            Console.WriteLine("Редактировать слово или перевод      - 4");
            Console.WriteLine("Найти перевод слова                  - 5");
        }
        static void Main(string[] args)
        {
            
            int caseMenu = 0;

            switch (caseMenu)
            {
                case 1:
                    Console.WriteLine("Case 1");
                    break;
                case 2:
                    Console.WriteLine("Case 2");
                    break;
                case 3:
                    Console.WriteLine("Case 2");
                    break;
                case 4:
                    Console.WriteLine("Case 2");
                    break;
                case 5:
                    Console.WriteLine("Case 2");
                    break;
                default:
                    Console.WriteLine("Default case");
                    break;
            }
            Dictionary<string, Word> dic1 = new Dictionary<string, Word>();
            Word word1 = new Word();
            word1.name = "sale";
            word1.meanings = new string[] { "meaning1", "meaning2"};
            dic1.Add(word1.name, word1);
            

            foreach (var pair in dic1)
            {
                Console.WriteLine("{0} - {1}", pair.Key, pair.Value.show());
            }

        }
    }
}
