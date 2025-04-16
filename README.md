# Бинарное дерево поиска (CTree)

## Общее описание

Программа представляет собой реализацию шаблонного класса `CTree` (бинарное дерево поиска), который хранит элементы с ключами типа `const char*` и значениями произвольного типа `T`. Класс поддерживает основные операции: добавление, удаление, поиск, обход элементов, а также слияние и разделение деревьев.


## Основные методы

### Работа с узлами
- **`Add(const char* key, const T &v)`**:
  - Добавляет новый узел с ключом `key` и значением `v` в дерево.
  - Возвращает `true` при успешном добавлении, `false` если ключ уже существует.

- **`Delete(const char* key)`**:
  - Удаляет узел с указанным ключом.
  - Возвращает `true` если узел не найден, `false` при успешном удалении.

- **`Find(const char* key)`**:
  - Возвращает указатель на узел с заданным ключом или `NULL`, если узел не найден.

### Обход дерева
- **`begin()`**, **`end()`**:
  - Возвращают итераторы для обхода дерева от минимального до максимального ключа.
- **`Next(CNode* n)`**:
  - Возвращает указатель на следующий узел в порядке обхода.

### Слияние и разделение
- **`MergingTree(CTree &rhs)`**:
  - Сливает текущее дерево с деревом `rhs`, используя минимальный элемент `rhs` как корень нового дерева.
- **`MergingTree(CTree &rhs, CNode* v)`**:
  - Сливает деревья, используя узел `v` как корень нового дерева.
