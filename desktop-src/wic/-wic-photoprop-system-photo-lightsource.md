---
description: Политика метаданных фотографии для свойства System. photo. Лигхтсаурце.
ms.assetid: 051a49ad-bb4c-459f-ae52-dc359a03a14a
title: Политика метаданных фото для System. photo. Лигхтсаурце
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 195d165a6a929c8e0b4bf2dd165a5f22068a8b75e8ea4dfcddb5b8979900b035
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118204726"
---
# <a name="systemphotolightsource-photo-metadata-policy"></a>Политика метаданных фото для System. photo. Лигхтсаурце

Политика метаданных фотографии для свойства [System. photo. лигхтсаурце](../properties/props-system-photo-lightsource.md) .

### <a name="pkey"></a>PKEY

\_Лигхтсаурце фото на PKEY \_

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
| 1     | /APP1/IFD/EXIF/{ushort = 37384} | ushort      |
| 2     | /КСМП/ексиф: Лигхтсаурце         | Юникод     |



 

### <a name="write-paths"></a>Пути записи



| Номер | Путь                          | Формат диска |
|-------|-------------------------------|-------------|
| 1     | /APP1/IFD/EXIF/{ushort = 37384} | ushort      |
| 2     | /КСМП/ексиф: Лигхтсаурце         | Юникод     |



 

### <a name="remove-paths"></a>Удалить пути



| Номер | Путь                          |
|-------|-------------------------------|
| 1     | /APP1/IFD/EXIF/{ushort = 37384} |
| 2     | /КСМП/ексиф: лигхтсаурце         |



 

### <a name="tiff-policies"></a>Политики TIFF

### <a name="read-paths"></a>Пути чтения



| Номер | Путь                      | Формат диска |
|-------|---------------------------|-------------|
| 1     | /ИФД/ексиф/{ушорт = 37384}  | ushort      |
| 2     | /ИФД/КСМП/ексиф: Лигхтсаурце | Юникод     |



 

### <a name="write-paths"></a>Пути записи



| Номер | Путь                      | Формат диска |
|-------|---------------------------|-------------|
| 1     | /ИФД/ексиф/{ушорт = 37384}  | ushort      |
| 2     | /ИФД/КСМП/ексиф: Лигхтсаурце | Юникод     |



 

### <a name="remove-paths"></a>Удалить пути



| Номер | Путь                      |
|-------|---------------------------|
| 1     | /ИФД/ексиф/{ушорт = 37384}  |
| 2     | /ИФД/КСМП/ексиф: лигхтсаурце |



 

## <a name="remarks"></a>Remarks

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[System. photo. Лигхтсаурце](../properties/props-system-photo-lightsource.md)
</dt> </dl>

 

 
