int main() 
{
  int countRows = 0;
	std::cin >> countRows;

	int **table = new (std::nothrow) int*[countRows];
	if (!table) 
	{
		std::cout << "failed to allocate table";
		return 0;
	}

	int countColumns = 0;
	std::cin >> countColumns;
	for (int rows = 0; rows < countRows; rows++)
	{
		table[rows] = new (std::nothrow) int[countColumns];
		if (!table[rows])
		{
			std::cout << "Failed to allocate table row";
			for (int i = 0; i < rows; i++) {
				delete[] table[i];
			}
			delete[] table;
			return 0;
		}
		for (int columns = 0; columns < countColumns; columns++)
			std::cin >> table[rows][columns];

	}
	for (int rows = 0; rows < countRows; rows++)
	{
		for (int columns = 0; columns < countColumns; columns++)
			std::cout << table[rows][columns] << " ";
	}
	std::cout << "\n";

	for (int i = 0; i < countRows; i++)
		delete[] table[i];
	delete[] table;

	return 0;
}
