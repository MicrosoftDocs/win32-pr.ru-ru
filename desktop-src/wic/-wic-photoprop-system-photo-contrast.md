---
description: Политика метаданных фотографии для свойства System. photo. контраста.
ms.assetid: c5e2589d-507c-4b92-9ada-7d64e7c45dd8
title: Политика метаданных фотографии System. photo. контраста
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1d6ed34854b525e9eaac2ff5ac7339a75ad10e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104547042"
---
# <a name="systemphotocontrast-photo-metadata-policy"></a>Политика метаданных фотографии System. photo. контраста

Политика метаданных фотографии для свойства [System. photo. контраста](../properties/props-system-photo-contrast.md) .

### <a name="pkey"></a>PKEY

\_Контрастность фото в PKEY \_

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
| 1     | /APP1/IFD/EXIF/{ushort = 41992} | ushort      |
| 2     | /КСМП/ексиф: контрастность            | Юникод     |



 

### <a name="write-paths"></a>Пути записи



| Заказ | Путь                          | Формат диска |
|-------|-------------------------------|-------------|
| 1     | /APP1/IFD/EXIF/{ushort = 41992} | ushort      |
| 2     | /КСМП/ексиф: контрастность            | Юникод     |



 

### <a name="remove-paths"></a>Удалить пути



| Заказ | Путь                          |
|-------|-------------------------------|
| 1     | /APP1/IFD/EXIF/{ushort = 41992} |
| 2     | /КСМП/ексиф: контрастность            |



 

### <a name="tiff-policies"></a>Политики TIFF

### <a name="read-paths"></a>Пути чтения



| Заказ | Путь                     | Формат диска |
|-------|--------------------------|-------------|
| 1     | /ИФД/ексиф/{ушорт = 41992} | ushort      |
| 2     | /ИФД/КСМП/ексиф: контрастность   | Юникод     |



 

### <a name="write-paths"></a>Пути записи



| Заказ | Путь                     | Формат диска |
|-------|--------------------------|-------------|
| 1     | /ИФД/ексиф/{ушорт = 41992} | ushort      |
| 2     | /ИФД/КСМП/ексиф: контрастность   | Юникод     |



 

### <a name="remove-paths"></a>Удалить пути



| Заказ | Путь                     |
|-------|--------------------------|
| 1     | /ИФД/ексиф/{ушорт = 41992} |
| 2     | /ИФД/КСМП/ексиф: контрастность   |



 

## <a name="remarks"></a>Комментарии

## <a name="related-topics"></a>См. также

<dl> <dt>

[System. photo. контраст](../properties/props-system-photo-contrast.md)
</dt> </dl>

 

 
