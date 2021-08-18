---
description: Политика метаданных фотографии для свойства System. GPS. Дестлонгитуде.
ms.assetid: 885a522d-e1bf-43fb-a996-97e725b6cf0c
title: Политика метаданных фотографии System. GPS. Дестлонгитуде
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 917c65dbd580b00cf25603e04050386383967e3a70c1896405346652667ef5f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119087845"
---
# <a name="systemgpsdestlongitude-photo-metadata-policy"></a>Политика метаданных фотографии System. GPS. Дестлонгитуде

Политика метаданных фотографии для свойства [System. GPS. дестлонгитуде](../properties/props-system-gps-destlongitude.md) .

### <a name="pkey"></a>PKEY

PKEY \_ GPS \_ дестлонгитуде

### <a name="containers"></a>Контейнеры

JPEG, TIFF

### <a name="read-only"></a>Только для чтения

Да

### <a name="output-propvariant-type"></a>Тип выходного ПРОПВАРИАНТ

VT \_ вектор \| VT \_ R8

### <a name="input-propvariant-type"></a>Тип входного ПРОПВАРИАНТ

VT \_ вектор \| VT \_ R8

### <a name="conflict-resolution-policy"></a>Политика разрешения конфликтов

Это значение формируется из System. GPS. Дестлонгитуденумератор и System. GPS. Дестлонгитудеденоминатор. Он не может быть записан напрямую. Выверяются значения из разных схем.

### <a name="jpeg-policy"></a>Политика JPEG

### <a name="read-paths"></a>Пути чтения



| Номер | Путь                       | Формат диска |
|-------|----------------------------|-------------|
| 1     | /APP1/IFD/GPS/{ushort = 22}  |             |
| 2     | /КСМП/ексиф: Гпсдестлонгитуде |             |



 

### <a name="write-paths"></a>Пути записи



| Номер | Путь                       | Формат диска |
|-------|----------------------------|-------------|
| 1     | /APP1/IFD/GPS/{ushort = 22}  |             |
| 2     | /КСМП/ексиф: Гпсдестлонгитуде |             |



 

### <a name="remove-paths"></a>Удалить пути



| Номер | Путь                       |
|-------|----------------------------|
| 1     | /APP1/IFD/GPS/{ushort = 22}  |
| 2     | /КСМП/ексиф: гпсдестлонгитуде |



 

### <a name="tiff-policies"></a>Политики TIFF

### <a name="read-paths"></a>Пути чтения



| Номер | Путь                           | Формат диска |
|-------|--------------------------------|-------------|
| 1     | /ИФД/ГПС/{ушорт = 22}           |             |
| 2     | /ИФД/КСМП/ексиф: Гпсдестлонгитуде |             |



 

### <a name="write-paths"></a>Пути записи



| Номер | Путь                           | Формат диска |
|-------|--------------------------------|-------------|
| 1     | /ИФД/ГПС/{ушорт = 22}           |             |
| 2     | /ИФД/КСМП/ексиф: Гпсдестлонгитуде |             |



 

### <a name="remove-paths"></a>Удалить пути



| Номер | Путь                           |
|-------|--------------------------------|
| 1     | /ИФД/ГПС/{ушорт = 22}           |
| 2     | /ИФД/КСМП/ексиф: гпсдестлонгитуде |



 

## <a name="remarks"></a>Remarks

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[System. GPS. Дестлонгитуде](../properties/props-system-gps-destlongitude.md)
</dt> </dl>

 

 
