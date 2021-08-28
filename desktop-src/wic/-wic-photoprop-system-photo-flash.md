---
description: Политика метаданных фотографии для свойства System. photo. Flash.
ms.assetid: 24b400a4-f4c7-4b59-a9e3-8a20144cd52e
title: Политика метаданных фотографии System. photo. Flash
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a7798e88c40193cac5c577f1960eee96fc2d868
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122880075"
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



| Порядок | путь                             | Формат диска |
|-------|----------------------------------|-------------|
| 1     | /APP1/IFD/EXIF/{ushort = 37385}    | ushort      |
| 2     | /КСМП/ &lt; ксмпструкт &gt; EXIF: Flash |             |



 

### <a name="write-paths"></a>Пути записи



| Порядок | путь                             | Формат диска |
|-------|----------------------------------|-------------|
| 1     | /APP1/IFD/EXIF/{ushort = 37385}    | ushort      |
| 2     | /КСМП/ &lt; ксмпструкт &gt; EXIF: Flash |             |



 

### <a name="remove-paths"></a>Удалить пути



| Порядок | путь                             |
|-------|----------------------------------|
| 1     | /APP1/IFD/EXIF/{ushort = 37385}    |
| 2     | /КСМП/ &lt; ксмпструкт &gt; EXIF: Flash |



 

### <a name="tiff-policies"></a>Политики TIFF

### <a name="read-paths"></a>Пути чтения



| Порядок | путь                                 | Формат диска |
|-------|--------------------------------------|-------------|
| 1     | /ИФД/ексиф/{ушорт = 37385}             | ushort      |
| 2     | /ИФД/КСМП/ &lt; ксмпструкт &gt; EXIF: Flash |             |



 

### <a name="write-paths"></a>Пути записи



| Порядок | путь                                 | Формат диска |
|-------|--------------------------------------|-------------|
| 1     | /ИФД/ексиф/{ушорт = 37385}             | ushort      |
| 2     | /ИФД/КСМП/ &lt; ксмпструкт &gt; EXIF: Flash |             |



 

### <a name="remove-paths"></a>Удалить пути



| Порядок | путь                                 |
|-------|--------------------------------------|
| 1     | /ИФД/ексиф/{ушорт = 37385}             |
| 2     | /ИФД/КСМП/ &lt; ксмпструкт &gt; EXIF: Flash |



 

## <a name="remarks"></a>Комментарии

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[System. photo. Flash](../properties/props-system-photo-exposuretime.md)
</dt> </dl>

 

 
