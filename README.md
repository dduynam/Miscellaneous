# Variable-Size-Array
an excercise in Hackerrank
int main()
{
	int num;
	cout << "Nhap so phan tu ";
	cin >> num;
	vector <vector<int>> arr;
	arr.resize(num);
	for (int i = 0; i < num; i++)
	{
		int index;
		cout << "Nhap so phan tu mang ";
		cin >> index;
		arr[i].resize(index);
		for (int j = 0; j < index; j++)
		{
			cin >> arr[i][j];
		}
	}
	for (int i = 0; i < num; i++)
	{
		for (int j = 0; j < arr[i].size(); j++)
		{
			cout << arr[i][j] << " ";
		}
		cout << endl;
	}
	int _num, _idx;

	int Ri;
	do {
	cout << "Nhap so mang tham chieu: ";
	cin >> Ri;
	} while (Ri > num);
	
	for (int i = 0; i < Ri; i++)
	{
		do {
			cout << "Nhap mang con tham chieu: ";
			cin >> _num;
		} while (_num > num);

		do {
			cout << "Nhap phan tu mang tham chieu: ";
			cin >> _idx;
		} while (_idx > arr[_num].size());

		cout << "Ketqua " << arr[_num][_idx] << endl;
	}
	

	return 0;
}
