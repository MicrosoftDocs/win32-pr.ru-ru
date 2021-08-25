---
description: Политика метаданных фотографии для свойства System. photo. Ексифверсион.
ms.assetid: 0f9c5ea8-918f-4101-8492-3f408145a73e
title: Политика метаданных фото для System. photo. Ексифверсион
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0eee0fdac7ba8e86321d4a055cb6c37c4e9c7bad3f5bcfced548cc2485b3347c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119882034"
---
# <a name="systemphotoexifversion-photo-metadata-policy"></a>Политика метаданных фото для System. photo. Ексифверсион

Политика метаданных фотографии для свойства [System. photo. ексифверсион](../properties/props-system-photo-exifversion.md) .

### <a name="pkey"></a>PKEY

\_Ексифверсион фото на PKEY \_

### <a name="containers"></a>Контейнеры

JPEG, TIFF

### <a name="read-only"></a>Только для чтения

Нет

### <a name="output-propvariant-type"></a>Тип выходного ПРОПВАРИАНТ

VT \_ LPWSTR

### <a name="input-type"></a>Тип входных данных

Строка.

### <a name="conflict-resolution-policy"></a>Политика разрешения конфликтов

Выверяются значения из разных схем.

### <a name="jpeg-policy"></a>Политика JPEG

### <a name="read-paths"></a>Пути чтения



| Номер | Путь                          | Формат диска   |
|-------|-------------------------------|---------------|
| 1     | /APP1/IFD/EXIF/{ushort = 36864} | \_версия EXIF |
| 2     | /КСМП/ексиф: Ексифверсион         | Юникод       |



 

### <a name="write-paths"></a>Пути записи



| Номер | Путь                          | Формат диска   |
|-------|-------------------------------|---------------|
| 1     | /APP1/IFD/EXIF/{ushort = 36864} | \_версия EXIF |
| 2     | /КСМП/ексиф: Ексифверсион         | Юникод       |



 

### <a name="remove-paths"></a>Удалить пути



| Номер | Путь                          |
|-------|-------------------------------|
| 1     | /APP1/IFD/EXIF/{ushort = 36864} |
| 2     | /КСМП/ексиф: Ексифверсион         |



 

### <a name="tiff-policy"></a>Политика TIFF

### <a name="read-paths"></a>Пути чтения



| Номер | Путь                      | Формат диска   |
|-------|---------------------------|---------------|
| 1     | /ИФД/ексиф/{ушорт = 36864}  | \_версия EXIF |
| 2     | /ИФД/КСМП/ексиф: Ексифверсион | Юникод       |



 

### <a name="write-paths"></a>Пути записи



| Номер | Путь                      | Формат диска   |
|-------|---------------------------|---------------|
| 1     | /ИФД/ексиф/{ушорт = 36864}  | \_версия EXIF |
| 2     | /ИФД/КСМП/ексиф: Ексифверсион | Юникод       |



 

### <a name="remove-paths"></a>Удалить пути



| Номер | Путь                      |
|-------|---------------------------|
| 1     | /ИФД/ексиф/{ушорт = 36864}  |
| 2     | /ИФД/КСМП/ексиф: Ексифверсион |



 

## <a name="remarks"></a>Remarks

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[System. photo. Ексифверсион](../properties/props-system-photo-exifversion.md)
</dt> </dl>

 

 
