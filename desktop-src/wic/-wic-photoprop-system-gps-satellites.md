---
description: Политика метаданных фотографии для свойства System. GPS. Спутниковоеs.
ms.assetid: 5dbbbeaf-e67d-45f6-95b2-de3287202d41
title: Политика метаданных фотографии System. GPS. Спутниковое
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a65bdc244324df513b5029c682e9c2cb355da58f2c95d13910fe093ce2521c8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118964843"
---
# <a name="systemgpssatellites-photo-metadata-policy"></a>Политика метаданных фотографии System. GPS. Спутниковое

Политика метаданных фотографии для свойства [System. GPS. спутниковоеs](../properties/props-system-gps-satellites.md) .

### <a name="pkey"></a>PKEY

\_Вспомогательная лицензия GPS "PKEY" \_

### <a name="containers"></a>Контейнеры

JPEG, TIFF

### <a name="read-only"></a>Только для чтения

Нет

### <a name="output-propvariant-type"></a>Тип выходного ПРОПВАРИАНТ

VT \_ LPWSTR

### <a name="input-type"></a>Тип входных данных

Строка.

### <a name="conflict-resolution-policy"></a>Политика разрешения конфликтов

Выверяются значения из разных схем.

### <a name="jpeg-policies"></a>Политики JPEG

### <a name="read-paths"></a>Пути чтения



| Номер | Путь                     | Формат диска |
|-------|--------------------------|-------------|
| 1     | /APP1/IFD/GPS/{ushort = 8} | ascii       |
| 2     | /КСМП/ексиф: Гпссателлитес  | Юникод     |



 

### <a name="write-paths"></a>Пути записи



| Номер | Путь                     | Формат диска |
|-------|--------------------------|-------------|
| 1     | /APP1/IFD/GPS/{ushort = 8} | ascii       |
| 2     | /КСМП/ексиф: Гпссателлитес  | Юникод     |



 

### <a name="remove-paths"></a>Удалить пути



| Номер | Путь                     |
|-------|--------------------------|
| 1     | /APP1/IFD/GPS/{ushort = 8} |
| 2     | /КСМП/ексиф: гпссателлитес  |



 

### <a name="tiff-policies"></a>Политики TIFF

### <a name="read-paths"></a>Пути чтения



| Номер | Путь                        | Формат диска |
|-------|-----------------------------|-------------|
| 1     | /ИФД/ГПС/{ушорт = 8}         | ascii       |
| 2     | /ИФД/КСМП/ексиф: Гпссателлитес | Юникод     |



 

### <a name="write-paths"></a>Пути записи



| Номер | Путь                        | Формат диска |
|-------|-----------------------------|-------------|
| 1     | /ИФД/ГПС/{ушорт = 8}         | ascii       |
| 2     | /ИФД/КСМП/ексиф: Гпссателлитес | Юникод     |



 

### <a name="remove-paths"></a>Удалить пути



| Номер | Путь                        |
|-------|-----------------------------|
| 1     | /ИФД/ГПС/{ушорт = 8}         |
| 2     | /ИФД/КСМП/ексиф: гпссателлитес |



 

## <a name="remarks"></a>Remarks

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[System. GPS. спутники](../properties/props-system-gps-satellites.md)
</dt> </dl>

 

 
