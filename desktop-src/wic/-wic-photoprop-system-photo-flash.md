---
description: Политика метаданных фотографии для свойства System. photo. Flash.
ms.assetid: 24b400a4-f4c7-4b59-a9e3-8a20144cd52e
title: Политика метаданных фотографии System. photo. Flash
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0302e0f310d2f9a6a4390b0d4856578cc2f43e93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674003"
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



| Заказ | Путь                             | Формат диска |
|-------|----------------------------------|-------------|
| 1     | /APP1/IFD/EXIF/{ushort = 37385}    | ushort      |
| 2     | /КСМП/ <xmpstruct> EXIF: Flash |             |



 

### <a name="write-paths"></a>Пути записи



| Заказ | Путь                             | Формат диска |
|-------|----------------------------------|-------------|
| 1     | /APP1/IFD/EXIF/{ushort = 37385}    | ushort      |
| 2     | /КСМП/ <xmpstruct> EXIF: Flash |             |



 

### <a name="remove-paths"></a>Удалить пути



| Заказ | Путь                             |
|-------|----------------------------------|
| 1     | /APP1/IFD/EXIF/{ushort = 37385}    |
| 2     | /КСМП/ <xmpstruct> EXIF: Flash |



 

### <a name="tiff-policies"></a>Политики TIFF

### <a name="read-paths"></a>Пути чтения



| Заказ | Путь                                 | Формат диска |
|-------|--------------------------------------|-------------|
| 1     | /ИФД/ексиф/{ушорт = 37385}             | ushort      |
| 2     | /ИФД/КСМП/ <xmpstruct> EXIF: Flash |             |



 

### <a name="write-paths"></a>Пути записи



| Заказ | Путь                                 | Формат диска |
|-------|--------------------------------------|-------------|
| 1     | /ИФД/ексиф/{ушорт = 37385}             | ushort      |
| 2     | /ИФД/КСМП/ <xmpstruct> EXIF: Flash |             |



 

### <a name="remove-paths"></a>Удалить пути



| Заказ | Путь                                 |
|-------|--------------------------------------|
| 1     | /ИФД/ексиф/{ушорт = 37385}             |
| 2     | /ИФД/КСМП/ <xmpstruct> EXIF: Flash |



 

## <a name="remarks"></a>Комментарии

## <a name="related-topics"></a>См. также

<dl> <dt>

[System. photo. Flash](../properties/props-system-photo-exposuretime.md)
</dt> </dl>

 

 
