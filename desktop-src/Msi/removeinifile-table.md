---
description: Таблица Ремовеинифиле содержит сведения, которые необходимо удалить из ini-файла приложения.
ms.assetid: 702cf86e-02f4-4ea7-8573-b500ac550aae
title: Таблица Ремовеинифиле
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b57b4ba6f2c42ee636f1b9e21e798e27665f102a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664541"
---
# <a name="removeinifile-table"></a>Таблица Ремовеинифиле

Таблица Ремовеинифиле содержит сведения, которые необходимо удалить из ini-файла приложения.

Таблица Ремовеинифиле содержит следующие столбцы.



| Столбец        | Type                         | Ключ | Допускает значения NULL |
|---------------|------------------------------|-----|----------|
| ремовеинифиле | [Идентификатор](identifier.md) | Да   | Нет        |
| FileName      | [FileName](text.md)         | Нет   | Нет        |
| дирпроперти   | [Идентификатор](identifier.md) | Нет   | Да        |
| Section       | [Формате](formatted.md)   | Нет   | Нет        |
| Ключ           | [Формате](formatted.md)   | Нет   | Нет        |
| Значение         | [Формате](formatted.md)   | Нет   | Да        |
| Действие        | [Integer](integer.md)       | Нет   | Нет        |
| Компонент\_   | [Идентификатор](identifier.md) | Нет   | Нет        |



 

## <a name="columns"></a>Столбцы

<dl> <dt>

<span id="RemoveIniFile"></span><span id="removeinifile"></span><span id="REMOVEINIFILE"></span>ремовеинифиле
</dt> <dd>

Ключ для этой таблицы.

</dd> <dt>

<span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>Файлов
</dt> <dd>

Имя ini-файла, в который необходимо удалить данные.

</dd> <dt>

<span id="DirProperty"></span><span id="dirproperty"></span><span id="DIRPROPERTY"></span>дирпроперти
</dt> <dd>

Имя свойства, значение которого предполагается преобразовать в полный путь к папке удаляемого ini-файла. Свойство может быть именем каталога в [таблице Directory](directory-table.md), свойством, заданным [таблицей аппсеарч](appsearch-table.md), или любым другим свойством, представляющим полный путь.

</dd> <dt>

<span id="Section"></span><span id="section"></span><span id="SECTION"></span>Раздела
</dt> <dd>

Раздел Localizable. ini-файла.

</dd> <dt>

<span id="Key"></span><span id="key"></span><span id="KEY"></span>Раздел
</dt> <dd>

Ключ локализуемого файла. ini ниже раздела.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Значений
</dt> <dd>

Локализуемое значение, которое необходимо удалить. Значение является обязательным, если действие равно 4.

</dd> <dt>

<span id="Action"></span><span id="action"></span><span id="ACTION"></span>Поддержки
</dt> <dd>

Тип изменения, которое необходимо выполнить.



| Константа                         | Шестнадцатеричный | Decimal | Значение                          |
|----------------------------------|-------------|---------|----------------------------------|
| **мсидбинифилеактионремовелине** | 0x002       | 2       | Удаляет запись ini.              |
| **мсидбинифилеактионремоветаг**  | 0x004       | 4       | Удаляет тег из INI-записи. |



 

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>См\_
</dt> <dd>

Внешний ключ в первый столбец [таблицы Component](component-table.md) , ссылающийся на компонент, который управляет удалением значения ini.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Сведения о ini-файле удаляются при выборе соответствующего компонента для установки (локально или из источника).

Эта таблица упоминается при выполнении [действия ремовеинивалуес](removeinivalues-action.md) .

Если столбец каталога \_ указан как null, то расположение ini-файла является стандартным расположением Windows ini, которое по умолчанию является каталогом Windows.

Удаление последнего значения из раздела приводит к удалению этого раздела. Нет другого способа удалить весь раздел, кроме удаления всех его значений.

## <a name="validation"></a>Проверка

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE40](ice40.md)  
[ICE46](ice46.md)  
[ICE69](ice69.md)  
</dl>

 

 



