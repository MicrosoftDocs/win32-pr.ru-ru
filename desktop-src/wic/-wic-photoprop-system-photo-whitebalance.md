---
description: Политика метаданных фотографии для свойства System. photo. Вхитебаланце.
ms.assetid: 7b3a31e6-a929-41e4-b7f0-c5b3beac2519
title: Политика метаданных фото для System. photo. Вхитебаланце
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc333cedcd4665ace37033452ec3c7f0336f13e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702741"
---
# <a name="systemphotowhitebalance-photo-metadata-policy"></a>Политика метаданных фото для System. photo. Вхитебаланце

Политика метаданных фотографии для свойства [System. photo. вхитебаланце](../properties/props-system-photo-whitebalance.md) .

### <a name="pkey"></a>PKEY

\_Вхитебаланце фото на PKEY \_

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
| 1     | /APP1/IFD/EXIF/{ushort = 41987} | ushort      |
| 2     | /КСМП/ексиф: Вхитебаланце        | Юникод     |



 

### <a name="write-paths"></a>Пути записи



| Заказ | Путь                          | Формат диска |
|-------|-------------------------------|-------------|
| 1     | /APP1/IFD/EXIF/{ushort = 41987} | ushort      |
| 2     | /КСМП/ексиф: Вхитебаланце        | Юникод     |



 

### <a name="remove-paths"></a>Удалить пути



| Заказ | Путь                          |
|-------|-------------------------------|
| 1     | /APP1/IFD/EXIF/{ushort = 41987} |
| 2     | /КСМП/ексиф: вхитебаланце        |



 

### <a name="tiff-policies"></a>Политики TIFF

### <a name="read-paths"></a>Пути чтения



| Заказ | Путь                       | Формат диска |
|-------|----------------------------|-------------|
| 1     | /ИФД/ексиф/{ушорт = 41987}   | ushort      |
| 2     | /ИФД/КСМП/ексиф: Вхитебаланце | Юникод     |



 

### <a name="write-paths"></a>Пути записи



| Заказ | Путь                       | Формат диска |
|-------|----------------------------|-------------|
| 1     | /ИФД/ексиф/{ушорт = 41987}   | ushort      |
| 2     | /ИФД/КСМП/ексиф: Вхитебаланце | Юникод     |



 

### <a name="remove-paths"></a>Удалить пути



| Заказ | Путь                       |
|-------|----------------------------|
| 1     | /ИФД/ексиф/{ушорт = 41987}   |
| 2     | /ИФД/КСМП/ексиф: вхитебаланце |



 

## <a name="remarks"></a>Комментарии

## <a name="related-topics"></a>См. также

<dl> <dt>

[System. photo. Вхитебаланце](../properties/props-system-photo-whitebalance.md)
</dt> </dl>

 

 
