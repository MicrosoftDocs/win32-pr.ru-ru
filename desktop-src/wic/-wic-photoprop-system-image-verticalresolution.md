---
description: Политика метаданных фотографии для свойства System. Image. Вертикалресолутион.
ms.assetid: a58b7463-3572-4ca8-8299-93d92d2f06fb
title: Политика метаданных фотографии System. Image. Вертикалресолутион
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9962a00be34d227756d295e992174d6e80b6d058fc32af29ad9cde58a04ed07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118710287"
---
# <a name="systemimageverticalresolution-photo-metadata-policy"></a>Политика метаданных фотографии System. Image. Вертикалресолутион

Политика метаданных фотографии для свойства [System. Image. вертикалресолутион](../properties/props-system-image-verticalresolution.md) .

### <a name="pkey"></a>PKEY

\_Вертикалресолутион образа \_ PKEY

### <a name="containers"></a>Контейнеры

JPEG, TIFF

### <a name="read-only"></a>Только для чтения

Да.

### <a name="output-propvariant-type"></a>Тип выходного ПРОПВАРИАНТ

VT \_ R8

### <a name="conflict-resolution-policy"></a>Политика разрешения конфликтов

Это значение создается системой и не может быть записано напрямую. Выверяются значения из разных схем.

### <a name="jpeg-policy"></a>Политика JPEG

### <a name="read-paths"></a>Пути чтения



| Номер | Путь                   | Формат диска |
|-------|------------------------|-------------|
| 1     | /APP1/IFD/{ushort = 283} |             |
| 2     | /КСМП/Тифф: Иресолутион  |             |



 

### <a name="remove-paths"></a>Удалить пути



| Номер | Путь                        |
|-------|-----------------------------|
| 1     | /APP1/IFD/EXIF/{ushort = 283} |
| 2     | /КСМП/Тифф: иресолутион       |



 

### <a name="tiff-policies"></a>Политики TIFF

### <a name="read-paths"></a>Пути чтения



| Номер | Путь                      | Формат диска |
|-------|---------------------------|-------------|
| 1     | /ИФД/ексиф/{ушорт = 283}    |             |
| 2     | /ИФД/КСМП/Тифф: Иресолутион |             |



 

### <a name="remove-paths"></a>Удалить пути



| Номер | Путь                      |
|-------|---------------------------|
| 1     | /ИФД/ексиф/{ушорт = 283}    |
| 2     | /ИФД/КСМП/Тифф: иресолутион |



 

## <a name="remarks"></a>Remarks

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[System. Image. Вертикалресолутион](../properties/props-system-image-verticalresolution.md)
</dt> </dl>

 

 
