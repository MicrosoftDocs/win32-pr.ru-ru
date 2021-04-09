---
description: Политика метаданных фотографии для свойства System. photo. Флашенерги.
ms.assetid: d10a4de9-16fe-4920-aa7f-b2f95fb23045
title: Политика метаданных фото для System. photo. Флашенерги
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c272b4d6d14bf2f2e81d0964a3dc4395ba62dc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081446"
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



| Заказ | Путь                          | Формат диска |
|-------|-------------------------------|-------------|
| 1     | /APP1/IFD/EXIF/{ushort = 41483} |             |
| 2     | /КСМП/ексиф: Флашенерги         |             |



 

### <a name="write-paths"></a>Пути записи



| Заказ | Путь                          | Формат диска |
|-------|-------------------------------|-------------|
| 1     | /APP1/IFD/EXIF/{ushort = 41483} |             |
| 2     | /КСМП/ексиф: Флашенерги         |             |



 

### <a name="remove-paths"></a>Удалить пути



| Заказ | Путь                          |
|-------|-------------------------------|
| 1     | /APP1/IFD/EXIF/{ushort = 41483} |
| 2     | /КСМП/ексиф: флашенерги         |



 

### <a name="tiff-policies"></a>Политики TIFF

### <a name="read-paths"></a>Пути чтения



| Заказ | Путь                      | Формат диска |
|-------|---------------------------|-------------|
| 1     | /ИФД/ексиф/{ушорт = 41483}  |             |
| 2     | /ИФД/КСМП/ексиф: Флашенерги |             |



 

### <a name="write-paths"></a>Пути записи



| Заказ | Путь                      | Формат диска |
|-------|---------------------------|-------------|
| 1     | /ИФД/ексиф/{ушорт = 41483}  |             |
| 2     | /ИФД/КСМП/ексиф: Флашенерги |             |



 

### <a name="remove-paths"></a>Удалить пути



| Заказ | Путь                      |
|-------|---------------------------|
| 1     | /ИФД/ексиф/{ушорт = 41483}  |
| 2     | /ИФД/КСМП/ексиф: флашенерги |



 

## <a name="remarks"></a>Комментарии

## <a name="related-topics"></a>См. также

<dl> <dt>

[System. photo. Флашенерги](../properties/props-system-photo-flashenergy.md)
</dt> </dl>

 

 
