---
description: Политика метаданных фотографии для свойства System. photo. яркость.
ms.assetid: 3fd73845-f1d9-468c-abf8-081109880974
title: Политика метаданных фотографии System. photo. яркость
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acd7328b4d40b8d1582dcc17b317b706b2695c73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999340"
---
# <a name="systemphotobrightness-photo-metadata-policy"></a>Политика метаданных фотографии System. photo. яркость

Политика метаданных фотографии для свойства [System. photo. яркость](../properties/props-system-photo-aperture.md) .

### <a name="pkey"></a>PKEY

\_Яркость фотографии \_ PKEY

### <a name="containers"></a>Контейнеры

JPEG, TIFF

### <a name="read-only"></a>Только для чтения

Да

### <a name="input-type"></a>Тип входных данных

Double

### <a name="conflict-resolution-policy"></a>Политика разрешения конфликтов

Это значение формируется из System. photo. Апертуренумератор и System. photo. Апертуреденоминатор. Он не может быть записан напрямую. Выверяются значения из разных схем.

### <a name="jpeg-policy"></a>Политика JPEG

### <a name="read-paths"></a>Пути чтения



| Заказ | Путь                          | Формат диска |
|-------|-------------------------------|-------------|
| 1     | /APP1/IFD/EXIF/{ushort = 37379} |             |
| 2     | /КСМП/ексиф: Бригхтнессвалуе     |             |



 

### <a name="write-paths"></a>Пути записи



| Заказ | Путь                          | Формат диска |
|-------|-------------------------------|-------------|
| 1     | /APP1/IFD/EXIF/{ushort = 37379} |             |
| 2     | /КСМП/ексиф: Бригхтнессвалуе     |             |



 

### <a name="remove-paths"></a>Удалить пути



| Заказ | Путь                          |
|-------|-------------------------------|
| 1     | /APP1/IFD/EXIF/{ushort = 37379} |
| 2     | /КСМП/ексиф: бригхтнессвалуе     |



 

### <a name="tiff-policies"></a>Политики TIFF

### <a name="read-paths"></a>Пути чтения



| Заказ | Путь                          | Формат диска |
|-------|-------------------------------|-------------|
| 1     | /ИФД/ексиф/{ушорт = 37379}      |             |
| 2     | /ИФД/КСМП/ексиф: Бригхтнессвалуе |             |



 

### <a name="write-paths"></a>Пути записи



| Заказ | Путь                          | Формат диска |
|-------|-------------------------------|-------------|
| 1     | /ИФД/ексиф/{ушорт = 37379}      |             |
| 2     | /ИФД/КСМП/ексиф: Бригхтнессвалуе |             |



 

### <a name="remove-paths"></a>Удалить пути



| Заказ | Путь                          |
|-------|-------------------------------|
| 1     | /ИФД/ексиф/{ушорт = 37379}      |
| 2     | /ИФД/КСМП/ексиф: бригхтнессвалуе |



 

## <a name="remarks"></a>Комментарии

## <a name="related-topics"></a>См. также

<dl> <dt>

[System. photo. яркость](../properties/props-system-photo-aperture.md)
</dt> </dl>

 

 
