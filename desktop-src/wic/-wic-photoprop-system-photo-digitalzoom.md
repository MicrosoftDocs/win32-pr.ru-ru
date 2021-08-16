---
description: Политика метаданных фотографии для свойства System. photo. Дигиталзум.
ms.assetid: 22a69d3e-4ec3-4652-b4bb-dfcfffc2322b
title: Политика метаданных фото для System. photo. Дигиталзум
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19dfaf2838c8f321b1406d951fcc335076bcdfc00e3a17de0954f1a62022570e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118205380"
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



| Номер | Путь                          | Формат диска |
|-------|-------------------------------|-------------|
| 1     | /APP1/IFD/EXIF/{ushort = 41988} |             |
| 2     | /КСМП/ексиф: Дигиталзумратио    |             |



 

### <a name="write-paths"></a>Пути записи



| Номер | Путь                          | Формат диска |
|-------|-------------------------------|-------------|
| 1     | /APP1/IFD/EXIF/{ushort = 41988} |             |
| 2     | /КСМП/ексиф: Дигиталзумратио    |             |



 

### <a name="remove-paths"></a>Удалить пути



| Номер | Путь                          |
|-------|-------------------------------|
| 1     | /APP1/IFD/EXIF/{ushort = 41988} |
| 2     | /КСМП/ексиф: дигиталзумратио    |



 

### <a name="tiff-policies"></a>Политики TIFF

### <a name="read-paths"></a>Пути чтения



| Номер | Путь                           | Формат диска |
|-------|--------------------------------|-------------|
| 1     | /ИФД/ексиф/{ушорт = 41988}       |             |
| 2     | /ИФД/КСМП/ексиф: Дигиталзумратио |             |



 

### <a name="write-paths"></a>Пути записи



| Номер | Путь                           | Формат диска |
|-------|--------------------------------|-------------|
| 1     | /ИФД/ексиф/{ушорт = 41988}       |             |
| 2     | /ИФД/КСМП/ексиф: Дигиталзумратио |             |



 

### <a name="remove-paths"></a>Удалить пути



| Номер | Путь                           |
|-------|--------------------------------|
| 1     | /ИФД/ексиф/{ушорт = 41988}       |
| 2     | /ИФД/КСМП/ексиф: дигиталзумратио |



 

## <a name="remarks"></a>Remarks

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[System. photo. Дигиталзум](../properties/props-system-photo-digitalzoom.md)
</dt> </dl>

 

 
