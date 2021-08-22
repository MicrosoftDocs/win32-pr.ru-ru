---
description: Политика метаданных фотографии для свойства System. GPS. долготы.
ms.assetid: 36539e20-d00c-4bbb-b9ee-1cf5e4b8df4b
title: Политика метаданных фотографии System. GPS. долготы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff05dd8ada6e10bbd3109187d34b220ff352ae984f92bd68281c56d3c1a29a76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119087192"
---
# <a name="systemgpslongitude-photo-metadata-policy"></a>Политика метаданных фотографии System. GPS. долготы

Политика метаданных фотографии для свойства [System. GPS. долготы](../properties/props-system-gps-longitude.md) .

### <a name="pkey"></a>PKEY

PKEY \_ GPS \_ Долгота

### <a name="containers"></a>Контейнеры

JPEG, TIFF

### <a name="read-only"></a>Только для чтения

Да

### <a name="output-propvariant-type"></a>Тип выходного ПРОПВАРИАНТ

VT \_ вектор \| VT \_ R8

### <a name="conflict-resolution-policy"></a>Политика разрешения конфликтов

Это значение можно записать с помощью записи в System. GPS. Лонгитуденумератор и System. GPS. Лонгитудеденоминатор. Он не может быть записан напрямую. Выверяются значения из разных схем.

### <a name="jpeg-policy"></a>Политика JPEG

### <a name="read-paths"></a>Пути чтения



| Номер | Путь                     | Формат диска |
|-------|--------------------------|-------------|
| 1     | /APP1/IFD/GPS/{ushort = 4} |             |
| 2     | /КСМП/ексиф: Гпслонгитуде   |             |



 

### <a name="write-paths"></a>Пути записи



| Номер | Путь                     | Формат диска |
|-------|--------------------------|-------------|
| 1     | /APP1/IFD/GPS/{ushort = 4} |             |
| 2     | /КСМП/ексиф: Гпслонгитуде   |             |



 

### <a name="remove-paths"></a>Удалить пути



| Номер | Путь                     |
|-------|--------------------------|
| 1     | /APP1/IFD/GPS/{ushort = 4} |
| 2     | /КСМП/ексиф: гпслонгитуде   |



 

### <a name="tiff-policies"></a>Политики TIFF

### <a name="read-paths"></a>Пути чтения



| Номер | Путь                       | Формат диска |
|-------|----------------------------|-------------|
| 1     | /ИФД/ГПС/{ушорт = 4}        |             |
| 2     | /ИФД/КСМП/ексиф: Гпслонгитуде |             |



 

### <a name="write-paths"></a>Пути записи



| Номер | Путь                       | Формат диска |
|-------|----------------------------|-------------|
| 1     | /ИФД/ГПС/{ушорт = 4}        |             |
| 2     | /ИФД/КСМП/ексиф: Гпслонгитуде |             |



 

### <a name="remove-paths"></a>Удалить пути



| Номер | Путь                       |
|-------|----------------------------|
| 1     | /ИФД/ГПС/{ушорт = 4}        |
| 2     | /ИФД/КСМП/ексиф: гпслонгитуде |



 

## <a name="remarks"></a>Remarks

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[System. GPS. Долгота](../properties/props-system-gps-longitude.md)
</dt> </dl>

 

 
