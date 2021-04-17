---
description: Политика метаданных фотографии для свойства System. photo. Пеопленамес.
ms.assetid: 567d5542-fc7b-4d19-bc3c-b9d6e26e3387
title: Политика метаданных фото для System. photo. Пеопленамес
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c3de9f5adda67fcd0e555194500f109df078bdf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674131"
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



| Заказ | Путь                                                           | Формат диска |
|-------|----------------------------------------------------------------|-------------|
| 1     | /КСМП/ <xmpstruct> MP: RegionInfo/ <xmpbag> МПРИ: регионы | ushort      |



 

### <a name="write-paths"></a>Пути записи

Это свойство нельзя записать с помощью политики метаданных.

### <a name="remove-paths"></a>Удалить пути



| Заказ | Путь                                |
|-------|-------------------------------------|
| 1     | /КСМП/ <xmpstruct> MP: RegionInfo |



 

### <a name="tiff-policies"></a>Политики TIFF

### <a name="read-paths"></a>Пути чтения



| Заказ | Путь                                                               | Формат диска |
|-------|--------------------------------------------------------------------|-------------|
| 1     | /ИФД/КСМП/ <xmpstruct> MP: RegionInfo/ <xmpbag> МПРИ: регионы | ushort      |



 

### <a name="write-paths"></a>Пути записи

Это свойство нельзя записать с помощью политики метаданных.

### <a name="remove-paths"></a>Удалить пути



| Заказ | Путь                                    |
|-------|-----------------------------------------|
| 1     | /ИФД/КСМП/ <xmpstruct> MP: RegionInfo |



 

## <a name="remarks"></a>Комментарии

## <a name="related-topics"></a>См. также

<dl> <dt>

[System. photo. Программоде](../properties/props-system-photo-programmode.md)
</dt> </dl>

 

 
