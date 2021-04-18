---
description: Политика метаданных фотографии для свойства System. Author.
ms.assetid: 2de9c452-93be-40a4-a72b-5da590534dfd
title: Политика метаданных фотографии System. Author
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb90345257ef1623f7cda1ce4318af7a9f472df5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105719694"
---
# <a name="systemauthor-photo-metadata-policy"></a>Политика метаданных фотографии System. Author

Политика метаданных фотографии для свойства [System. Author](../properties/props-system-author.md) .

### <a name="pkey"></a>PKEY

\_Автор PKEY

### <a name="containers"></a>Контейнеры

JPEG, TIFF

### <a name="read-only"></a>Только для чтения

Нет

### <a name="output-propvariant-type"></a>Тип выходного ПРОПВАРИАНТ

VT \_ Векторная \| \_ LPWSTR

### <a name="input-propvariant-type"></a>Тип входного ПРОПВАРИАНТ

\_Предпочтителен VT Vector \| VT \_ , но \_ также принимается VT LPWSTR.

### <a name="conflict-resolution-policy"></a>Политика разрешения конфликтов

Выверяются значения из разных схем.

### <a name="jpeg-policy"></a>Политика JPEG

### <a name="read-paths"></a>Пути чтения



| Заказ | Путь                             | Формат диска    |
|-------|----------------------------------|----------------|
| 1     | /APP1/IFD/{ushort = 315}           | ascii          |
| 2     | /app13/irb/8bimiptc/iptc/by-line |                |
| 3     | /КСМП/ <xmpseq> DC: Creator    | Юникод        |
| 4     | /app13/irb/8bimiptc/iptc/by-line |                |
| 5     | /APP1/IFD/{ushort = 40093}         | байт в Юникоде \_ |
| 6     | /КСМП/Тифф: исполнитель                 | Юникод        |



 

### <a name="write-paths"></a>Пути записи



| Заказ | Путь                             | Формат диска    |
|-------|----------------------------------|----------------|
| 1     | /КСМП/ <xmpseq> DC: Creator    | Юникод        |
| 2     | /КСМП/Тифф: исполнитель                 | Юникод        |
| 3     | /app13/irb/8bimiptc/iptc/by-line |                |
| 4     | /APP1/IFD/{ushort = 315}           | ascii          |
| 5     | /APP1/IFD/{ushort = 40093}         | байт в Юникоде \_ |



 

### <a name="remove-paths"></a>Удалить пути



| Заказ | Путь                             |
|-------|----------------------------------|
| 1     | /КСМП/ДК: Creator                  |
| 2     | /КСМП/Тифф: исполнитель                 |
| 3     | /app13/irb/8bimiptc/iptc/by-line |
| 4     | /APP1/IFD/{ushort = 315}           |
| 5     | /APP1/IFD/{ushort = 40093}         |



 

### <a name="tiff-policy"></a>Политика TIFF

### <a name="read-paths"></a>Пути чтения



| Заказ | Путь                              | Формат диска    |
|-------|-----------------------------------|----------------|
| 1     | /ИФД/{ушорт = 315}                 | ascii          |
| 2     | /ифд/иптк/би-лине                 |                |
| 3     | /ИФД/КСМП/ <xmpseq> DC: Creator | Юникод        |
| 4     | /ифд/иптк/би-лине                 |                |
| 5     | /ИФД/{ушорт = 40093}               | байт в Юникоде \_ |
| 6     | /ifd/irb/8bimiptc/iptc/by-line    |                |
| 7     | /ИФД/КСМП/Тифф: исполнитель              | Юникод        |



 

### <a name="write-paths"></a>Пути записи



| Заказ | Путь                              | Формат диска    |
|-------|-----------------------------------|----------------|
| 1     | /ИФД/КСМП/ <xmpseq> DC: Creator | Юникод        |
| 2     | /ИФД/КСМП/Тифф: исполнитель              | Юникод        |
| 3     | /ифд/иптк/би-лине                 |                |
| 4     | /ИФД/{ушорт = 315}                 | \_вектор ASCII  |
| 5     | /ИФД/{ушорт = 40093}               | байт в Юникоде \_ |
| 6     | /ифд/иптк/би-лине                 |                |



 

### <a name="remove-paths"></a>Удалить пути



| Заказ | Путь                           |
|-------|--------------------------------|
| 1     | /ИФД/КСМП/ДК: Creator            |
| 2     | /ИФД/КСМП/Тифф: исполнитель           |
| 3     | /ифд/иптк/би-лине              |
| 4     | /ifd/irb/8bimiptc/iptc/by-line |
| 5     | /ИФД/{ушорт = 315}              |
| 6     | /ИФД/{ушорт = 40093}            |



 

### <a name="remarks"></a>Комментарии

## <a name="related-topics"></a>См. также

<dl> <dt>

[System.Author](../properties/props-system-author.md)
</dt> </dl>

 

 
