---
description: Политика метаданных фотографии для свойства System. Image. Компресседбитсперпиксел.
ms.assetid: e97a5c68-6d4a-44af-8096-22680f8b16b8
title: Политика метаданных фотографии System. Image. Компресседбитсперпиксел
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b45b3b1e8b29cdf992cd3b451a2e8a43947139a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702310"
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



| Заказ | Путь                             | Формат диска |
|-------|----------------------------------|-------------|
| 1     | /APP1/IFD/EXIF/{ushort = 37122}    |             |
| 2     | /КСМП/ексиф: Компресседбитсперпиксел |             |



 

### <a name="remove-paths"></a>Удалить пути



| Заказ | Путь                             |
|-------|----------------------------------|
| 1     | /APP1/IFD/EXIF/{ushort = 37122}    |
| 2     | /КСМП/ексиф: компресседбитсперпиксел |



 

### <a name="tiff-policies"></a>Политики TIFF

### <a name="read-paths"></a>Пути чтения



| Заказ | Путь                                 | Формат диска |
|-------|--------------------------------------|-------------|
| 1     | /ИФД/ексиф/{ушорт = 37122}             |             |
| 2     | /ИФД/КСМП/ексиф: Компресседбитсперпиксел |             |



 

### <a name="remove-paths"></a>Удалить пути



| Заказ | Путь                                 |
|-------|--------------------------------------|
| 1     | /ИФД/ексиф/{ушорт = 37122}             |
| 2     | /ИФД/КСМП/ексиф: компресседбитсперпиксел |



 

## <a name="remarks"></a>Комментарии

## <a name="related-topics"></a>См. также

<dl> <dt>

[System. Image. Компресседбитсперпиксел](../properties/props-system-image-compressedbitsperpixel.md)
</dt> </dl>

 

 
