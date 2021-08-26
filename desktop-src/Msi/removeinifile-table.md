---
description: Таблица Ремовеинифиле содержит информацию, которую приложение необходимо удалить из файла .ini.
ms.assetid: 702cf86e-02f4-4ea7-8573-b500ac550aae
title: Таблица Ремовеинифиле
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6aca38f320a8cb548faf00d284cff4c934e127a44cbaf7ca5b96013fac80d63
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120074584"
---
# <a name="removeinifile-table"></a>Таблица Ремовеинифиле

Таблица Ремовеинифиле содержит информацию, которую приложение необходимо удалить из файла .ini.

Таблица Ремовеинифиле содержит следующие столбцы.



| Столбец        | Type                         | Ключ | Допускает значения NULL |
|---------------|------------------------------|-----|----------|
| ремовеинифиле | [Идентификатор](identifier.md) | Д   | Нет        |
| FileName      | [FileName](text.md)         | Нет   | Нет        |
| дирпроперти   | [Идентификатор](identifier.md) | Нет   | Д        |
| Section       | [Формате](formatted.md)   | Нет   | Нет        |
| Ключ           | [Формате](formatted.md)   | Нет   | Нет        |
| Значение         | [Формате](formatted.md)   | Нет   | Д        |
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

.ini имя файла, в который нужно удалить данные.

</dd> <dt>

<span id="DirProperty"></span><span id="dirproperty"></span><span id="DIRPROPERTY"></span>дирпроперти
</dt> <dd>

Имя свойства, значение которого предполагается разрешить в полный путь к папке удаляемого файла .ini. Свойство может быть именем каталога в [таблице Directory](directory-table.md), свойством, заданным [таблицей аппсеарч](appsearch-table.md), или любым другим свойством, представляющим полный путь.

</dd> <dt>

<span id="Section"></span><span id="section"></span><span id="SECTION"></span>Раздела
</dt> <dd>

Раздел файла локализуемого .ini.

</dd> <dt>

<span id="Key"></span><span id="key"></span><span id="KEY"></span>Раздел
</dt> <dd>

Локализованный .iniный ключ файла под разделом.

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
| **мсидбинифилеактионремовелине** | 0x002       | 2       | Удаляет .ini запись.              |
| **мсидбинифилеактионремоветаг**  | 0x004       | 4       | Удаляет тег из записи .ini. |



 

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>См\_
</dt> <dd>

Внешний ключ в первый столбец [таблицы Component](component-table.md) , ссылающийся на компонент, который управляет удалением значения .ini.

</dd> </dl>

## <a name="remarks"></a>Remarks

Сведения о .ini файле удаляются, когда соответствующий компонент выбран для установки, локально или из источника.

Эта таблица упоминается при выполнении [действия ремовеинивалуес](removeinivalues-action.md) .

если столбец каталога \_ указан как null, то расположение ini-файла является стандартным расположением Windows ini, которое по умолчанию является каталогом Windows.

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

 

 



