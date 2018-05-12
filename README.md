#include <iostream>
#include <fstream>
using namespace std;
 
int main()
{
    setlocale(LC_ALL,"Russian");
    int n, mark_math, mark_progr, mark_phys;
    char fam[50],name[50];
    cout << ":::::::::::::::::";
    cout << "\n::Запись в файл::";
    cout << "\n:::::::::::::::::\n\n";
    cout << "Количество студентов: ";
    cin >> n;
     float kol = 0;
     float sum=0; 
     float k = n;
    ofstream fout("students.txt");
    for(int i=0;i<n;i++)
    {
    	cout << "Введите имя: ";
    	cin >> name;
    	fout << name << " ";
        cout << "Введите фамилия: ";
        cin >> fam;
        fout << fam <<" ";
        cout << "Математика: ";
        cin >> mark_math;
        fout << mark_math <<" ";
        cout << "Программирование: ";
        cin >> mark_progr;
        fout << mark_progr <<" ";
        cout << "Физика: ";
        cin >> mark_phys;
        fout << mark_phys<<endl <<" ";
        cout << "\nЗаписано\n\n";
         if(mark_phys != 2)
        {
        	kol ++;
		}
    }
    fout << "Количество студентов не имеющий 2 по физике: " << kol <<endl;
for(int i=0;i<n;i++){ 
	sum +=mark_math+mark_progr+mark_phys; 
} 
float kolvo = k * 3; 
float sredball = sum / kolvo; 
fout << "Средний балл всех студентов: " << sredball;
system("pause");
return 0;
}
