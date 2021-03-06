Постановка задачи
Разработать программу, реализующую алгоритм Диффи-Хелмана. 
Ход выполнения работы
1) Написание класса Main
2) Создание класса, реализующий алгоритм Диффи – Хеллмана (Deffi.java) :
	При работе алгоритма, каждая сторона:
1.	генерирует случайное натуральное число a — закрытый ключ
2.	совместно с удалённой стороной устанавливает открытые параметры p и g (обычно значения p и g генерируются на одной стороне и передаются другой), где:
p является случайным простым числом
g является первообразным корнем по модулю p
3.	вычисляет открытый ключ A, используя преобразование над закрытым ключом:
A = g^a mod p
4.	обменивается открытыми ключами с удалённой стороной
5.	вычисляет общий секретный ключ K, используя открытый ключ удаленной стороны B и свой закрытый ключ a:
K = B^a mod p

К получается равным с обоих сторон, потому что:
B^a mod p = (g^b mod p)^a mod p = g^ab mod p = (g^a mod p)^b mod p = A^b mod p

В практических реализациях, для a и b используются числа порядка 10^100 и p порядка 10^300. Число g не должно быть большим и обычно имеет значения 2 или 5.
Вывод
Разработана программа, реализующая алгоритм Диффи-Хеллмана. Программа работает корректно, закрытые ключи сходятся.
