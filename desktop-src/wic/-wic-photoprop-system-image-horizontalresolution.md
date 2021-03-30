---
title: Политика метаданных фотографии System. Image. Хоризонталресолутион
description: Политика метаданных фотографии для свойства System. Image. Хоризонталресолутион.
ms.assetid: 1fe73c50-4179-4ea4-be1c-9e103fb65d59
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ade406e644524fea84ef6baf957aed661d2adf07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103814248"
---
# <a name="systemimagehorizontalresolution-photo-metadata-policy"></a>Политика метаданных фотографии System. Image. Хоризонталресолутион

Политика метаданных фотографии для свойства [System. Image. хоризонталресолутион](../properties/props-system-image-horizontalresolution.md) .

### <a name="pkey"></a>PKEY

\_Хоризонталресолутион образа \_ PKEY

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



| Заказ | Путь                   | Формат диска |
|-------|------------------------|-------------|
| 1     | /APP1/IFD/{ushort = 282} |             |
| 2     | /КСМП/Тифф: Ксресолутион  |             |



 

### <a name="remove-paths"></a>Удалить пути



| Заказ | Путь                        | Формат диска |
|-------|-----------------------------|-------------|
| 1     | /APP1/IFD/EXIF/{ushort = 282} |             |
| 2     | /КСМП/Тифф: ксресолутион       |             |



 

### <a name="tiff-policies"></a>Политики TIFF

### <a name="read-paths"></a>Пути чтения



| Заказ | Путь                      | Формат диска |
|-------|---------------------------|-------------|
| 1     | /ИФД/ексиф/{ушорт = 282}    |             |
| 2     | /ИФД/КСМП/Тифф: Ксресолутион |             |



 

### <a name="remove-paths"></a>Удалить пути



| Заказ | Путь                      | Формат диска |
|-------|---------------------------|-------------|
| 1     | /ИФД/ексиф/{ушорт = 282}    |             |
| 2     | /ИФД/КСМП/Тифф: ксресолутион |             |



 

## <a name="remarks"></a>Комментарии

## <a name="related-topics"></a>См. также

<dl> <dt>

[System. Image. Хоризонталресолутион](../properties/props-system-image-horizontalresolution.md)
</dt> </dl>

 

 
