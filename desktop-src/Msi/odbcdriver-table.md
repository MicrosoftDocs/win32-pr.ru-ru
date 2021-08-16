---
description: В таблице Одбкдривер перечислены драйверы ODBC, принадлежащие установке.
ms.assetid: 3518b370-0652-4b54-8057-9871365d5e8c
title: Таблица Одбкдривер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a1eb0da3217d7466fc0beef90933c8a6af32e3d0551ecc6975a31ac55ed2730
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118943125"
---
# <a name="odbcdriver-table"></a>Таблица Одбкдривер

В таблице Одбкдривер перечислены драйверы ODBC, принадлежащие установке.

Таблица Одбкдривер содержит следующие столбцы.



| Столбец      | Type                         | Ключ | Допускает значения NULL |
|-------------|------------------------------|-----|----------|
| Драйвер      | [Идентификатор](identifier.md) | Д   | Нет        |
| Компонент\_ | [Идентификатор](identifier.md) | Нет   | Нет        |
| Описание | [Text](text.md)             | Нет   | Нет        |
| File\_      | [Идентификатор](identifier.md) | Нет   | Нет        |
| \_Настройка файла | [Идентификатор](identifier.md) | Нет   | Д        |



 

## <a name="columns"></a>Столбцы

<dl> <dt>

<span id="Driver"></span><span id="driver"></span><span id="DRIVER"></span>Аудиодрайвера
</dt> <dd>

Имя внутреннего маркера для драйвера. Первичный ключ для таблицы

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>См\_
</dt> <dd>

Внешний ключ в таблице Component.

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Nописание
</dt> <dd>

Описание, зарегистрированное для этого драйвера ODBC. Это значение не может быть локализовано.

</dd> <dt>

<span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_
</dt> <dd>

DLL-файл для драйверов, перечисленных в столбце драйвер. Столбец File \_ является внешним ключом в [таблице File](file-table.md). Имя файла, указанное в столбце filename этой записи таблицы файлов, должно быть указано в коротком формате имени файла. Синтаксис СФН \| лфн использовать нельзя.

</dd> <dt>

<span id="File_Setup"></span><span id="file_setup"></span><span id="FILE_SETUP"></span>\_Настройка файла
</dt> <dd>

Файл DLL установки драйвера, если он отличается от драйвера. Столбец File \_ является внешним ключом в [таблице File](file-table.md). Имя файла, указанное в столбце filename этой записи таблицы файлов, должно быть указано в коротком формате имени файла. Синтаксис СФН \| лфн использовать нельзя.

</dd> </dl>

## <a name="remarks"></a>Remarks

Действия [инсталлодбк](installodbc-action.md) и [ремовеодбк](removeodbc-action.md) в [*таблицах последовательностей*](s-gly.md) обрабатывают сведения, приведенные в этой таблице. Дополнительные сведения об использовании *таблиц последовательности* см. [в разделе Использование таблицы последовательностей](using-a-sequence-table.md).

## <a name="validation"></a>Проверка

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
</dl>

 

 



