---
description: Политика метаданных фотографии для свойства System. GPS. Спутниковоеs.
ms.assetid: 5dbbbeaf-e67d-45f6-95b2-de3287202d41
title: Политика метаданных фотографии System. GPS. Спутниковое
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 980393accdb1bee3d2a44dd539f3c9fb169c648b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105673875"
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



| Заказ | Путь                     | Формат диска |
|-------|--------------------------|-------------|
| 1     | /APP1/IFD/GPS/{ushort = 8} | ascii       |
| 2     | /КСМП/ексиф: Гпссателлитес  | Юникод     |



 

### <a name="write-paths"></a>Пути записи



| Заказ | Путь                     | Формат диска |
|-------|--------------------------|-------------|
| 1     | /APP1/IFD/GPS/{ushort = 8} | ascii       |
| 2     | /КСМП/ексиф: Гпссателлитес  | Юникод     |



 

### <a name="remove-paths"></a>Удалить пути



| Заказ | Путь                     |
|-------|--------------------------|
| 1     | /APP1/IFD/GPS/{ushort = 8} |
| 2     | /КСМП/ексиф: гпссателлитес  |



 

### <a name="tiff-policies"></a>Политики TIFF

### <a name="read-paths"></a>Пути чтения



| Заказ | Путь                        | Формат диска |
|-------|-----------------------------|-------------|
| 1     | /ИФД/ГПС/{ушорт = 8}         | ascii       |
| 2     | /ИФД/КСМП/ексиф: Гпссателлитес | Юникод     |



 

### <a name="write-paths"></a>Пути записи



| Заказ | Путь                        | Формат диска |
|-------|-----------------------------|-------------|
| 1     | /ИФД/ГПС/{ушорт = 8}         | ascii       |
| 2     | /ИФД/КСМП/ексиф: Гпссателлитес | Юникод     |



 

### <a name="remove-paths"></a>Удалить пути



| Заказ | Путь                        |
|-------|-----------------------------|
| 1     | /ИФД/ГПС/{ушорт = 8}         |
| 2     | /ИФД/КСМП/ексиф: гпссателлитес |



 

## <a name="remarks"></a>Комментарии

## <a name="related-topics"></a>См. также

<dl> <dt>

[System. GPS. спутники](../properties/props-system-gps-satellites.md)
</dt> </dl>

 

 
