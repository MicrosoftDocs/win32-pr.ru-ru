---
description: Политика метаданных фотографии для свойства System. Image. Ресолутионунит.
ms.assetid: b8b744bd-976b-4648-a04b-33607467d6ac
title: Политика метаданных фотографии System. Image. Ресолутионунит
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d954df0b7efe9501cf25c33a54cd4296fb03f3c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702306"
---
# <a name="systemimageresolutionunit-photo-metadata-policy"></a>Политика метаданных фотографии System. Image. Ресолутионунит

Политика метаданных фотографии для свойства [System. Image. ресолутионунит](../properties/props-system-image-resolutionunit.md) .

### <a name="pkey"></a>PKEY

\_Ресолутионунит образа \_ PKEY

### <a name="containers"></a>Контейнеры

JPEG, TIFF

### <a name="read-only"></a>Только для чтения

Да.

### <a name="output-propvariant-type"></a>Тип выходного ПРОПВАРИАНТ

VT \_ I2

### <a name="input-type"></a>Тип входных данных

UShort

### <a name="conflict-resolution-policy"></a>Политика разрешения конфликтов

Выверяются значения из разных схем.

### <a name="jpeg-policy"></a>Политика JPEG

### <a name="read-paths"></a>Пути чтения



| Заказ | Путь                     | Формат диска |
|-------|--------------------------|-------------|
| 1     | /APP1/IFD/{ushort = 296}   | ushort      |
| 2     | /КСМП/Тифф: Ресолутионунит | Юникод     |



 

### <a name="write-paths"></a>Пути записи



| Заказ | Путь                     | Формат диска |
|-------|--------------------------|-------------|
| 1     | /APP1/IFD/{ushort = 296}   | ushort      |
| 2     | /КСМП/Тифф: Ресолутионунит | Юникод     |



 

### <a name="remove-paths"></a>Удалить пути



| Заказ | Путь                     |
|-------|--------------------------|
| 1     | /APP1/IFD/{ushort = 296}   |
| 2     | /КСМП/Тифф: ресолутионунит |



 

### <a name="tiff-policies"></a>Политики TIFF

### <a name="read-paths"></a>Пути чтения



| Заказ | Путь                         | Формат диска |
|-------|------------------------------|-------------|
| 1     | /ИФД/{ушорт = 296}            | ushort      |
| 2     | /ИФД/КСМП/Тифф: Ресолутионунит | Юникод     |



 

### <a name="write-paths"></a>Пути записи



| Заказ | Путь                         | Формат диска |
|-------|------------------------------|-------------|
| 1     | /ИФД/{ушорт = 296}            | ushort      |
| 2     | /ИФД/КСМП/Тифф: Ресолутионунит | Юникод     |



 

### <a name="remove-paths"></a>Удалить пути



| Заказ | Путь                         |
|-------|------------------------------|
| 1     | /ИФД/{ушорт = 296}            |
| 2     | /ИФД/КСМП/Тифф: ресолутионунит |



 

## <a name="remarks"></a>Комментарии

## <a name="related-topics"></a>См. также

<dl> <dt>

[System. Image. Ресолутионунит](../properties/props-system-image-resolutionunit.md)
</dt> </dl>

 

 
