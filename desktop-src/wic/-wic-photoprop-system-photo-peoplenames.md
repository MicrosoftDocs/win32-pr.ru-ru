---
description: Политика метаданных фотографии для свойства System. photo. Пеопленамес.
ms.assetid: 567d5542-fc7b-4d19-bc3c-b9d6e26e3387
title: Политика метаданных фото для System. photo. Пеопленамес
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4118cc8242d6dfe8a91d0bcd2b6039095fdf180037f51205d3541b9aefa2cc0d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119087053"
---
# <a name="systemphotopeoplenames-photo-metadata-policy"></a>Политика метаданных фото для System. photo. Пеопленамес

Политика метаданных фотографии для свойства [System. photo. пеопленамес](../properties/props-system-photo-peoplenames.md) .

### <a name="pkey"></a>PKEY

\_Пеопленамес фото на PKEY \_

### <a name="containers"></a>Контейнеры

JPEG, TIFF

### <a name="read-only"></a>Только для чтения

Нет

### <a name="output-propvariant-type"></a>Тип выходного ПРОПВАРИАНТ

VT \_ Векторная \| \_ LPWSTR

### <a name="input-type"></a>Тип входных данных

стрингмулти

### <a name="conflict-resolution-policy"></a>Политика разрешения конфликтов

Выверяются значения из разных схем.

### <a name="jpeg-policy"></a>Политика JPEG

### <a name="read-paths"></a>Пути чтения



| Номер | Путь                                                           | Формат диска |
|-------|----------------------------------------------------------------|-------------|
| 1     | /КСМП/ <xmpstruct> MP: RegionInfo/ <xmpbag> МПРИ: регионы | ushort      |



 

### <a name="write-paths"></a>Пути записи

Это свойство нельзя записать с помощью политики метаданных.

### <a name="remove-paths"></a>Удалить пути



| Номер | Путь                                |
|-------|-------------------------------------|
| 1     | /КСМП/ <xmpstruct> MP: RegionInfo |



 

### <a name="tiff-policies"></a>Политики TIFF

### <a name="read-paths"></a>Пути чтения



| Номер | Путь                                                               | Формат диска |
|-------|--------------------------------------------------------------------|-------------|
| 1     | /ИФД/КСМП/ <xmpstruct> MP: RegionInfo/ <xmpbag> МПРИ: регионы | ushort      |



 

### <a name="write-paths"></a>Пути записи

Это свойство нельзя записать с помощью политики метаданных.

### <a name="remove-paths"></a>Удалить пути



| Номер | Путь                                    |
|-------|-----------------------------------------|
| 1     | /ИФД/КСМП/ <xmpstruct> MP: RegionInfo |



 

## <a name="remarks"></a>Remarks

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[System. photo. Программоде](../properties/props-system-photo-programmode.md)
</dt> </dl>

 

 
