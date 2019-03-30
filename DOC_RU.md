# класс DiffUtils

- procedure Insert(i:integer;elem:T) - добавляет элемент по  индексу и значению
- procedure AddElem(elem:T) - добавляет элемент по значению в конец списка
- procedure Remove(index:integer) - удаляет элемент из списка по индексу
- procedure Clear() - удаляет все элементы из списка
- procedure GoBack() - удаляет последнее изменение (из истории)
- procedure GoForward() - повторяет поледнее удалённое изменение из истории
- procedure ClearHistory() - удаляет все записи из истории
- property HistoryCountBack - возвращает количество записей в истории до данного состояния
- property History - Возвращает полную историю изменений
- property HistoryCountForward - Возвращает количество записей в истории после текущего состояния
- property Items - позволяет доступ к элементам списка по индексу в квадратных скобках
- property Count - возвращает количество элементов в списке

# запись THistoryItem

- index - целочисленное поле, хранящее индекс изменённого элемента
- action - поле, хранящее тип действия
- value - хранит значение элемента с заданным индексом
- OldValue - хранит значение элемента, которое было до данного изменения

# Основные возможности

* создавать список из элементов любого типа с возможностью отменять и повторять последние изменения
* изменять список
  + вставлять элементы в заданную позицию
  + добавлять элементы в конец списка
  + удалять конкретный элемент
  + заменять конкретный элемент новым значением
  + очищать весь список
* Список хранит историю зменений
  + Каждое изменение сохраняется
  + истори можно очищать
  + Вы можете
    * Отменять любые изменения
    * Возвращать отмененные изменения с помощью коданды истории
  + когды Вы делаете новое изменение вся история последанного состояния стирается.