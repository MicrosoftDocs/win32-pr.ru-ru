---
description: Таблица Филесфпкаталог связывает указанные файлы с файлами каталога, используемыми системой защиты системных файлов.
ms.assetid: 70c8b64a-cf15-411c-8388-4a7e3051f45c
title: Таблица Филесфпкаталог
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2300b73cc1639d8a54e206ea609043cf657c91f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663976"
---
# <a name="filesfpcatalog-table"></a>Таблица Филесфпкаталог

Таблица Филесфпкаталог связывает указанные файлы с файлами каталога, используемыми системой защиты системных файлов.

Windows **Vista, Windows Server 2003 и Windows XP:** Не поддерживается.

Таблица Филесфпкаталог содержит следующие столбцы.



| Столбец       | Type                         | Ключ | Допускает значения NULL |
|--------------|------------------------------|-----|----------|
| Файл\_       | [Идентификатор](identifier.md) | Да   | Нет        |
| сфпкаталог\_ | [Имя файла](filename.md)     | Да   | Нет        |



 

## <a name="columns"></a>Столбцы

<dl> <dt>

<span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_
</dt> <dd>

Внешний ключ к [таблице файлов](file-table.md).

</dd> <dt>

<span id="SFPCatalog_"></span><span id="sfpcatalog_"></span><span id="SFPCATALOG_"></span>сфпкаталог\_
</dt> <dd>

Внешний ключ к [таблице сфпкаталог](sfpcatalog-table.md).

</dd> </dl>

## <a name="remarks"></a>Комментарии

[Действие инсталлсфпкаталогфиле](installsfpcatalogfile-action.md) запрашивает [таблицу компонентов](component-table.md), [таблицу файлов](file-table.md), таблицу филесфпкаталог и [таблицу сфпкаталог](sfpcatalog-table.md).

## <a name="validation"></a>Проверка

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE66](ice66.md)  
[ICE76](ice76.md)  
</dl>

 

 



