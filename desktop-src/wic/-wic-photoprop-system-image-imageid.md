---
description: Политика метаданных фотографии для свойства System. Image. Имажеид.
ms.assetid: 2a092d16-e7b9-4ffe-9bdb-01ed328ca26f
title: Политика метаданных фотографии System. Image. Имажеид
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bab812a8719c905002c91d33a65cc2b570d37cc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104545719"
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



| Заказ | Путь                          | Формат диска |
|-------|-------------------------------|-------------|
| 1     | /APP1/IFD/EXIF/{ushort = 42016} | ascii       |
| 2     | /КСМП/ексиф: Imageuniqueid)       | Юникод     |



 

### <a name="write-paths"></a>Пути записи



| Заказ | Путь                          | Формат диска |
|-------|-------------------------------|-------------|
| 1     | /APP1/IFD/EXIF/{ushort = 42016} | ascii       |
| 2     | /КСМП/ексиф: Imageuniqueid)       | Юникод     |



 

### <a name="remove-paths"></a>Удалить пути



| Заказ | Путь                          |
|-------|-------------------------------|
| 1     | /APP1/IFD/EXIF/{ushort = 42016} |
| 2     | /КСМП/ексиф: Imageuniqueid)       |



 

### <a name="tiff-policy"></a>Политика TIFF

### <a name="read-paths"></a>Пути чтения



| Заказ | Путь                        | Формат диска |
|-------|-----------------------------|-------------|
|       | /ИФД/ексиф/{ушорт = 42016}    | ascii       |
|       | /ИФД/КСМП/ексиф: Imageuniqueid) | Юникод     |



 

### <a name="write-paths"></a>Пути записи



| Заказ | Путь                        | Формат диска |
|-------|-----------------------------|-------------|
|       | /ИФД/ексиф/{ушорт = 42016}    | ascii       |
|       | /ИФД/КСМП/ексиф: Imageuniqueid) | Юникод     |



 

### <a name="remove-paths"></a>Удалить пути



| Заказ | Путь                        |
|-------|-----------------------------|
|       | /ИФД/ексиф/{ушорт = 42016}    |
|       | /ИФД/КСМП/ексиф: Imageuniqueid) |



 

## <a name="remarks"></a>Комментарии

## <a name="related-topics"></a>См. также

<dl> <dt>

[System. Image. Имажеид](../properties/props-system-image-imageid.md)
</dt> </dl>

 

 
