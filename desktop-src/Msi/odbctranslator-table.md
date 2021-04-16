---
description: В таблице Одбктранслатор перечислены трансляторы ODBC, принадлежащие установке.
ms.assetid: fecb7454-29bb-4ddf-b4d5-2e56c20ff2dc
title: Таблица Одбктранслатор
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9fdf85f73b649e18c0980508e234bf7599e69c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105651168"
---
# <a name="odbctranslator-table"></a>Таблица Одбктранслатор

В таблице Одбктранслатор перечислены трансляторы ODBC, принадлежащие установке.

Таблица Одбктранслатор содержит следующие столбцы.



| Столбец      | Type                         | Ключ | Допускает значения NULL |
|-------------|------------------------------|-----|----------|
| Переводчик  | [Идентификатор](identifier.md) | Да   | Нет        |
| Компонент\_ | [Идентификатор](identifier.md) | Нет   | Нет        |
| Описание | [Text](text.md)             | Нет   | Нет        |
| Файл\_      | [Идентификатор](identifier.md) | Нет   | Нет        |
| \_Настройка файла | [Идентификатор](identifier.md) | Нет   | Да        |



 

## <a name="columns"></a>Столбцы

<dl> <dt>

<span id="Translator"></span><span id="translator"></span><span id="TRANSLATOR"></span>Translator
</dt> <dd>

Имя внутреннего маркера для переводчика. Первичный ключ для таблицы.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>См\_
</dt> <dd>

Внешний ключ в таблице Component.

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Nописание
</dt> <dd>

Описание, зарегистрированное для этого транслятора драйвера ODBC. Это значение не может быть локализовано.

</dd> <dt>

<span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_
</dt> <dd>

DLL-файл для перемещения, указанный в столбце Translator. Столбец File \_ является внешним ключом в [таблице File](file-table.md). Имя файла, указанное в столбце filename этой записи таблицы файлов, должно быть указано в коротком формате имени файла. Синтаксис СФН \| лфн использовать нельзя.

</dd> <dt>

<span id="File_Setup"></span><span id="file_setup"></span><span id="FILE_SETUP"></span>\_Настройка файла
</dt> <dd>

Файл DLL установки для транслятора, если он отличается от столбца Translator. Столбец File \_ является внешним ключом в [таблице File](file-table.md). Имя файла, указанное в столбце filename этой записи таблицы файлов, должно быть указано в коротком формате имени файла. Синтаксис СФН \| лфн использовать нельзя.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Действия [инсталлодбк](installodbc-action.md) и [ремовеодбк](removeodbc-action.md) в [*таблицах последовательностей*](s-gly.md) обрабатывают сведения, приведенные в этой таблице. Дополнительные сведения об использовании *таблиц последовательности* см. [в разделе Использование таблицы последовательностей](using-a-sequence-table.md).

## <a name="validation"></a>Проверка

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
</dl>

 

 



