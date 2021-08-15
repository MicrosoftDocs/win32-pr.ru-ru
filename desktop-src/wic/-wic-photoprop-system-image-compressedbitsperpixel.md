---
description: Политика метаданных фотографии для свойства System. Image. Компресседбитсперпиксел.
ms.assetid: e97a5c68-6d4a-44af-8096-22680f8b16b8
title: Политика метаданных фотографии System. Image. Компресседбитсперпиксел
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a18cc76e22c5c409e19e08fc5a2e667ad374348bc753ffa85cd09003a8bdaf4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118032713"
---
# <a name="systemimagecompressedbitsperpixel-photo-metadata-policy"></a>Политика метаданных фотографии System. Image. Компресседбитсперпиксел

Политика метаданных фотографии для свойства [System. Image. компресседбитсперпиксел](../properties/props-system-image-compressedbitsperpixel.md) .

### <a name="pkey"></a>PKEY

\_Компресседбитсперпиксел образа \_ PKEY

### <a name="containers"></a>Контейнеры

JPEG, TIFF

### <a name="read-only"></a>Только для чтения

Да

### <a name="output-propvariant-type"></a>Тип выходного ПРОПВАРИАНТ

VT \_ R8

### <a name="conflict-resolution-policy"></a>Политика разрешения конфликтов

Это значение формируется из System. Image. Компресседбитсперпикселнумератор и System. Image. Компресседбитсперпикселденоминатор. Он не может быть записан напрямую. Выверяются значения из разных схем.

### <a name="jpeg-policy"></a>Политика JPEG

### <a name="read-paths"></a>Пути чтения



| Номер | Путь                             | Формат диска |
|-------|----------------------------------|-------------|
| 1     | /APP1/IFD/EXIF/{ushort = 37122}    |             |
| 2     | /КСМП/ексиф: Компресседбитсперпиксел |             |



 

### <a name="remove-paths"></a>Удалить пути



| Номер | Путь                             |
|-------|----------------------------------|
| 1     | /APP1/IFD/EXIF/{ushort = 37122}    |
| 2     | /КСМП/ексиф: компресседбитсперпиксел |



 

### <a name="tiff-policies"></a>Политики TIFF

### <a name="read-paths"></a>Пути чтения



| Номер | Путь                                 | Формат диска |
|-------|--------------------------------------|-------------|
| 1     | /ИФД/ексиф/{ушорт = 37122}             |             |
| 2     | /ИФД/КСМП/ексиф: Компресседбитсперпиксел |             |



 

### <a name="remove-paths"></a>Удалить пути



| Номер | Путь                                 |
|-------|--------------------------------------|
| 1     | /ИФД/ексиф/{ушорт = 37122}             |
| 2     | /ИФД/КСМП/ексиф: компресседбитсперпиксел |



 

## <a name="remarks"></a>Remarks

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[System. Image. Компресседбитсперпиксел](../properties/props-system-image-compressedbitsperpixel.md)
</dt> </dl>

 

 
