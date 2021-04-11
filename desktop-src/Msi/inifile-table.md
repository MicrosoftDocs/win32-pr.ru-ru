---
description: Таблица Инифиле содержит сведения о ini-файле, которые приложение должно установить в ini-файл.
ms.assetid: fdb1a627-da6b-4da1-87a7-7f1c94d3836e
title: Таблица Инифиле
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d63ae37f7c8ed5c50b9b425b0462b445f7acb5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080672"
---
# <a name="inifile-table"></a>Таблица Инифиле

Таблица Инифиле содержит сведения о ini-файле, которые приложение должно установить в ini-файл.

Таблица Инифиле содержит следующие столбцы.



| Столбец      | Type                         | Ключ | Допускает значения NULL |
|-------------|------------------------------|-----|----------|
| инифиле     | [Идентификатор](identifier.md) | Да   | Нет        |
| FileName    | [FileName](text.md)         | Нет   | Нет        |
| дирпроперти | [Идентификатор](identifier.md) | Нет   | Да        |
| Section     | [Формате](formatted.md)   | Нет   | Нет        |
| Ключ         | [Формате](formatted.md)   | Нет   | Нет        |
| Значение       | [Формате](formatted.md)   | Нет   | Нет        |
| Действие      | [Integer](integer.md)       | Нет   | Нет        |
| Компонент\_ | [Идентификатор](identifier.md) | Нет   | Нет        |



 

## <a name="columns"></a>Столбцы

<dl> <dt>

<span id="IniFile"></span><span id="inifile"></span><span id="INIFILE"></span>инифиле
</dt> <dd>

Ключ для этой таблицы.

</dd> <dt>

<span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>Файлов
</dt> <dd>

Локализуемое имя ini-файла, в который записываются сведения.

</dd> <dt>

<span id="DirProperty"></span><span id="dirproperty"></span><span id="DIRPROPERTY"></span>дирпроперти
</dt> <dd>

Имя свойства со значением, которое разрешается в полный путь к папке, содержащей ini-файл. Свойство может быть именем каталога в [таблице Directory](directory-table.md), свойством, заданным [таблицей аппсеарч](appsearch-table.md), или любым другим свойством, представляющим полный путь. Если это поле оставлено пустым, ini-файл создается в папке с полным путем, указанным в свойстве [**виндовсфолдер**](windowsfolder.md) .

</dd> <dt>

<span id="Section"></span><span id="section"></span><span id="SECTION"></span>Раздела
</dt> <dd>

Раздел Localizable. ini-файла.

</dd> <dt>

<span id="Key"></span><span id="key"></span><span id="KEY"></span>Раздел
</dt> <dd>

Ключ локализуемого файла. ini в разделе.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Значений
</dt> <dd>

Локализуемое значение, которое необходимо записать.

</dd> <dt>

<span id="Action"></span><span id="action"></span><span id="ACTION"></span>Поддержки
</dt> <dd>

Тип изменения, которое необходимо выполнить.



| Константа                         | Шестнадцатеричный | Decimal | Изменение                                                                     |
|----------------------------------|-------------|---------|----------------------------------------------------------------------------------|
| **мсидбинифилеактионаддлине**    | 0x000       | 0       | Создает или обновляет запись ini-элемента.                                                 |
| **мсидбинифилеактионкреателине** | 0x001       | 1       | Создает запись ini, только если запись еще не существует.                   |
| **мсидбинифилеактионаддтаг**     | 0x003       | 3       | Создает новую запись или добавляет к существующей записи новое значение с разделителями-запятыми. |



 

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>См\_
</dt> <dd>

Внешний ключ в первый столбец [таблицы Component](component-table.md) , ссылающийся на компонент, который управляет установкой значения. ini.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Сведения о ini-файле записываются, когда соответствующий компонент был выбран для установки в качестве локального или запуска из источника.

Эта таблица упоминается при выполнении [действия вритеинивалуес](writeinivalues-action.md) или [ремовеинивалуес](removeinivalues-action.md) .

## <a name="validation"></a>Проверка

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE46](ice46.md)  
[ICE69](ice69.md)  
[ICE88](ice88.md)  
[ICE91](ice91.md)  
</dl>

 

 



