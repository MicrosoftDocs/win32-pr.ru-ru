---
description: Политика метаданных фотографии для свойства System. Image. Compression.
ms.assetid: 0fada41f-f6f8-43b3-ad65-79785e859c9c
title: Политика метаданных фотографии System. Image. Compression
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a32fdc55e2a6a962b1a3dfd9057ef25c89d942f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683568"
---
# <a name="systemimagecompression-photo-metadata-policy"></a>Политика метаданных фотографии System. Image. Compression

Политика метаданных фотографии для свойства [System. Image. Compression](../properties/props-system-image-compression.md) .

### <a name="pkey"></a>PKEY

\_Сжатие образа \_ PKEY

### <a name="containers"></a>Контейнеры

JPEG, TIFF

### <a name="read-only"></a>Только для чтения

Да

### <a name="output-propvariant-type"></a>Тип выходного ПРОПВАРИАНТ

VT \_ UI2

### <a name="input-type"></a>Тип входных данных

UShort

### <a name="conflict-resolution-policy"></a>Политика разрешения конфликтов

Выверяются значения из разных схем.

### <a name="jpeg-policy"></a>Политика JPEG

### <a name="read-paths"></a>Пути чтения



| Заказ | Путь                   | Формат диска |
|-------|------------------------|-------------|
| 1     | /APP1/IFD/{ushort = 259} | ushort      |
| 2     | /КСМП/Тифф: сжатие  | Юникод     |



 

### <a name="write-paths"></a>Пути записи



| Заказ | Путь                   | Формат диска |
|-------|------------------------|-------------|
| 1     | /APP1/IFD/{ushort = 259} | ushort      |
| 2     | /КСМП/Тифф: сжатие  | Юникод     |



 

### <a name="remove-paths"></a>Удалить пути



| Заказ | Путь                   |
|-------|------------------------|
| 1     | /APP1/IFD/{ushort = 259} |
| 2     | /КСМП/Тифф: сжатие  |



 

### <a name="tiff-policies"></a>Политики TIFF

### <a name="read-paths"></a>Пути чтения



| Заказ | Путь                      | Формат диска |
|-------|---------------------------|-------------|
| 1     | /ИФД/{ушорт = 259}         | ushort      |
| 2     | /ИФД/КСМП/Тифф: сжатие | Юникод     |



 

### <a name="write-paths"></a>Пути записи



| Заказ | Путь                      | Формат диска |
|-------|---------------------------|-------------|
| 1     | /ИФД/{ушорт = 259}         | ushort      |
| 2     | /ИФД/КСМП/Тифф: сжатие | Юникод     |



 

### <a name="remove-paths"></a>Удалить пути



| Заказ | Путь                      |
|-------|---------------------------|
| 1     | /ИФД/{ушорт = 259}         |
| 2     | /ИФД/КСМП/Тифф: сжатие |



 

## <a name="remarks"></a>Комментарии

## <a name="related-topics"></a>См. также

<dl> <dt>

[System. Image. Compression](../properties/props-system-image-compression.md)
</dt> </dl>

 

 
