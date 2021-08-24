---
description: Таблица Филесфпкаталог связывает указанные файлы с файлами каталога, используемыми системой защиты системных файлов.
ms.assetid: 70c8b64a-cf15-411c-8388-4a7e3051f45c
title: Таблица Филесфпкаталог
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41bec6e31cba93730cc65b04ffdfb4a509f0cd817ba709cc029edfb47c4c4e60
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119581594"
---
# <a name="filesfpcatalog-table"></a>Таблица Филесфпкаталог

Таблица Филесфпкаталог связывает указанные файлы с файлами каталога, используемыми системой защиты системных файлов.

**Windows Vista, Windows Server 2003 и Windows XP:** Не поддерживается.

Таблица Филесфпкаталог содержит следующие столбцы.



| Столбец       | Type                         | Ключ | Допускает значения NULL |
|--------------|------------------------------|-----|----------|
| File\_       | [Идентификатор](identifier.md) | Д   | Нет        |
| сфпкаталог\_ | [Имя файла](filename.md)     | Д   | Нет        |



 

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

## <a name="remarks"></a>Remarks

[Действие инсталлсфпкаталогфиле](installsfpcatalogfile-action.md) запрашивает [таблицу компонентов](component-table.md), [таблицу файлов](file-table.md), таблицу филесфпкаталог и [таблицу сфпкаталог](sfpcatalog-table.md).

## <a name="validation"></a>Проверка

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE66](ice66.md)  
[ICE76](ice76.md)  
</dl>

 

 



