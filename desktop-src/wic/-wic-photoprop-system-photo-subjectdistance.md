---
description: Политика метаданных фотографии для свойства System. photo. Субжектдистанце.
ms.assetid: 8d5acd7e-7227-4a79-890a-43e6dace3864
title: Политика метаданных фото для System. photo. Субжектдистанце
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86ec1868b1e33c4bcaaaea9a9203cc73733646cc82dade52c86b0c8caec4a704
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118964773"
---
# <a name="systemphotosubjectdistance-photo-metadata-policy"></a>Политика метаданных фото для System. photo. Субжектдистанце

Политика метаданных фотографии для свойства [System. photo. субжектдистанце](../properties/props-system-photo-subjectdistance.md) .

### <a name="pkey"></a>PKEY

\_Субжектдистанце фото на PKEY \_

### <a name="containers"></a>Контейнеры

JPEG, TIFF

### <a name="read-only"></a>Только для чтения

Да

### <a name="output-propvariant-type"></a>Тип выходного ПРОПВАРИАНТ

VT \_ R8

### <a name="conflict-resolution-policy"></a>Политика разрешения конфликтов

Это значение формируется из System. photo. Субжектдистанценумератор и System. photo. Субжектдистанцеденоминатор. Он не может быть записан напрямую. Выверяются значения из разных схем.

### <a name="jpeg-policy"></a>Политика JPEG

### <a name="read-paths"></a>Пути чтения



| Номер | Путь                          | Формат диска |
|-------|-------------------------------|-------------|
| 1     | /APP1/IFD/EXIF/{ushort = 37382} |             |
| 2     | /КСМП/ексиф: Субжектдистанце     |             |



 

### <a name="write-paths"></a>Пути записи



| Номер | Путь                          | Формат диска |
|-------|-------------------------------|-------------|
| 1     | /APP1/IFD/EXIF/{ushort = 37382} |             |
| 2     | /КСМП/ексиф: Субжектдистанце     |             |



 

### <a name="remove-paths"></a>Удалить пути



| Номер | Путь                          |
|-------|-------------------------------|
| 1     | /APP1/IFD/EXIF/{ushort = 37382} |
| 2     | /КСМП/ексиф: субжектдистанце     |



 

### <a name="tiff-policies"></a>Политики TIFF

### <a name="read-paths"></a>Пути чтения



| Номер | Путь                          | Формат диска |
|-------|-------------------------------|-------------|
| 1     | /ИФД/ексиф/{ушорт = 37382}      |             |
| 2     | /ИФД/КСМП/ексиф: Субжектдистанце |             |



 

### <a name="write-paths"></a>Пути записи



| Номер | Путь                          | Формат диска |
|-------|-------------------------------|-------------|
| 1     | /ИФД/ексиф/{ушорт = 37382}      |             |
| 2     | /ИФД/КСМП/ексиф: Субжектдистанце |             |



 

### <a name="remove-paths"></a>Удалить пути



| Номер | Путь                          |
|-------|-------------------------------|
| 1     | /ИФД/ексиф/{ушорт = 37382}      |
| 2     | /ИФД/КСМП/ексиф: субжектдистанце |



 

## <a name="remarks"></a>Remarks

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[System. photo. Субжектдистанце](../properties/props-system-photo-subjectdistance.md)
</dt> </dl>

 

 
