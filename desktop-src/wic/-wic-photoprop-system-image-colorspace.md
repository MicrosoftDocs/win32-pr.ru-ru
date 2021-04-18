---
description: Политика метаданных фотографии для свойства System. Image. Колорспаце.
ms.assetid: 10770f16-8db2-4719-bce3-452f578002ec
title: Политика метаданных фотографии System. Image. Колорспаце
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b6ef2003d05fa19b958b28950f71ec2d5f73027
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702311"
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



| Заказ | Путь                          | Формат диска |
|-------|-------------------------------|-------------|
| 1     | /APP1/IFD/EXIF/{ushort = 40961} | ushort      |
| 2     | /КСМП/ексиф: Колорспаце          | Юникод     |



 

### <a name="write-paths"></a>Пути записи



| Заказ | Путь                          | Формат диска |
|-------|-------------------------------|-------------|
| 1     | /APP1/IFD/EXIF/{ushort = 40961} | ushort      |
| 2     | /КСМП/ексиф: Колорспаце          | Юникод     |



 

### <a name="remove-paths"></a>Удалить пути



| Заказ | Путь                          |
|-------|-------------------------------|
| 1     | /APP1/IFD/EXIF/{ushort = 40961} |
| 2     | /КСМП/ексиф: колорспаце          |



 

### <a name="tiff-policies"></a>Политики TIFF

### <a name="read-paths"></a>Пути чтения



| Заказ | Путь                     | Формат диска |
|-------|--------------------------|-------------|
| 1     | /ИФД/ексиф/{ушорт = 40961} | ushort      |
| 2     | /ИФД/КСМП/ексиф: Колорспаце | Юникод     |



 

### <a name="write-paths"></a>Пути записи



| Заказ | Путь                     | Формат диска |
|-------|--------------------------|-------------|
| 1     | /ИФД/ексиф/{ушорт = 40961} | ushort      |
| 2     | /ИФД/КСМП/ексиф: Колорспаце | Юникод     |



 

### <a name="remove-paths"></a>Удалить пути



| Заказ | Путь                     |
|-------|--------------------------|
| 1     | /ИФД/ексиф/{ушорт = 40961} |
| 2     | /ИФД/КСМП/ексиф: колорспаце |



 

## <a name="remarks"></a>Комментарии

## <a name="related-topics"></a>См. также

<dl> <dt>

[System. Image. Колорспаце](../properties/props-system-image-colorspace.md)
</dt> </dl>

 

 
