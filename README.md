using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
namespace Excercise
{
    internal class Program
    {
        static void Ex1()
        {
            Console.WriteLine("Tinh tong");
            float a, b, sum;
            Console.WriteLine("Nhap so a:");
            float.TryParse(Console.ReadLine(), out a);
            Console.WriteLine("Nhap so b:");
            float.TryParse(Console.ReadLine(), out b);

            sum = a + b;

            Console.WriteLine("sum = " + sum);
        }
        static void ex2()
        {
            int a, b, c;
            Console.WriteLine("Nhap so a:");
            int.TryParse(Console.ReadLine(), out a);
            Console.WriteLine("Nhap so b:");
            int.TryParse(Console.ReadLine(), out b);
            c = a;
            a = b;
            b = c;
            Console.WriteLine("Da hoan doi:");
            Console.WriteLine("a = " + a);
            Console.WriteLine("b = " + b);
        }
        static void ex3()
        {
            float a, b, mul;
            Console.WriteLine("Nhap so a:");
            float.TryParse(Console.ReadLine(), out a);
            Console.WriteLine("Nhap so b:");
            float.TryParse(Console.ReadLine(), out b);
            mul = a * b;
            Console.WriteLine("mul = " + mul);
        }
        static void ex4()
        {
            float feet, met;
            Console.WriteLine("Nhap so feet:");
            float.TryParse(Console.ReadLine(), out feet);
            met = feet * 0.3048f; // 1 feet = 0.3048 meters 
            Console.WriteLine("Chuyen doi sang met: " + met);
        }
        static void ex5()
        {
            float C, F;
            Console.WriteLine("Chon kieu chuyen doi");
            Console.WriteLine("1. C -> F");
            Console.WriteLine("2. F -> C");
            Console.WriteLine("Nhap lua chon cua ban(1 hoac 2):");
            int choice;
            int.TryParse(Console.ReadLine(), out choice);
            if (choice == 1)
            {
                Console.WriteLine("Nhap nhiet do C:");
                float.TryParse(Console.ReadLine(), out C);
                F = C * 9f / 5f + 32f;
                Console.WriteLine($"{C} °C = {F} °F");
            }
            else if (choice == 2)
            {
                Console.WriteLine("Nhap nhiet do F:");
                float.TryParse(Console.ReadLine(), out F);
                C = (F - 32f) * 5f / 9f;
                Console.WriteLine($"{F} °F = {C} °C");
            }
            else
            {
                Console.WriteLine("Lua chon khong hop le.");
            }
        }
        static void ex6()
        {
            Console.WriteLine(" Size of data type");
            Console.WriteLine("int: {0} byte ", sizeof(int));
            Console.WriteLine("float: {0} byte ", sizeof(float));
            Console.WriteLine("double: {0} byte ", sizeof(double));
            Console.WriteLine("char: {0} byte ", sizeof(char));
            Console.WriteLine("bool: {0} byte ", sizeof(bool));
            Console.WriteLine("long: {0} byte ", sizeof(long));
            Console.WriteLine("short: {0} byte ", sizeof(short));
            Console.WriteLine("decimal: {0} byte ", sizeof(decimal));
        }
        static void ex7()
        {
            Console.OutputEncoding = Encoding.UTF8;
            Console.WriteLine("Nhap mot ki tu: ");
            char kitu = Console.ReadKey().KeyChar;
            Console.WriteLine(); // Để xuống dòng sau khi nhập ký tự 
            int ascii = (int)kitu;
            Console.WriteLine($"Kí tự {kitu} chuyển đổi sang ascii là:{ascii}");
        }
        static void ex8()
        {
            float r, S;
            Console.WriteLine("Nhap ban kinh r:");
            r = float.Parse(Console.ReadLine());
            float pi = 3.14f;
            S = pi * r * r;
            Console.WriteLine("dien tich hinh tron:" + S);
        }
        static void ex9()
        {
            float r, S;
            Console.WriteLine("nhap canh hinh vuong r");
            r = float.Parse(Console.ReadLine());
            S = r * r;
            Console.WriteLine("dien tich hinh vuong: " + S);
        }
        static void ex10()
        {
            Console.OutputEncoding = Encoding.UTF8;
            int ngay, thang, nam, ngaynhap;
            Console.WriteLine("Nhập ngày để chuyển đổi :");
            ngaynhap = int.Parse(Console.ReadLine());
            nam = ngaynhap / 365;
            thang = (ngaynhap % 365) / 30;
            ngay = (ngaynhap % 365) % 30;
            Console.WriteLine($"{ngaynhap} ngày= {nam} năm,{thang} tháng,{ngay} ngày");
        }
        static void Main(string[] args)
        {
            Console.WriteLine("Bai tap 1: ");
            Ex1();
            Console.WriteLine("Bai tap 2: ");
            ex2();
            Console.WriteLine("Bai tap 3: ");
            ex3();
            Console.ReadKey();
            Console.WriteLine("Bai tap 4: ");
            ex4();
            Console.WriteLine("Bai tap 5: ");
            ex5();
            Console.WriteLine("Bai tap 6: ");
            ex6();
            Console.WriteLine("Bai tap 7: ");
            ex7();
            Console.WriteLine("Bai tap 8: ");
            ex8();
            Console.WriteLine("Bai tap 9: ");
            ex9();
            Console.WriteLine("Bai tap 10: ");
            ex10();
        }
    }
}
