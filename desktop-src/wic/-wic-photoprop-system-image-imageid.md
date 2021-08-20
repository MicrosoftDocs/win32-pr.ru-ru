---
description: Политика метаданных фотографии для свойства System. Image. Имажеид.
ms.assetid: 2a092d16-e7b9-4ffe-9bdb-01ed328ca26f
title: Политика метаданных фотографии System. Image. Имажеид
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17453b989aba5ab0c750138ec6802d1c67a82b936dd1747d7413e39b38ae2256
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117667604"
---
# <a name="systemimageimageid-photo-metadata-policy"></a>Политика метаданных фотографии System. Image. Имажеид

Политика метаданных фотографии для свойства [System. Image. имажеид](../properties/props-system-image-imageid.md) .

### <a name="pkey"></a>PKEY

\_Имажеид образа \_ PKEY

### <a name="containers"></a>Контейнеры

JPEG, TIFF

### <a name="read-only"></a>Только для чтения

Нет

### <a name="output-propvariant-type"></a>Тип выходного ПРОПВАРИАНТ

VT \_ LPWSTR

### <a name="input-type"></a>Тип входных данных

Строка.

### <a name="conflict-resolution-policy"></a>Политика разрешения конфликтов

Выверяются значения из разных схем.

### <a name="jpeg-policy"></a>Политика JPEG

### <a name="read-paths"></a>Пути чтения



| Номер | Путь                          | Формат диска |
|-------|-------------------------------|-------------|
| 1     | /APP1/IFD/EXIF/{ushort = 42016} | ascii       |
| 2     | /КСМП/ексиф: Imageuniqueid)       | Юникод     |



 

### <a name="write-paths"></a>Пути записи



| Номер | Путь                          | Формат диска |
|-------|-------------------------------|-------------|
| 1     | /APP1/IFD/EXIF/{ushort = 42016} | ascii       |
| 2     | /КСМП/ексиф: Imageuniqueid)       | Юникод     |



 

### <a name="remove-paths"></a>Удалить пути



| Номер | Путь                          |
|-------|-------------------------------|
| 1     | /APP1/IFD/EXIF/{ushort = 42016} |
| 2     | /КСМП/ексиф: Imageuniqueid)       |



 

### <a name="tiff-policy"></a>Политика TIFF

### <a name="read-paths"></a>Пути чтения



| Номер | Путь                        | Формат диска |
|-------|-----------------------------|-------------|
|       | /ИФД/ексиф/{ушорт = 42016}    | ascii       |
|       | /ИФД/КСМП/ексиф: Imageuniqueid) | Юникод     |



 

### <a name="write-paths"></a>Пути записи



| Номер | Путь                        | Формат диска |
|-------|-----------------------------|-------------|
|       | /ИФД/ексиф/{ушорт = 42016}    | ascii       |
|       | /ИФД/КСМП/ексиф: Imageuniqueid) | Юникод     |



 

### <a name="remove-paths"></a>Удалить пути



| Номер | Путь                        |
|-------|-----------------------------|
|       | /ИФД/ексиф/{ушорт = 42016}    |
|       | /ИФД/КСМП/ексиф: Imageuniqueid) |



 

## <a name="remarks"></a>Remarks

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[System. Image. Имажеид](../properties/props-system-image-imageid.md)
</dt> </dl>

 

 
