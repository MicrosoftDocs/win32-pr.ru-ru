---
description: Политика метаданных фотографии для свойства System. photo. Flash.
ms.assetid: 24b400a4-f4c7-4b59-a9e3-8a20144cd52e
title: Политика метаданных фотографии System. photo. Flash
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba32a7b4dfcde564f6b0c0c9e175aa56786e1324080264c7c928398fe97e6a34
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119811734"
---
# <a name="systemphotoflash-photo-metadata-policy"></a>Политика метаданных фотографии System. photo. Flash

Политика метаданных фотографии для свойства [System. photo. Flash](../properties/props-system-photo-exposuretime.md) .

### <a name="pkey"></a>PKEY

\_Фото \_ -ВСПЫШКа PKEY

### <a name="containers"></a>Контейнеры

JPEG, TIFF

### <a name="read-only"></a>Только для чтения

Нет

### <a name="output-propvariant-type"></a>Тип выходного ПРОПВАРИАНТ

VT \_ UI1 (если исходная схема — XMP) или VT \_ UI2 (если исходная схема — EXIF)

\\lang1036

### <a name="input-type"></a>Тип входных данных

VT \_ UI1, VTUI2, VT \_ UI4

\\lang1033

### <a name="conflict-resolution-policy"></a>Политика разрешения конфликтов

Выверяются значения из разных схем.

### <a name="jpeg-policy"></a>Политика JPEG

### <a name="read-paths"></a>Пути чтения



| Номер | Путь                             | Формат диска |
|-------|----------------------------------|-------------|
| 1     | /APP1/IFD/EXIF/{ushort = 37385}    | ushort      |
| 2     | /КСМП/ <xmpstruct> EXIF: Flash |             |



 

### <a name="write-paths"></a>Пути записи



| Номер | Путь                             | Формат диска |
|-------|----------------------------------|-------------|
| 1     | /APP1/IFD/EXIF/{ushort = 37385}    | ushort      |
| 2     | /КСМП/ <xmpstruct> EXIF: Flash |             |



 

### <a name="remove-paths"></a>Удалить пути



| Номер | Путь                             |
|-------|----------------------------------|
| 1     | /APP1/IFD/EXIF/{ushort = 37385}    |
| 2     | /КСМП/ <xmpstruct> EXIF: Flash |



 

### <a name="tiff-policies"></a>Политики TIFF

### <a name="read-paths"></a>Пути чтения



| Номер | Путь                                 | Формат диска |
|-------|--------------------------------------|-------------|
| 1     | /ИФД/ексиф/{ушорт = 37385}             | ushort      |
| 2     | /ИФД/КСМП/ <xmpstruct> EXIF: Flash |             |



 

### <a name="write-paths"></a>Пути записи



| Номер | Путь                                 | Формат диска |
|-------|--------------------------------------|-------------|
| 1     | /ИФД/ексиф/{ушорт = 37385}             | ushort      |
| 2     | /ИФД/КСМП/ <xmpstruct> EXIF: Flash |             |



 

### <a name="remove-paths"></a>Удалить пути



| Номер | Путь                                 |
|-------|--------------------------------------|
| 1     | /ИФД/ексиф/{ушорт = 37385}             |
| 2     | /ИФД/КСМП/ <xmpstruct> EXIF: Flash |



 

## <a name="remarks"></a>Remarks

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[System. photo. Flash](../properties/props-system-photo-exposuretime.md)
</dt> </dl>

 

 
