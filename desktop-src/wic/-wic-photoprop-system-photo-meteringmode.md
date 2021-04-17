---
description: Политика метаданных фотографии для свойства System. photo. Метерингмоде.
ms.assetid: cb0bf0d5-eccf-4345-a242-76769c34e02d
title: Политика метаданных фото для System. photo. Метерингмоде
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12a4443521c84113e4e2a6f4c2b9b2b3f822ae90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674132"
---
# <a name="systemphotometeringmode-photo-metadata-policy"></a>Политика метаданных фото для System. photo. Метерингмоде

Политика метаданных фотографии для свойства [System. photo. метерингмоде](../properties/props-system-photo-meteringmode.md) .

### <a name="pkey"></a>PKEY

\_Метерингмоде фото на PKEY \_

### <a name="containers"></a>Контейнеры

JPEG, TIFF

### <a name="read-only"></a>Только для чтения

Нет

### <a name="output-propvariant-type"></a>Тип выходного ПРОПВАРИАНТ

VT \_ UI2

### <a name="input-type"></a>Тип входных данных

UShort

### <a name="conflict-resolution-policy"></a>Политика разрешения конфликтов

Выверяются значения из разных схем.

### <a name="jpeg-policy"></a>Политика JPEG

### <a name="read-paths"></a>Пути чтения



| Заказ | Путь                          | Формат диска |
|-------|-------------------------------|-------------|
| 1     | /APP1/IFD/EXIF/{ushort = 37383} | ushort      |
| 2     | /КСМП/ексиф: Метерингмоде        | Юникод     |



 

### <a name="write-paths"></a>Пути записи



| Заказ | Путь                          | Формат диска |
|-------|-------------------------------|-------------|
| 1     | /APP1/IFD/EXIF/{ushort = 37383} | ushort      |
| 2     | /КСМП/ексиф: Метерингмоде        | Юникод     |



 

### <a name="remove-paths"></a>Удалить пути



| Заказ | Путь                          |
|-------|-------------------------------|
| 1     | /APP1/IFD/EXIF/{ushort = 37383} |
| 2     | /КСМП/ексиф: метерингмоде        |



 

### <a name="tiff-policies"></a>Политики TIFF

### <a name="read-paths"></a>Пути чтения



| Заказ | Путь                       | Формат диска |
|-------|----------------------------|-------------|
| 1     | /ИФД/ексиф/{ушорт = 37383}   | ushort      |
| 2     | /ИФД/КСМП/ексиф: Метерингмоде | Юникод     |



 

### <a name="write-paths"></a>Пути записи



| Заказ | Путь                       | Формат диска |
|-------|----------------------------|-------------|
| 1     | /ИФД/ексиф/{ушорт = 37383}   | ushort      |
| 2     | /ИФД/КСМП/ексиф: Метерингмоде | Юникод     |



 

### <a name="remove-paths"></a>Удалить пути



| Заказ | Путь                       |
|-------|----------------------------|
| 1     | /ИФД/ексиф/{ушорт = 37383}   |
| 2     | /ИФД/КСМП/ексиф: метерингмоде |



 

## <a name="remarks"></a>Комментарии

## <a name="related-topics"></a>См. также

<dl> <dt>

[System. photo. Метерингмоде](../properties/props-system-photo-meteringmode.md)
</dt> </dl>

 

 
