---
description: Политика метаданных фотографии для свойства System. photo. Релатедсаундфиле.
ms.assetid: 3b212d90-7ae2-4b7c-b77a-2017490aca40
title: Политика метаданных фото для System. photo. Релатедсаундфиле
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07a29adb71f572868f21b1b8427e71b09616b24c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999123"
---
# <a name="systemphotorelatedsoundfile-photo-metadata-policy"></a>Политика метаданных фото для System. photo. Релатедсаундфиле

Политика метаданных фотографии для свойства [System. photo. релатедсаундфиле](../properties/props-system-photo-relatedsoundfile.md) .

### <a name="pkey"></a>PKEY

\_Релатедсаундфиле фото на PKEY \_

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



| Заказ | Путь                          | Формат диска |
|-------|-------------------------------|-------------|
| 1     | /APP1/IFD/EXIF/{ushort = 40964} | ascii       |
| 2     | /КСМП/ексиф: Релатедсаундфиле    | Юникод     |



 

### <a name="write-paths"></a>Пути записи



| Заказ | Путь                          | Формат диска |
|-------|-------------------------------|-------------|
| 1     | /APP1/IFD/EXIF/{ushort = 40964} | ascii       |
| 2     | /КСМП/ексиф: Релатедсаундфиле    | Юникод     |



 

### <a name="remove-paths"></a>Удалить пути



| Заказ | Путь                          |
|-------|-------------------------------|
| 1     | /APP1/IFD/EXIF/{ushort = 40964} |
| 2     | /КСМП/ексиф: Релатедсаундфиле    |



 

### <a name="tiff-policy"></a>Политика TIFF

### <a name="read-paths"></a>Пути чтения



| Заказ | Путь                           | Формат диска |
|-------|--------------------------------|-------------|
| 1     | /ИФД/ексиф/{ушорт = 40964}       | ascii       |
| 2     | /ИФД/КСМП/ексиф: Релатедсаундфиле | Юникод     |



 

### <a name="write-paths"></a>Пути записи



| Заказ | Путь                           | Формат диска |
|-------|--------------------------------|-------------|
| 1     | /ИФД/ексиф/{ушорт = 40964}       | ascii       |
| 2     | /ИФД/КСМП/ексиф: Релатедсаундфиле | Юникод     |



 

### <a name="remove-paths"></a>Удалить пути



| Заказ | Путь                           |
|-------|--------------------------------|
| 1     | /ИФД/ексиф/{ушорт = 40964}       |
| 2     | /ИФД/КСМП/ексиф: Релатедсаундфиле |



 

## <a name="remarks"></a>Комментарии

## <a name="related-topics"></a>См. также

<dl> <dt>

[System. photo. Релатедсаундфиле](../properties/props-system-photo-relatedsoundfile.md)
</dt> </dl>

 

 
