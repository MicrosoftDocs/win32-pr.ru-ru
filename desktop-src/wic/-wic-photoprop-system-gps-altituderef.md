---
description: Политика метаданных фотографии для свойства System. GPS. Алтитудереф.
ms.assetid: abbb2441-25ca-484b-a744-620ff2794221
title: Политика метаданных фотографии System. GPS. Алтитудереф
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca49213754f605dcf6df40dfa3ff00e2b7aeaf765008037c23da21e35ab9ddee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118710701"
---
# <a name="systemgpsaltituderef-photo-metadata-policy"></a>Политика метаданных фотографии System. GPS. Алтитудереф

Политика метаданных фотографии для свойства [System. GPS. алтитудереф](../properties/props-system-gps-altituderef.md) .

### <a name="pkey"></a>PKEY

PKEY \_ GPS \_ алтитудереф

### <a name="description"></a>Описание

Указывает высоту, используемую в качестве высоты ссылки. Значение 0 указывает, что высота превышает уровень моря. Значение 1 указывает на высоту ниже уровня Sea.

### <a name="containers"></a>Контейнеры

JPEG, TIFF

### <a name="read-only"></a>Только для чтения

Нет

### <a name="output-propvariant-type"></a>Тип выходного ПРОПВАРИАНТ

VT \_ UI1

### <a name="input-type"></a>Тип входных данных

Двухбайтовых.

### <a name="conflict-resolution-policy"></a>Политика разрешения конфликтов

Выверяются значения из разных схем.

### <a name="jpeg-policies"></a>Политики JPEG

### <a name="read-paths"></a>Пути чтения



| Номер | Путь                     | Формат диска |
|-------|--------------------------|-------------|
| 1     | /APP1/IFD/GPS/{ushort = 5} | byte        |
| 2     | /КСМП/ексиф: Гпсалтитудереф | Юникод     |



 

### <a name="write-paths"></a>Пути записи



| Номер | Путь                     | Формат диска |
|-------|--------------------------|-------------|
| 1     | /APP1/IFD/GPS/{ushort = 5} | byte        |
| 2     | /КСМП/ексиф: Гпсалтитудереф | Юникод     |



 

### <a name="remove-paths"></a>Удалить пути



| Номер | Путь                     |
|-------|--------------------------|
| 1     | /APP1/IFD/GPS/{ushort = 5} |
| 2     | /КСМП/ексиф: гпсалтитудереф |



 

### <a name="tiff-policies"></a>Политики TIFF

### <a name="read-paths"></a>Пути чтения



| Номер | Путь                         | Формат диска |
|-------|------------------------------|-------------|
| 1     | /ИФД/ГПС/{ушорт = 5}          | byte        |
| 2     | /ИФД/КСМП/ексиф: Гпсалтитудереф | Юникод     |



 

### <a name="write-paths"></a>Пути записи



| Номер | Путь                         | Формат диска |
|-------|------------------------------|-------------|
| 1     | /ИФД/ГПС/{ушорт = 5}          | byte        |
| 2     | /ИФД/КСМП/ексиф: Гпсалтитудереф | Юникод     |



 

### <a name="remove-paths"></a>Удалить пути



| Номер | Путь                         |
|-------|------------------------------|
| 1     | /ИФД/ГПС/{ушорт = 5}          |
| 2     | /ИФД/КСМП/ексиф: гпсалтитудереф |



 

## <a name="remarks"></a>Remarks

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[System. GPS. Алтитудереф](../properties/props-system-gps-altituderef.md)
</dt> </dl>

 

 
