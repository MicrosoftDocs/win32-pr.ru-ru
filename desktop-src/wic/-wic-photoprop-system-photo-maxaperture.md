---
description: Политика метаданных фотографии для свойства System. photo. Максапертуре.
ms.assetid: 9d12d265-0b0a-44d9-bbf6-ca7d748382ee
title: Политика метаданных фото для System. photo. Максапертуре
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d692c12b9a5df584331a9a5ff4a82707d8549ab7891e1d9162eef318a77fe4d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118204716"
---
# <a name="systemphotomaxaperture-photo-metadata-policy"></a>Политика метаданных фото для System. photo. Максапертуре

Политика метаданных фотографии для свойства [System. photo. максапертуре](../properties/props-system-photo-maxaperture.md) .

### <a name="pkey"></a>PKEY

\_Максапертуре фото на PKEY \_

### <a name="containers"></a>Контейнеры

JPEG, TIFF

### <a name="read-only"></a>Только для чтения

Да

### <a name="output-propvariant-type"></a>Тип выходного ПРОПВАРИАНТ

VT \_ R8

### <a name="input-type"></a>Тип входных данных

Double

### <a name="conflict-resolution-policy"></a>Политика разрешения конфликтов

Это значение формируется из System. photo. Максапертуренумератор и System. photo. Максапертуреденоминатор. Он не может быть записан напрямую. Выверяются значения из разных схем.

### <a name="jpeg-policy"></a>Политика JPEG

### <a name="read-paths"></a>Пути чтения



| Номер | Путь                          | Формат диска |
|-------|-------------------------------|-------------|
| 1     | /APP1/IFD/EXIF/{ushort = 37381} |             |
| 2     | /КСМП/ексиф: Максапертуревалуе    |             |



 

### <a name="write-paths"></a>Пути записи



| Номер | Путь                          | Формат диска |
|-------|-------------------------------|-------------|
| 1     | /APP1/IFD/EXIF/{ushort = 37381} |             |
| 2     | /КСМП/ексиф: Максапертуревалуе    |             |



 

### <a name="remove-paths"></a>Удалить пути



| Номер | Путь                          |
|-------|-------------------------------|
| 1     | /APP1/IFD/EXIF/{ushort = 37381} |
| 2     | /КСМП/ексиф: максапертуревалуе    |



 

### <a name="tiff-policies"></a>Политики TIFF

### <a name="read-paths"></a>Пути чтения



| Номер | Путь                           | Формат диска |
|-------|--------------------------------|-------------|
| 1     | /ИФД/ексиф/{ушорт = 37381}       |             |
| 2     | /ИФД/КСМП/ексиф: Максапертуревалуе |             |



 

### <a name="write-paths"></a>Пути записи



| Номер | Путь                           | Формат диска |
|-------|--------------------------------|-------------|
| 1     | /ИФД/ексиф/{ушорт = 37381}       |             |
| 2     | /ИФД/КСМП/ексиф: Максапертуревалуе |             |



 

### <a name="remove-paths"></a>Удалить пути



| Номер | Путь                           |
|-------|--------------------------------|
| 1     | /ИФД/ексиф/{ушорт = 37381}       |
| 2     | /ИФД/КСМП/ексиф: максапертуревалуе |



 

## <a name="remarks"></a>Remarks

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[System. photo. Максапертуре](../properties/props-system-photo-maxaperture.md)
</dt> </dl>

 

 
