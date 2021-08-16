---
description: Политика метаданных фотографии для свойства System. GPS. Дестбеаринг.
ms.assetid: ccc31b3d-27fd-4a8c-a304-852cf6114ec5
title: Политика метаданных фотографии System. GPS. Дестбеаринг
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 598ef1e759f75dfb4851f2f3f435b53db1f875421c3d21446ae3de33f688cefd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118205515"
---
# <a name="systemgpsdestbearing-photo-metadata-policy"></a>Политика метаданных фотографии System. GPS. Дестбеаринг

Политика метаданных фотографии для свойства [System. GPS. дестбеаринг](../properties/props-system-gps-destbearing.md) .

### <a name="pkey"></a>PKEY

PKEY \_ GPS \_ дестбеаринг

### <a name="containers"></a>Контейнеры

JPEG, TIFF

### <a name="read-only"></a>Только для чтения

Да

### <a name="output-propvariant-type"></a>Тип выходного ПРОПВАРИАНТ

VT \_ R8

### <a name="conflict-resolution-policy"></a>Политика разрешения конфликтов

Это значение можно записать с помощью записи в System. GPS. Дестбеарингнумератор и System. GPS. Дестбеарингденоминатор. Он не может быть записан напрямую. Выверяются значения из разных схем.

### <a name="jpeg-policy"></a>Политика JPEG

### <a name="read-paths"></a>Пути чтения



| Номер | Путь                      | Формат диска |
|-------|---------------------------|-------------|
| 1     | /APP1/IFD/GPS/{ushort = 24} |             |
| 2     | /КСМП/ексиф: Гпсдестбеаринг  |             |



 

### <a name="write-paths"></a>Пути записи



| Номер | Путь                      | Формат диска |
|-------|---------------------------|-------------|
| 1     | /APP1/IFD/GPS/{ushort = 24} |             |
| 2     | /КСМП/ексиф: Гпсдестбеаринг  |             |



 

### <a name="remove-paths"></a>Удалить пути



| Номер | Путь                      | Формат диска |
|-------|---------------------------|-------------|
| 1     | /APP1/IFD/GPS/{ushort = 24} |             |
| 2     | /КСМП/ексиф: гпсдестбеаринг  |             |



 

### <a name="tiff-policies"></a>Политики TIFF

### <a name="read-paths"></a>Пути чтения



| Номер | Путь                         | Формат диска |
|-------|------------------------------|-------------|
| 1     | /ИФД/ГПС/{ушорт = 24}         |             |
| 2     | /ИФД/КСМП/ексиф: Гпсдестбеаринг |             |



 

### <a name="write-paths"></a>Пути записи



| Номер | Путь                         | Формат диска |
|-------|------------------------------|-------------|
| 1     | /ИФД/ГПС/{ушорт = 24}         |             |
| 2     | /ИФД/КСМП/ексиф: Гпсдестбеаринг |             |



 

### <a name="remove-paths"></a>Удалить пути



| Номер | Путь                         |
|-------|------------------------------|
| 1     | /ИФД/ГПС/{ушорт = 24}         |
| 2     | /ИФД/КСМП/ексиф: гпсдестбеаринг |



 

## <a name="remarks"></a>Remarks

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[System. GPS. Дестбеаринг](../properties/props-system-gps-destbearing.md)
</dt> </dl>

 

 
