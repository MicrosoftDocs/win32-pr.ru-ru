---
description: Политика метаданных фотографии для свойства System. photo. Фокалленгс.
ms.assetid: a282c31f-00dd-4df5-9b93-300bb9bc8f2d
title: Политика метаданных фото для System. photo. Фокалленгс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfc7b36240713782c98d52e4fbf4dae5c0c06082
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712351"
---
# <a name="systemphotofocallength-photo-metadata-policy"></a>Политика метаданных фото для System. photo. Фокалленгс

Политика метаданных фотографии для свойства [System. photo. фокалленгс](../properties/props-system-photo-focallength.md) .

### <a name="pkey"></a>PKEY

\_Фокалленгс фото на PKEY \_

### <a name="containers"></a>Контейнеры

JPEG, TIFF

### <a name="read-only"></a>Только для чтения

Да

### <a name="output-propvariant-type"></a>Тип выходного ПРОПВАРИАНТ

VT \_ R8

### <a name="conflict-resolution-policy"></a>Политика разрешения конфликтов

Это значение формируется из System. photo. Фокалленгснумератор и System. photo. Фокалленгсденоминатор. Он не может быть записан напрямую. Выверяются значения из разных схем.

### <a name="jpeg-policy"></a>Политика JPEG

### <a name="read-paths"></a>Пути чтения



| Заказ | Путь                          | Формат диска |
|-------|-------------------------------|-------------|
| 1     | /APP1/IFD/EXIF/{ushort = 37386} |             |
| 2     | /КСМП/ексиф: Фокалленгс         |             |



 

### <a name="write-paths"></a>Пути записи



| Заказ | Путь                          | Формат диска |
|-------|-------------------------------|-------------|
| 1     | /APP1/IFD/EXIF/{ushort = 37386} |             |
| 2     | /КСМП/ексиф: Фокалленгс         |             |



 

### <a name="remove-paths"></a>Удалить пути



| Заказ | Путь                          |
|-------|-------------------------------|
| 1     | /APP1/IFD/EXIF/{ushort = 37386} |
| 2     | /КСМП/ексиф: фокалленгс         |



 

### <a name="tiff-policies"></a>Политики TIFF

### <a name="read-paths"></a>Пути чтения



| Заказ | Путь                      | Формат диска |
|-------|---------------------------|-------------|
| 1     | /ИФД/ексиф/{ушорт = 37386}  |             |
| 2     | /ИФД/КСМП/ексиф: Фокалленгс |             |



 

### <a name="write-paths"></a>Пути записи



| Заказ | Путь                      | Формат диска |
|-------|---------------------------|-------------|
| 1     | /ИФД/ексиф/{ушорт = 37386}  |             |
| 2     | /ИФД/КСМП/ексиф: Фокалленгс |             |



 

### <a name="remove-paths"></a>Удалить пути



| Заказ | Путь                      |
|-------|---------------------------|
| 1     | /ИФД/ексиф/{ушорт = 37386}  |
| 2     | /ИФД/КСМП/ексиф: фокалленгс |



 

## <a name="remarks"></a>Комментарии

## <a name="related-topics"></a>См. также

<dl> <dt>

[System. photo. Фокалленгс](../properties/props-system-photo-focallength.md)
</dt> </dl>

 

 
