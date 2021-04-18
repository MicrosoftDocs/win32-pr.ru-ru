---
description: Политика метаданных фотографии для свойства System. photo. Експосуретиме.
ms.assetid: 26f6ff27-b326-46f8-b4be-b091acbec575
title: Политика метаданных фото для System. photo. Експосуретиме
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea9078befd0cbc26272ff14ae023b1b22cb4f0f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674004"
---
# <a name="systemphotoexposuretime-photo-metadata-policy"></a>Политика метаданных фото для System. photo. Експосуретиме

Политика метаданных фотографии для свойства [System. photo. експосуретиме](../properties/props-system-photo-exposuretime.md) .

### <a name="pkey"></a>PKEY

\_Експосуретиме фото на PKEY \_

### <a name="containers"></a>Контейнеры

JPEG, TIFF

### <a name="read-only"></a>Только для чтения

Да

### <a name="output-propvariant-type"></a>Тип выходного ПРОПВАРИАНТ

VT \_ R8

### <a name="conflict-resolution-policy"></a>Политика разрешения конфликтов

Это значение формируется из System. photo. Експосуретименумератор и System. photo. Експосуретимеденоминатор. Он не может быть записан напрямую. Выверяются значения из разных схем.

### <a name="jpeg-policy"></a>Политика JPEG

### <a name="read-paths"></a>Пути чтения



| Заказ | Путь                          | Формат диска |
|-------|-------------------------------|-------------|
| 1     | /APP1/IFD/EXIF/{ushort = 33434} |             |
| 2     | /КСМП/ексиф: Експосуретиме        |             |



 

### <a name="write-paths"></a>Пути записи



| Заказ | Путь                          | Формат диска |
|-------|-------------------------------|-------------|
| 1     | /APP1/IFD/EXIF/{ushort = 33434} |             |
| 2     | /КСМП/ексиф: Експосуретиме        |             |



 

### <a name="remove-paths"></a>Удалить пути



| Заказ | Путь                          |
|-------|-------------------------------|
| 1     | /APP1/IFD/EXIF/{ushort = 33434} |
| 2     | /КСМП/ексиф: експосуретиме        |



 

### <a name="tiff-policies"></a>Политики TIFF

### <a name="read-paths"></a>Пути чтения



| Заказ | Путь                       | Формат диска |
|-------|----------------------------|-------------|
| 1     | /ИФД/ексиф/{ушорт = 33434}   |             |
| 2     | /ИФД/КСМП/ексиф: Експосуретиме |             |



 

### <a name="write-paths"></a>Пути записи



| Заказ | Путь                       | Формат диска |
|-------|----------------------------|-------------|
| 1     | /ИФД/ексиф/{ушорт = 33434}   |             |
| 2     | /ИФД/КСМП/ексиф: Експосуретиме |             |



 

### <a name="remove-paths"></a>Удалить пути



| Заказ | Путь                       |
|-------|----------------------------|
| 1     | /ИФД/ексиф/{ушорт = 33434}   |
| 2     | /ИФД/КСМП/ексиф: експосуретиме |



 

## <a name="remarks"></a>Комментарии

## <a name="related-topics"></a>См. также

<dl> <dt>

[System. photo. Експосуретиме](../properties/props-system-photo-exposuretime.md)
</dt> </dl>

 

 
