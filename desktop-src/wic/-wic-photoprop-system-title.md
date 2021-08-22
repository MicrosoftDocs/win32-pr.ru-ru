---
description: Политика метаданных фотографии для свойства System. Title.
ms.assetid: 84da345e-ec03-48fe-8fda-043b706e4e1c
title: Политика метаданных фотографии System. Title
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26917efc84b3308a039abe3a60b279d080aa023e2e4b5f76be8623a7aaae7bf9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118964663"
---
# <a name="systemtitle-photo-metadata-policy"></a>Политика метаданных фотографии System. Title

Политика метаданных фотографии для свойства [System. Title](../properties/props-system-title.md) .

### <a name="pkey"></a>PKEY

\_Название PKEY

### <a name="containers"></a>Контейнеры

JPEG, TIFF

### <a name="read-only"></a>Только для чтения

Нет

### <a name="output-propvariant-type"></a>Тип выходного ПРОПВАРИАНТ

VT \_ LPWSTR

### <a name="input-propvariant-type"></a>Тип входного ПРОПВАРИАНТ

VT \_ LPWSTR или VT \_ LPSTR

### <a name="conflict-resolution-policy"></a>Политика разрешения конфликтов

Выверяются значения из разных схем.

### <a name="jpeg-policy"></a>Политика JPEG

### <a name="read-paths"></a>Пути чтения



| Номер | Путь                                | Формат диска    |
|-------|-------------------------------------|----------------|
| 1     | /APP1/IFD/{ushort = 40091}            | байт в Юникоде \_ |
| 2     | /КСМП/ <xmpalt> DC: Title         | Юникод        |
| 3     | /КСМП/ДК: Title                       | Юникод        |
| 4     | /APP1/IFD/EXIF/{ushort = 37510}       | Юникод        |
| 5     | /APP1/IFD/{ushort = 270}              | ascii          |
| 6     | /app13/irb/8bimiptc/iptc/caption    |                |
| 7     | /КСМП/ <xmpalt> DC: описание   | Юникод        |
| 8     | /КСМП/ДК: описание                 | Юникод        |
| 9     | /app13/irb/8bimiptc/iptc/caption    |                |
| 10    | /КСМП/ <xmpalt> EXIF: усеркоммент | Юникод        |



 

### <a name="write-paths"></a>Пути записи



| Номер | Путь                                | Формат диска    |
|-------|-------------------------------------|----------------|
| 1     | /APP1/IFD/{ushort = 40091}            | байт в Юникоде \_ |
| 2     | /КСМП/ДК: Title                       | Юникод        |
| 3     | /КСМП/ <xmpalt> DC: Title         | Юникод        |
| 4     | /APP1/IFD/EXIF/{ushort = 37510}       | Юникод        |
| 5     | /КСМП/ <xmpalt> EXIF: усеркоммент | Юникод        |
| 6     | /APP1/IFD/{ushort = 270}              | ascii          |
| 7     | /app13/irb/8bimiptc/iptc/caption    |                |
| 8     | /КСМП/ДК: описание                 | Юникод        |
| 9     | /КСМП/ <xmpalt> DC: описание   | Юникод        |



 

### <a name="remove-paths"></a>Удалить пути



| Номер | Путь                                |
|-------|-------------------------------------|
| 1     | /APP1/IFD/{ushort = 40091}            |
| 2     | /КСМП/ДК: Title                       |
| 3     | /APP1/IFD/EXIF/{ushort = 37510}       |
| 4     | /КСМП/ <xmpalt> EXIF: усеркоммент |
| 5     | /APP1/IFD/{ushort = 270}              |
| 6     | /app13/irb/8bimiptc/iptc/caption    |
| 7     | /КСМП/ДК: описание                 |



 

### <a name="tiff-policy"></a>Политика TIFF

### <a name="read-paths"></a>Пути чтения



| Номер | Путь                                    | Формат диска    |
|-------|-----------------------------------------|----------------|
| 1     | /ИФД/{ушорт = 40091}                     | байт в Юникоде \_ |
| 2     | /ИФД/КСМП/ <xmpalt> DC: Title         | Юникод        |
| 3     | /ИФД/КСМП/ДК: Title                       | Юникод        |
| 4     | /ИФД/ексиф/{ушорт = 37510}                | Юникод        |
| 5     | /ИФД/{ушорт = 270}                       | ascii          |
| 6     | /ифд/иптк/каптион                       |                |
| 7     | /ИФД/КСМП/ <xmpalt> DC: описание   | Юникод        |
| 8     | /ИФД/КСМП/ДК: описание                 | Юникод        |
| 9     | /ифд/иптк/каптион                       |                |
| 10    | /ifd/irb/8bimiptc/iptc/caption          |                |
| 11    | /ИФД/КСМП/ <xmpalt> EXIF: усеркоммент | Юникод        |



 

### <a name="write-paths"></a>Пути записи



| Номер | Путь                                    | Формат диска    |
|-------|-----------------------------------------|----------------|
| 1     | /ИФД/{ушорт = 40091}                     | байт в Юникоде \_ |
| 2     | /ИФД/КСМП/ДК: Title                       | Юникод        |
| 3     | /ИФД/КСМП/ <xmpalt> DC: Title         | Юникод        |
| 4     | /ИФД/ексиф/{ушорт = 37510}                | Юникод        |
| 5     | /ИФД/КСМП/ <xmpalt> EXIF: усеркоммент | Юникод        |
| 6     | /ИФД/{ушорт = 270}                       | ascii          |
| 7     | /ифд/иптк/каптион                       |                |
| 8     | /ifd/irb/8bimiptc/iptc/caption          |                |
| 9     | /ИФД/КСМП/ДК: описание                 | Юникод        |
| 10    | /ИФД/КСМП/ <xmpalt> DC: описание   | Юникод        |



 

### <a name="remove-paths"></a>Удалить пути



| Номер | Путь                                    |
|-------|-----------------------------------------|
| 1     | /ИФД/{ушорт = 40091}                     |
| 2     | /ИФД/КСМП/ДК: Title                       |
| 3     | /ИФД/ексиф/{ушорт = 37510}                |
| 4     | /ИФД/КСМП/ <xmpalt> EXIF: усеркоммент |
| 5     | /ИФД/{ушорт = 270}                       |
| 6     | /ифд/иптк/каптион                       |
| 7     | /ifd/irb/8bimiptc/iptc/caption          |
| 8     | /ИФД/КСМП/ДК: описание                 |



 

## <a name="remarks"></a>Remarks

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[System.Title](../properties/props-system-title.md)
</dt> </dl>

 

 
