---
description: Таблица BindImage содержит сведения о каждом исполняемом файле или библиотеке DLL, которые необходимо привязать к DLL-библиотекам, которые были импортированы.
ms.assetid: 68bf064c-dd85-4796-8e08-6af307f94ad8
title: Таблица BindImage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 729ae4f36f3b258845bcba13748495dc9dfb53c86268bd61e98475d1c7c0c282
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119500772"
---
# <a name="bindimage-table"></a>Таблица BindImage

Таблица BindImage содержит сведения о каждом исполняемом файле или библиотеке DLL, которые необходимо привязать к DLL-библиотекам, которые были импортированы.

Таблица BindImage содержит следующие столбцы.



| Столбец | Type                         | Ключ | Допускает значения NULL |
|--------|------------------------------|-----|----------|
| File\_ | [Идентификатор](identifier.md) | Д   | Нет        |
| Путь   | [Пути](paths.md)           | Нет   | Д        |



 

## <a name="columns"></a>Столбцы

<dl> <dt>

<span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_
</dt> <dd>

Внешний ключ для столбца одной [таблицы File](file-table.md). Это должен быть исполняемый файл или DLL-файл.

</dd> <dt>

<span id="Path"></span><span id="path"></span><span id="PATH"></span>Путь
</dt> <dd>

Список путей, разделенных точкой с запятой, которые представляют пути для поиска импортируемых библиотек DLL. Список обычно представляет собой список свойств, в котором каждое свойство заключено в квадратные скобки ( \[ \] ).

</dd> </dl>

## <a name="remarks"></a>Remarks

Установщик рассчитывает виртуальный адрес каждой функции, которая импортируется из всех библиотек DLL, а вычисленный виртуальный адрес сохраняется в таблице адресов импорта импортируемого образа (IAT).

Эта таблица упоминается при выполнении [действия BindImage](bindimage-action.md) .

## <a name="validation"></a>Проверка

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE46](ice46.md)  
[ICE76](ice76.md)  
</dl>

 

 



