---
description: Политика метаданных фотографии для свойства System. photo. Дигиталзум.
ms.assetid: 22a69d3e-4ec3-4652-b4bb-dfcfffc2322b
title: Политика метаданных фото для System. photo. Дигиталзум
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bf440e92243eb2102ac6abaa349ea83e58d9a2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347425"
---
# <a name="systemphotodigitalzoom-photo-metadata-policy"></a>Политика метаданных фото для System. photo. Дигиталзум

Политика метаданных фотографии для свойства [System. photo. дигиталзум](../properties/props-system-photo-digitalzoom.md) .

### <a name="pkey"></a>PKEY

\_Дигиталзум фото на PKEY \_

### <a name="containers"></a>Контейнеры

JPEG, TIFF

### <a name="read-only"></a>Только для чтения

Да

### <a name="output-propvariant-type"></a>Тип выходного ПРОПВАРИАНТ

VT \_ R8

### <a name="conflict-resolution-policy"></a>Политика разрешения конфликтов

Это значение формируется из System. photo. Дигиталзумнумератор и System. photo. Дигиталзумденоминатор. Он не может быть записан напрямую. Выверяются значения из разных схем.

### <a name="jpeg-policy"></a>Политика JPEG

### <a name="read-paths"></a>Пути чтения



| Заказ | Путь                          | Формат диска |
|-------|-------------------------------|-------------|
| 1     | /APP1/IFD/EXIF/{ushort = 41988} |             |
| 2     | /КСМП/ексиф: Дигиталзумратио    |             |



 

### <a name="write-paths"></a>Пути записи



| Заказ | Путь                          | Формат диска |
|-------|-------------------------------|-------------|
| 1     | /APP1/IFD/EXIF/{ushort = 41988} |             |
| 2     | /КСМП/ексиф: Дигиталзумратио    |             |



 

### <a name="remove-paths"></a>Удалить пути



| Заказ | Путь                          |
|-------|-------------------------------|
| 1     | /APP1/IFD/EXIF/{ushort = 41988} |
| 2     | /КСМП/ексиф: дигиталзумратио    |



 

### <a name="tiff-policies"></a>Политики TIFF

### <a name="read-paths"></a>Пути чтения



| Заказ | Путь                           | Формат диска |
|-------|--------------------------------|-------------|
| 1     | /ИФД/ексиф/{ушорт = 41988}       |             |
| 2     | /ИФД/КСМП/ексиф: Дигиталзумратио |             |



 

### <a name="write-paths"></a>Пути записи



| Заказ | Путь                           | Формат диска |
|-------|--------------------------------|-------------|
| 1     | /ИФД/ексиф/{ушорт = 41988}       |             |
| 2     | /ИФД/КСМП/ексиф: Дигиталзумратио |             |



 

### <a name="remove-paths"></a>Удалить пути



| Заказ | Путь                           |
|-------|--------------------------------|
| 1     | /ИФД/ексиф/{ушорт = 41988}       |
| 2     | /ИФД/КСМП/ексиф: дигиталзумратио |



 

## <a name="remarks"></a>Комментарии

## <a name="related-topics"></a>См. также

<dl> <dt>

[System. photo. Дигиталзум](../properties/props-system-photo-digitalzoom.md)
</dt> </dl>

 

 
