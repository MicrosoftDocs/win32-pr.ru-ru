---
description: Политика метаданных фотографии для свойства System. Image. Колорспаце.
ms.assetid: 10770f16-8db2-4719-bce3-452f578002ec
title: Политика метаданных фотографии System. Image. Колорспаце
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85c7d7c9134a8bd93a12ba6cfb6bd8605e228cb6b745ad4401a94f91a2ba9ff9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118710424"
---
# <a name="systemimagecolorspace-photo-metadata-policy"></a>Политика метаданных фотографии System. Image. Колорспаце

Политика метаданных фотографии для свойства [System. Image. колорспаце](../properties/props-system-image-colorspace.md) .

### <a name="pkey"></a>PKEY

\_Колорспаце образа \_ PKEY

### <a name="containers"></a>Контейнеры

JPEG, TIFF

### <a name="read-only"></a>Только для чтения

Да

### <a name="output-propvariant-type"></a>Тип выходного ПРОПВАРИАНТ

VT \_ UI2

### <a name="input-type"></a>Тип входных данных

UShort

### <a name="conflict-resolution-policy"></a>Политика разрешения конфликтов

Выверяются значения из разных схем.

### <a name="jpeg-policy"></a>Политика JPEG

### <a name="read-paths"></a>Пути чтения



| Номер | Путь                          | Формат диска |
|-------|-------------------------------|-------------|
| 1     | /APP1/IFD/EXIF/{ushort = 40961} | ushort      |
| 2     | /КСМП/ексиф: Колорспаце          | Юникод     |



 

### <a name="write-paths"></a>Пути записи



| Номер | Путь                          | Формат диска |
|-------|-------------------------------|-------------|
| 1     | /APP1/IFD/EXIF/{ushort = 40961} | ushort      |
| 2     | /КСМП/ексиф: Колорспаце          | Юникод     |



 

### <a name="remove-paths"></a>Удалить пути



| Номер | Путь                          |
|-------|-------------------------------|
| 1     | /APP1/IFD/EXIF/{ushort = 40961} |
| 2     | /КСМП/ексиф: колорспаце          |



 

### <a name="tiff-policies"></a>Политики TIFF

### <a name="read-paths"></a>Пути чтения



| Номер | Путь                     | Формат диска |
|-------|--------------------------|-------------|
| 1     | /ИФД/ексиф/{ушорт = 40961} | ushort      |
| 2     | /ИФД/КСМП/ексиф: Колорспаце | Юникод     |



 

### <a name="write-paths"></a>Пути записи



| Номер | Путь                     | Формат диска |
|-------|--------------------------|-------------|
| 1     | /ИФД/ексиф/{ушорт = 40961} | ushort      |
| 2     | /ИФД/КСМП/ексиф: Колорспаце | Юникод     |



 

### <a name="remove-paths"></a>Удалить пути



| Номер | Путь                     |
|-------|--------------------------|
| 1     | /ИФД/ексиф/{ушорт = 40961} |
| 2     | /ИФД/КСМП/ексиф: колорспаце |



 

## <a name="remarks"></a>Remarks

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[System. Image. Колорспаце](../properties/props-system-image-colorspace.md)
</dt> </dl>

 

 
