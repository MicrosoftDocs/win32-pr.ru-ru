---
description: Политика метаданных фотографии для свойства System. GPS. Алтитудереф.
ms.assetid: abbb2441-25ca-484b-a744-620ff2794221
title: Политика метаданных фотографии System. GPS. Алтитудереф
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db600d218d72014c49fd3f0a8b5eb11dd4c467d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712801"
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



| Заказ | Путь                     | Формат диска |
|-------|--------------------------|-------------|
| 1     | /APP1/IFD/GPS/{ushort = 5} | byte        |
| 2     | /КСМП/ексиф: Гпсалтитудереф | Юникод     |



 

### <a name="write-paths"></a>Пути записи



| Заказ | Путь                     | Формат диска |
|-------|--------------------------|-------------|
| 1     | /APP1/IFD/GPS/{ushort = 5} | byte        |
| 2     | /КСМП/ексиф: Гпсалтитудереф | Юникод     |



 

### <a name="remove-paths"></a>Удалить пути



| Заказ | Путь                     |
|-------|--------------------------|
| 1     | /APP1/IFD/GPS/{ushort = 5} |
| 2     | /КСМП/ексиф: гпсалтитудереф |



 

### <a name="tiff-policies"></a>Политики TIFF

### <a name="read-paths"></a>Пути чтения



| Заказ | Путь                         | Формат диска |
|-------|------------------------------|-------------|
| 1     | /ИФД/ГПС/{ушорт = 5}          | byte        |
| 2     | /ИФД/КСМП/ексиф: Гпсалтитудереф | Юникод     |



 

### <a name="write-paths"></a>Пути записи



| Заказ | Путь                         | Формат диска |
|-------|------------------------------|-------------|
| 1     | /ИФД/ГПС/{ушорт = 5}          | byte        |
| 2     | /ИФД/КСМП/ексиф: Гпсалтитудереф | Юникод     |



 

### <a name="remove-paths"></a>Удалить пути



| Заказ | Путь                         |
|-------|------------------------------|
| 1     | /ИФД/ГПС/{ушорт = 5}          |
| 2     | /ИФД/КСМП/ексиф: гпсалтитудереф |



 

## <a name="remarks"></a>Комментарии

## <a name="related-topics"></a>См. также

<dl> <dt>

[System. GPS. Алтитудереф](../properties/props-system-gps-altituderef.md)
</dt> </dl>

 

 
