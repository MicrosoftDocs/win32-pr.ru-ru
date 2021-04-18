---
description: Политика метаданных фотографии для свойства System. photo. Лигхтсаурце.
ms.assetid: 051a49ad-bb4c-459f-ae52-dc359a03a14a
title: Политика метаданных фото для System. photo. Лигхтсаурце
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec9b3d31f01cdd2bea8d3fabbbc730a41f1fb0da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546607"
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



| Заказ | Путь                          | Формат диска |
|-------|-------------------------------|-------------|
| 1     | /APP1/IFD/EXIF/{ushort = 37384} | ushort      |
| 2     | /КСМП/ексиф: Лигхтсаурце         | Юникод     |



 

### <a name="write-paths"></a>Пути записи



| Заказ | Путь                          | Формат диска |
|-------|-------------------------------|-------------|
| 1     | /APP1/IFD/EXIF/{ushort = 37384} | ushort      |
| 2     | /КСМП/ексиф: Лигхтсаурце         | Юникод     |



 

### <a name="remove-paths"></a>Удалить пути



| Заказ | Путь                          |
|-------|-------------------------------|
| 1     | /APP1/IFD/EXIF/{ushort = 37384} |
| 2     | /КСМП/ексиф: лигхтсаурце         |



 

### <a name="tiff-policies"></a>Политики TIFF

### <a name="read-paths"></a>Пути чтения



| Заказ | Путь                      | Формат диска |
|-------|---------------------------|-------------|
| 1     | /ИФД/ексиф/{ушорт = 37384}  | ushort      |
| 2     | /ИФД/КСМП/ексиф: Лигхтсаурце | Юникод     |



 

### <a name="write-paths"></a>Пути записи



| Заказ | Путь                      | Формат диска |
|-------|---------------------------|-------------|
| 1     | /ИФД/ексиф/{ушорт = 37384}  | ushort      |
| 2     | /ИФД/КСМП/ексиф: Лигхтсаурце | Юникод     |



 

### <a name="remove-paths"></a>Удалить пути



| Заказ | Путь                      |
|-------|---------------------------|
| 1     | /ИФД/ексиф/{ушорт = 37384}  |
| 2     | /ИФД/КСМП/ексиф: лигхтсаурце |



 

## <a name="remarks"></a>Комментарии

## <a name="related-topics"></a>См. также

<dl> <dt>

[System. photo. Лигхтсаурце](../properties/props-system-photo-lightsource.md)
</dt> </dl>

 

 
