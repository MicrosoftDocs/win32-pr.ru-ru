---
description: Политика метаданных фотографии для свойства System. photo. контраста.
ms.assetid: c5e2589d-507c-4b92-9ada-7d64e7c45dd8
title: Политика метаданных фотографии System. photo. контраста
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4a9309ecab96a2244e08ebf05ff8896c792f7366c9db21d41072d2d94aacf47
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119087100"
---
# <a name="systemphotocontrast-photo-metadata-policy"></a>Политика метаданных фотографии System. photo. контраста

Политика метаданных фотографии для свойства [System. photo. контраста](../properties/props-system-photo-contrast.md) .

### <a name="pkey"></a>PKEY

\_Контрастность фото в PKEY \_

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
| 1     | /APP1/IFD/EXIF/{ushort = 41992} | ushort      |
| 2     | /КСМП/ексиф: контрастность            | Юникод     |



 

### <a name="write-paths"></a>Пути записи



| Номер | Путь                          | Формат диска |
|-------|-------------------------------|-------------|
| 1     | /APP1/IFD/EXIF/{ushort = 41992} | ushort      |
| 2     | /КСМП/ексиф: контрастность            | Юникод     |



 

### <a name="remove-paths"></a>Удалить пути



| Номер | Путь                          |
|-------|-------------------------------|
| 1     | /APP1/IFD/EXIF/{ushort = 41992} |
| 2     | /КСМП/ексиф: контрастность            |



 

### <a name="tiff-policies"></a>Политики TIFF

### <a name="read-paths"></a>Пути чтения



| Номер | Путь                     | Формат диска |
|-------|--------------------------|-------------|
| 1     | /ИФД/ексиф/{ушорт = 41992} | ushort      |
| 2     | /ИФД/КСМП/ексиф: контрастность   | Юникод     |



 

### <a name="write-paths"></a>Пути записи



| Номер | Путь                     | Формат диска |
|-------|--------------------------|-------------|
| 1     | /ИФД/ексиф/{ушорт = 41992} | ushort      |
| 2     | /ИФД/КСМП/ексиф: контрастность   | Юникод     |



 

### <a name="remove-paths"></a>Удалить пути



| Номер | Путь                     |
|-------|--------------------------|
| 1     | /ИФД/ексиф/{ушорт = 41992} |
| 2     | /ИФД/КСМП/ексиф: контрастность   |



 

## <a name="remarks"></a>Remarks

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[System. photo. контраст](../properties/props-system-photo-contrast.md)
</dt> </dl>

 

 
