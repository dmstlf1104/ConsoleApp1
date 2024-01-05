using System;

class Program
{
    static void Main()
    {
        int numberOfTries = 0;
        bool isNumberGuessed = false;

        Console.WriteLine("스파르타 마을에 오신 여러분 환영합니다.\r\n이곳에서 던전으로 들어가기전 활동을 할 수 있습니다.");

        while (!isNumberGuessed)
        {
            Console.WriteLine("\r\n1. 상태보기");
            Console.WriteLine("2. 인벤토리");
            Console.WriteLine("3. 상점");
            Console.Write("\r\n원하시는 행동을 입력해 주세요: ");

            string userInput = Console.ReadLine();

            int userChoice;
            if (int.TryParse(userInput, out userChoice))
            {
                if (userChoice >= 1 && userChoice <= 3)
                {
                    // 사용자의 선택에 따라 원하는 작업을 수행합니다.
                    switch (userChoice)
                    {
                        case 1:
                            Console.WriteLine("\r\n상태보기");
                            Console.WriteLine("캐릭터의 정보가 표시 됩니다.");
                            Console.WriteLine("\r\nLv. 01");
                            Console.WriteLine("Chad ( 전사 )");
                            Console.WriteLine("공격력 : 10)");
                            Console.WriteLine("방여력 : 5");
                            Console.WriteLine("체 력 : 100");
                            Console.WriteLine("Gold : 1500G");
                            Console.Write("\r\n0. 나가기");
                            break;
                        case 2:
                            Console.WriteLine("\r\n인벤토리");
                            Console.WriteLine("보유 중인 아이템을 관리할 수 있습니다.");
                            Console.WriteLine("\r\n[아이템 목록]");
                            Console.WriteLine("\r\n1. 장착 관리");
                            Console.WriteLine("0. 나가기");
                            break;
                        case 3:
                            Console.WriteLine("\r\n상점");
                            Console.WriteLine("필요한 아이템을 얻을 수 있는 상점입니다.");
                            Console.WriteLine("\r\n[보유 골드]");
                            Console.WriteLine("800 G");
                            Console.WriteLine("\r\n[아이템 목록]");
                            Console.WriteLine("- 수련자 갑옷    | 방어력 +5  | 수련에 도움을 주는 갑옷입니다.             |  1000 G");
                            Console.WriteLine("- 무쇠갑옷       | 방어력 +9  | 무쇠로 만들어져 튼튼한 갑옷입니다.         |  구매완료");
                            Console.WriteLine("- 스파르타의 갑옷 | 방어력 +15 | 스파르타의 전사들이 사용했다는 전설의 갑옷입니다.|  3500 G");
                            Console.WriteLine("- 청동 도끼     | 공격력 +5  |  어디선가 사용됐던거 같은 도끼입니다.        |  1500 G");
                            Console.WriteLine("- 스파르타의 창  | 공격력 +7  | 스파르타의 전사들이 사용했다는 전설의 창입니다. |  구매완료");

                            Console.WriteLine("\r\n1. 아이템 구매");
                            Console.WriteLine("0. 나가기");
                            break;
                    }
                    // 사용자가 선택지를 볼 수 있도록 isNumberGuessed를 false로 다시 설정합니다.
                    isNumberGuessed = false;
                }
                else
                {
                    Console.WriteLine("1부터 3 사이의 번호를 입력해주세요.");
                }
            }
            else
            {
                Console.WriteLine("잘못된 입력입니다. 숫자를 입력해주세요.");
            }
        }
    }
}
