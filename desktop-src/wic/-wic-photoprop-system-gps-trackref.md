---
description: Политика метаданных фотографии для свойства System. GPS. Траккреф.
ms.assetid: e6912177-8add-4520-b396-c28060b359c7
title: Политика метаданных фотографии System. GPS. Траккреф
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34a523f801b8e82fc4191b54bf0bb5fee659ab4f5b09c326d5d1adf14c713f13
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119087182"
---
# <a name="systemgpstrackref-photo-metadata-policy"></a>Политика метаданных фотографии System. GPS. Траккреф

Политика метаданных фотографии для свойства [System. GPS. траккреф](../properties/props-system-gps-trackref.md) .

### <a name="pkey"></a>PKEY

PKEY \_ GPS \_ траккреф

### <a name="containers"></a>Контейнеры

JPEG, TIFF

### <a name="read-only"></a>Только для чтения

Нет

### <a name="output-propvariant-type"></a>Тип выходного ПРОПВАРИАНТ

VT \_ LPWSTR

### <a name="input-type"></a>Тип входных данных

Строковый тип

### <a name="conflict-resolution-policy"></a>Политика разрешения конфликтов

Выверяются значения из разных схем.

### <a name="jpeg-policies"></a>Политики JPEG

### <a name="read-paths"></a>Пути чтения



| Номер | Путь                      | Формат диска |
|-------|---------------------------|-------------|
| 1     | /APP1/IFD/GPS/{ushort = 14} | ascii       |
| 2     | /КСМП/ексиф: Гпстраккреф     | Юникод     |



 

### <a name="write-paths"></a>Пути записи



| Номер | Путь                      | Формат диска |
|-------|---------------------------|-------------|
| 1     | /APP1/IFD/GPS/{ushort = 14} | ascii       |
| 2     | /КСМП/ексиф: Гпстраккреф     | Юникод     |



 

### <a name="remove-paths"></a>Удалить пути



| Номер | Путь                      |
|-------|---------------------------|
| 1     | /APP1/IFD/GPS/{ushort = 14} |
| 2     | /КСМП/ексиф: гпстраккреф     |



 

### <a name="tiff-policies"></a>Политики TIFF

### <a name="read-paths"></a>Пути чтения



| Номер | Путь                      | Формат диска |
|-------|---------------------------|-------------|
| 1     | /ИФД/ГПС/{ушорт = 14}      | ascii       |
| 2     | /ИФД/КСМП/ексиф: Гпстраккреф | Юникод     |



 

### <a name="write-paths"></a>Пути записи



| Номер | Путь                      | Формат диска |
|-------|---------------------------|-------------|
| 1     | /ИФД/ГПС/{ушорт = 14}      | ascii       |
| 2     | /ИФД/КСМП/ексиф: Гпстраккреф | Юникод     |



 

### <a name="remove-paths"></a>Удалить пути



| Номер | Путь                      |
|-------|---------------------------|
| 1     | /ИФД/ГПС/{ушорт = 14}      |
| 2     | /ИФД/КСМП/ексиф: гпстраккреф |



 

## <a name="remarks"></a>Remarks

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[System. GPS. Траккреф](../properties/props-system-gps-trackref.md)
</dt> </dl>

 

 
