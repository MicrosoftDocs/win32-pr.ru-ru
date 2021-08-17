---
description: Политика метаданных фотографии для свойства System. photo. Метерингмоде.
ms.assetid: cb0bf0d5-eccf-4345-a242-76769c34e02d
title: Политика метаданных фото для System. photo. Метерингмоде
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 424b14fa6216d5c88c350512d1583b311f92ef2f487e604760b1836b296d3bf2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118964783"
---
# <a name="systemphotometeringmode-photo-metadata-policy"></a>Политика метаданных фото для System. photo. Метерингмоде

Политика метаданных фотографии для свойства [System. photo. метерингмоде](../properties/props-system-photo-meteringmode.md) .

### <a name="pkey"></a>PKEY

\_Метерингмоде фото на PKEY \_

### <a name="containers"></a>Контейнеры

JPEG, TIFF

### <a name="read-only"></a>Только для чтения

Нет

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
| 1     | /APP1/IFD/EXIF/{ushort = 37383} | ushort      |
| 2     | /КСМП/ексиф: Метерингмоде        | Юникод     |



 

### <a name="write-paths"></a>Пути записи



| Номер | Путь                          | Формат диска |
|-------|-------------------------------|-------------|
| 1     | /APP1/IFD/EXIF/{ushort = 37383} | ushort      |
| 2     | /КСМП/ексиф: Метерингмоде        | Юникод     |



 

### <a name="remove-paths"></a>Удалить пути



| Номер | Путь                          |
|-------|-------------------------------|
| 1     | /APP1/IFD/EXIF/{ushort = 37383} |
| 2     | /КСМП/ексиф: метерингмоде        |



 

### <a name="tiff-policies"></a>Политики TIFF

### <a name="read-paths"></a>Пути чтения



| Номер | Путь                       | Формат диска |
|-------|----------------------------|-------------|
| 1     | /ИФД/ексиф/{ушорт = 37383}   | ushort      |
| 2     | /ИФД/КСМП/ексиф: Метерингмоде | Юникод     |



 

### <a name="write-paths"></a>Пути записи



| Номер | Путь                       | Формат диска |
|-------|----------------------------|-------------|
| 1     | /ИФД/ексиф/{ушорт = 37383}   | ushort      |
| 2     | /ИФД/КСМП/ексиф: Метерингмоде | Юникод     |



 

### <a name="remove-paths"></a>Удалить пути



| Номер | Путь                       |
|-------|----------------------------|
| 1     | /ИФД/ексиф/{ушорт = 37383}   |
| 2     | /ИФД/КСМП/ексиф: метерингмоде |



 

## <a name="remarks"></a>Remarks

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[System. photo. Метерингмоде](../properties/props-system-photo-meteringmode.md)
</dt> </dl>

 

 
