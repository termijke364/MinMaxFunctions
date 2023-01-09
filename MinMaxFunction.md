#include <iostream>

using namespace std;
const int arrsize = 10;
void CrMassive(int arr[])
{
	for (int i = 0; i < arrsize; i++)
		arr[i] = rand() % 100 + 20;
}
void MinimunArr(int min, int arr[])
{
	min = arr[0];
	int l{};
	for (int i = 0; i < arrsize; i++)
	{
		if (min > arr[i])
		{
			min = arr[i];
			l = i;
		}
	}
	cout << "Минимальное значение:  " << min << endl;
	cout << "Индекс минимального значения: " << l + 1 << endl;
}

void MaximumArr(int max, int arr[])
{
	max = arr[0];
	int k{};
	for (int i = 0; i < arrsize; i++)
	{
		if (max < arr[i])
		{
			max = arr[i];
			k = i;
		}
	}
	cout << "Максимальное значение:  " << max << endl;
	cout << "Индекс максимального значения: " << k + 1 << endl;
}

int main()
{
	setlocale(0, "");
	srand(time(NULL));

	cout << "Минимальное и максимально значение в одномерном массиве" << endl;

	int arr[arrsize]{};

	CrMassive(arr);

	cout << endl;

	for (int i = 0; i < arrsize; i++)
		cout << arr[i] << "\t";
	cout << endl;

	int min{}, max{}, k{}, l{};

	MinimunArr(min, arr);
	MaximumArr(max, arr);

	return 0;
  }
