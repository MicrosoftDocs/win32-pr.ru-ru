---
description: Политика метаданных фотографии для свойства System. GPS. Дестбеарингреф.
ms.assetid: d1c8b3cc-ed52-43ca-a0ba-045a2c5fe274
title: Политика метаданных фотографии System. GPS. Дестбеарингреф
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26ee4b984d0a759769b80be76b53499690673c7ec630c759aa0371b53ea9368f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119087855"
---
# <a name="systemgpsdestbearingref-photo-metadata-policy"></a>Политика метаданных фотографии System. GPS. Дестбеарингреф

Политика метаданных фотографии для свойства [System. GPS. дестбеарингреф](../properties/props-system-gps-destbearingref.md) .

### <a name="pkey"></a>PKEY

PKEY \_ GPS \_ дестбеарингреф

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



| Номер | Путь                        | Формат диска |
|-------|-----------------------------|-------------|
| 1     | /APP1/IFD/GPS/{ushort = 23}   | ascii       |
| 2     | /КСМП/ексиф: Гпсдестбеарингреф | Юникод     |



 

### <a name="write-paths"></a>Пути записи



| Номер | Путь                        | Формат диска |
|-------|-----------------------------|-------------|
| 1     | /APP1/IFD/GPS/{ushort = 23}   | ascii       |
| 2     | /КСМП/ексиф: Гпсдестбеарингреф | Юникод     |



 

### <a name="remove-paths"></a>Удалить пути



| Номер | Путь                        |
|-------|-----------------------------|
| 1     | /APP1/IFD/GPS/{ushort = 23}   |
| 2     | /КСМП/ексиф: гпсдестбеарингреф |



 

### <a name="tiff-policies"></a>Политики TIFF

### <a name="read-paths"></a>Пути чтения



| Номер | Путь                            | Формат диска |
|-------|---------------------------------|-------------|
| 1     | /ИФД/ГПС/{ушорт = 23}            | ascii       |
| 2     | /ИФД/КСМП/ексиф: Гпсдестбеарингреф | Юникод     |



 

### <a name="write-paths"></a>Пути записи



| Номер | Путь                            | Формат диска |
|-------|---------------------------------|-------------|
| 1     | /ИФД/ГПС/{ушорт = 23}            | ascii       |
| 2     | /ИФД/КСМП/ексиф: Гпсдестбеарингреф | Юникод     |



 

### <a name="remove-paths"></a>Удалить пути



| порядок | path                            |
|-------|---------------------------------|
| 1     | /ИФД/ГПС/{ушорт = 23}            |
| 2     | /ИФД/КСМП/ексиф: гпсдестбеарингреф |



 

## <a name="remarks"></a>Remarks

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[System. GPS. Дестбеарингреф](../properties/props-system-gps-destbearingref.md)
</dt> </dl>

 

 
