---
description: Политика метаданных фотографии для свойства System. Image. Вертикалресолутион.
ms.assetid: a58b7463-3572-4ca8-8299-93d92d2f06fb
title: Политика метаданных фотографии System. Image. Вертикалресолутион
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02e895ef9e1181a3ec40b474940c6dfaaa3e1329
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702303"
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



| Заказ | Путь                   | Формат диска |
|-------|------------------------|-------------|
| 1     | /APP1/IFD/{ushort = 283} |             |
| 2     | /КСМП/Тифф: Иресолутион  |             |



 

### <a name="remove-paths"></a>Удалить пути



| Заказ | Путь                        |
|-------|-----------------------------|
| 1     | /APP1/IFD/EXIF/{ushort = 283} |
| 2     | /КСМП/Тифф: иресолутион       |



 

### <a name="tiff-policies"></a>Политики TIFF

### <a name="read-paths"></a>Пути чтения



| Заказ | Путь                      | Формат диска |
|-------|---------------------------|-------------|
| 1     | /ИФД/ексиф/{ушорт = 283}    |             |
| 2     | /ИФД/КСМП/Тифф: Иресолутион |             |



 

### <a name="remove-paths"></a>Удалить пути



| Заказ | Путь                      |
|-------|---------------------------|
| 1     | /ИФД/ексиф/{ушорт = 283}    |
| 2     | /ИФД/КСМП/Тифф: иресолутион |



 

## <a name="remarks"></a>Комментарии

## <a name="related-topics"></a>См. также

<dl> <dt>

[System. Image. Вертикалресолутион](../properties/props-system-image-verticalresolution.md)
</dt> </dl>

 

 
