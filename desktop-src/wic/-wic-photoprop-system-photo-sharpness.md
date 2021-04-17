---
description: Политика метаданных фотографии для свойства System. photo. четкости.
ms.assetid: 0fda4832-940b-4b5a-bd20-7e48c7800925
title: Политика метаданных фотографии System. photo. резкость
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48d635691f0b0e0801c1e37a006faa686aff0a8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674129"
---
# <a name="systemphotosharpness-photo-metadata-policy"></a>Политика метаданных фотографии System. photo. резкость

Политика метаданных фотографии для свойства [System. photo. четкости](../properties/props-system-photo-sharpness.md) .

### <a name="pkey"></a>PKEY

\_Четкость фото в PKEY \_

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



| Заказ | Путь                          | Формат диска |
|-------|-------------------------------|-------------|
| 1     | /APP1/IFD/EXIF/{ushort = 41994} | ushort      |
| 2     | /КСМП/ексиф: резкость           | Юникод     |



 

### <a name="write-paths"></a>Пути записи



| Заказ | Путь                          | Формат диска |
|-------|-------------------------------|-------------|
| 1     | /APP1/IFD/EXIF/{ushort = 41994} | ushort      |
| 2     | /КСМП/ексиф: резкость           | Юникод     |



 

### <a name="remove-paths"></a>Удалить пути



| Заказ | Путь                          |
|-------|-------------------------------|
| 1     | /APP1/IFD/EXIF/{ushort = 41994} |
| 2     | /КСМП/ексиф: резкость           |



 

### <a name="tiff-policies"></a>Политики TIFF

### <a name="read-paths"></a>Пути чтения



| Заказ | Путь                     | Формат диска |
|-------|--------------------------|-------------|
| 1     | /ИФД/ексиф/{ушорт = 41994} | ushort      |
| 2     | /ИФД/КСМП/ексиф: резкость  | Юникод     |



 

### <a name="write-paths"></a>Пути записи



| Заказ | Путь                     | Формат диска |
|-------|--------------------------|-------------|
| 1     | /ИФД/ексиф/{ушорт = 41994} | ushort      |
| 2     | /ИФД/КСМП/ексиф: резкость  | Юникод     |



 

### <a name="remove-paths"></a>Удалить пути



| Заказ | Путь                     |
|-------|--------------------------|
| 1     | /ИФД/ексиф/{ушорт = 41994} |
| 2     | /ИФД/КСМП/ексиф: резкость  |



 

## <a name="remarks"></a>Комментарии

## <a name="related-topics"></a>См. также

<dl> <dt>

[System. photo. резкость](../properties/props-system-photo-sharpness.md)
</dt> </dl>

 

 
