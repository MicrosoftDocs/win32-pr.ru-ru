---
description: Политика метаданных фотографии для свойства System. photo. насыщенности.
ms.assetid: 1dbb7515-7022-404c-928a-9eb09e43e7a7
title: Политика метаданных фотографии System. photo. насыщенности
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1be1c5be7a0663d5f57823dcb704b843f56e6076713de3682e4b12d6b533ff48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119087017"
---
# <a name="systemphotosaturation-photo-metadata-policy"></a>Политика метаданных фотографии System. photo. насыщенности

Политика метаданных фотографии для свойства [System. photo. насыщенности](../properties/props-system-photo-saturation.md) .

### <a name="pkey"></a>PKEY

\_ \_ Насыщенность фото PKEY

### <a name="containers"></a>Контейнеры

JPEG, TIFF

### <a name="read-only"></a>Только для чтения

Нет

### <a name="output-propvariant-type"></a>Тип выходного ПРОПВАРИАНТ

VT \_ UI4

### <a name="input-type"></a>Тип входных данных

UShort

### <a name="conflict-resolution-policy"></a>Политика разрешения конфликтов

Выверяются значения из разных схем.

### <a name="jpeg-policy"></a>Политика JPEG

### <a name="read-paths"></a>Пути чтения



| Номер | Путь                          | Формат диска |
|-------|-------------------------------|-------------|
| 1     | /APP1/IFD/EXIF/{ushort = 41993} | ushort      |
| 2     | /КСМП/ексиф: насыщенность          | Юникод     |



 

### <a name="write-paths"></a>Пути записи



| Номер | Путь                          | Формат диска |
|-------|-------------------------------|-------------|
| 1     | /APP1/IFD/EXIF/{ushort = 41993} | ushort      |
| 2     | /КСМП/ексиф: насыщенность          | Юникод     |



 

### <a name="remove-paths"></a>Удалить пути



| Номер | Путь                          |
|-------|-------------------------------|
| 1     | /APP1/IFD/EXIF/{ushort = 41993} |
| 2     | /КСМП/ексиф: насыщенность          |



 

### <a name="tiff-policies"></a>Политики TIFF

### <a name="read-paths"></a>Пути чтения



| Номер | Путь                     | Формат диска |
|-------|--------------------------|-------------|
| 1     | /ИФД/ексиф/{ушорт = 41993} | ushort      |
| 2     | /ИФД/КСМП/ексиф: насыщенность | Юникод     |



 

### <a name="write-paths"></a>Пути записи



| Номер | Путь                     | Формат диска |
|-------|--------------------------|-------------|
| 1     | /ИФД/ексиф/{ушорт = 41993} | ushort      |
| 2     | /ИФД/КСМП/ексиф: насыщенность | Юникод     |



 

### <a name="remove-paths"></a>Удалить пути



| Номер | Путь                     |
|-------|--------------------------|
| 1     | /ИФД/ексиф/{ушорт = 41993} |
| 2     | /ИФД/КСМП/ексиф: насыщенность |



 

## <a name="remarks"></a>Remarks

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[System. photo. насыщенность](../properties/props-system-photo-saturation.md)
</dt> </dl>

 

 
