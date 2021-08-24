---
description: Политика метаданных фотографии для свойства System. photo. яркость.
ms.assetid: 3fd73845-f1d9-468c-abf8-081109880974
title: Политика метаданных фотографии System. photo. яркость
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a78549d86d50f9b48359932698b02c827bd454a439476f2dc82627e4aab21d25
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119882064"
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

Тип Double

### <a name="conflict-resolution-policy"></a>Политика разрешения конфликтов

Это значение формируется из System. photo. Апертуренумератор и System. photo. Апертуреденоминатор. Он не может быть записан напрямую. Выверяются значения из разных схем.

### <a name="jpeg-policy"></a>Политика JPEG

### <a name="read-paths"></a>Пути чтения



| Номер | Путь                          | Формат диска |
|-------|-------------------------------|-------------|
| 1     | /APP1/IFD/EXIF/{ushort = 37379} |             |
| 2     | /КСМП/ексиф: Бригхтнессвалуе     |             |



 

### <a name="write-paths"></a>Пути записи



| Номер | Путь                          | Формат диска |
|-------|-------------------------------|-------------|
| 1     | /APP1/IFD/EXIF/{ushort = 37379} |             |
| 2     | /КСМП/ексиф: Бригхтнессвалуе     |             |



 

### <a name="remove-paths"></a>Удалить пути



| Номер | Путь                          |
|-------|-------------------------------|
| 1     | /APP1/IFD/EXIF/{ushort = 37379} |
| 2     | /КСМП/ексиф: бригхтнессвалуе     |



 

### <a name="tiff-policies"></a>Политики TIFF

### <a name="read-paths"></a>Пути чтения



| Номер | Путь                          | Формат диска |
|-------|-------------------------------|-------------|
| 1     | /ИФД/ексиф/{ушорт = 37379}      |             |
| 2     | /ИФД/КСМП/ексиф: Бригхтнессвалуе |             |



 

### <a name="write-paths"></a>Пути записи



| Номер | Путь                          | Формат диска |
|-------|-------------------------------|-------------|
| 1     | /ИФД/ексиф/{ушорт = 37379}      |             |
| 2     | /ИФД/КСМП/ексиф: Бригхтнессвалуе |             |



 

### <a name="remove-paths"></a>Удалить пути



| Номер | Путь                          |
|-------|-------------------------------|
| 1     | /ИФД/ексиф/{ушорт = 37379}      |
| 2     | /ИФД/КСМП/ексиф: бригхтнессвалуе |



 

## <a name="remarks"></a>Remarks

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[System. photo. яркость](../properties/props-system-photo-aperture.md)
</dt> </dl>

 

 
