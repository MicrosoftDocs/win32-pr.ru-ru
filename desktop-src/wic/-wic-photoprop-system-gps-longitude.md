---
description: Политика метаданных фотографии для свойства System. GPS. долготы.
ms.assetid: 36539e20-d00c-4bbb-b9ee-1cf5e4b8df4b
title: Политика метаданных фотографии System. GPS. долготы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25eb9869bc536f97adfc8f3c0f5b1f70c8bf030f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674275"
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



| Заказ | Путь                     | Формат диска |
|-------|--------------------------|-------------|
| 1     | /APP1/IFD/GPS/{ushort = 4} |             |
| 2     | /КСМП/ексиф: Гпслонгитуде   |             |



 

### <a name="write-paths"></a>Пути записи



| Заказ | Путь                     | Формат диска |
|-------|--------------------------|-------------|
| 1     | /APP1/IFD/GPS/{ushort = 4} |             |
| 2     | /КСМП/ексиф: Гпслонгитуде   |             |



 

### <a name="remove-paths"></a>Удалить пути



| Заказ | Путь                     |
|-------|--------------------------|
| 1     | /APP1/IFD/GPS/{ushort = 4} |
| 2     | /КСМП/ексиф: гпслонгитуде   |



 

### <a name="tiff-policies"></a>Политики TIFF

### <a name="read-paths"></a>Пути чтения



| Заказ | Путь                       | Формат диска |
|-------|----------------------------|-------------|
| 1     | /ИФД/ГПС/{ушорт = 4}        |             |
| 2     | /ИФД/КСМП/ексиф: Гпслонгитуде |             |



 

### <a name="write-paths"></a>Пути записи



| Заказ | Путь                       | Формат диска |
|-------|----------------------------|-------------|
| 1     | /ИФД/ГПС/{ушорт = 4}        |             |
| 2     | /ИФД/КСМП/ексиф: Гпслонгитуде |             |



 

### <a name="remove-paths"></a>Удалить пути



| Заказ | Путь                       |
|-------|----------------------------|
| 1     | /ИФД/ГПС/{ушорт = 4}        |
| 2     | /ИФД/КСМП/ексиф: гпслонгитуде |



 

## <a name="remarks"></a>Комментарии

## <a name="related-topics"></a>См. также

<dl> <dt>

[System. GPS. Долгота](../properties/props-system-gps-longitude.md)
</dt> </dl>

 

 
