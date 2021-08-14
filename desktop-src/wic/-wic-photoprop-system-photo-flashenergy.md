---
description: Политика метаданных фотографии для свойства System. photo. Флашенерги.
ms.assetid: d10a4de9-16fe-4920-aa7f-b2f95fb23045
title: Политика метаданных фото для System. photo. Флашенерги
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1faebdcd32eaae346a44de9d1fa19f6954cb9d74ee9d79a09645216660845d16
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118204933"
---
# <a name="systemphotoflashenergy-photo-metadata-policy"></a>Политика метаданных фото для System. photo. Флашенерги

Политика метаданных фотографии для свойства [System. photo. флашенерги](../properties/props-system-photo-flashenergy.md) .

### <a name="pkey"></a>PKEY

\_Флашенерги фото на PKEY \_

### <a name="containers"></a>Контейнеры

JPEG, TIFF

### <a name="read-only"></a>Только для чтения

Да

### <a name="input-type"></a>Тип входных данных

Double

### <a name="conflict-resolution-policy"></a>Политика разрешения конфликтов

Выверяются значения из разных схем.

### <a name="jpeg-policy"></a>Политика JPEG

### <a name="read-paths"></a>Пути чтения



| Номер | Путь                          | Формат диска |
|-------|-------------------------------|-------------|
| 1     | /APP1/IFD/EXIF/{ushort = 41483} |             |
| 2     | /КСМП/ексиф: Флашенерги         |             |



 

### <a name="write-paths"></a>Пути записи



| Номер | Путь                          | Формат диска |
|-------|-------------------------------|-------------|
| 1     | /APP1/IFD/EXIF/{ushort = 41483} |             |
| 2     | /КСМП/ексиф: Флашенерги         |             |



 

### <a name="remove-paths"></a>Удалить пути



| Номер | Путь                          |
|-------|-------------------------------|
| 1     | /APP1/IFD/EXIF/{ushort = 41483} |
| 2     | /КСМП/ексиф: флашенерги         |



 

### <a name="tiff-policies"></a>Политики TIFF

### <a name="read-paths"></a>Пути чтения



| Номер | Путь                      | Формат диска |
|-------|---------------------------|-------------|
| 1     | /ИФД/ексиф/{ушорт = 41483}  |             |
| 2     | /ИФД/КСМП/ексиф: Флашенерги |             |



 

### <a name="write-paths"></a>Пути записи



| Номер | Путь                      | Формат диска |
|-------|---------------------------|-------------|
| 1     | /ИФД/ексиф/{ушорт = 41483}  |             |
| 2     | /ИФД/КСМП/ексиф: Флашенерги |             |



 

### <a name="remove-paths"></a>Удалить пути



| Номер | Путь                      |
|-------|---------------------------|
| 1     | /ИФД/ексиф/{ушорт = 41483}  |
| 2     | /ИФД/КСМП/ексиф: флашенерги |



 

## <a name="remarks"></a>Remarks

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[System. photo. Флашенерги](../properties/props-system-photo-flashenergy.md)
</dt> </dl>

 

 
