---
description: Политика метаданных фотографии для свойства System. GPS. Дестдистанцереф.
ms.assetid: eb671f34-7366-4182-b72e-0dd7830751e0
title: Политика метаданных фотографии System. GPS. Дестдистанцереф
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bba6e04bee00aaed868fcc02059403fe479f8cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684399"
---
# <a name="systemgpsdestdistanceref-photo-metadata-policy"></a>Политика метаданных фотографии System. GPS. Дестдистанцереф

Политика метаданных фотографии для свойства [System. GPS. дестдистанцереф](../properties/props-system-gps-destdistanceref.md) .

### <a name="pkey"></a>PKEY

PKEY \_ дестдистанцереф

### <a name="containers"></a>Контейнеры

JPEG, TIFF

### <a name="read-only"></a>Только для чтения

Нет

### <a name="output-propvariant-type"></a>Тип выходного ПРОПВАРИАНТ

VT \_ LPWSTR

### <a name="input-type"></a>Тип входных данных

\_Принимаются VT LPWSTR или VT \_ LPSTR.

### <a name="conflict-resolution-policy"></a>Политика разрешения конфликтов

Выверяются значения из разных схем.

### <a name="jpeg-policies"></a>Политики JPEG

### <a name="read-paths"></a>Пути чтения



| Заказ | Путь                         | Формат диска |
|-------|------------------------------|-------------|
| 1     | /APP1/IFD/GPS/{ushort = 25}    | ascii       |
| 2     | /КСМП/ексиф: Гпсдестдистанцереф | Юникод     |



 

### <a name="write-paths"></a>Пути записи



| Заказ | Путь                         | Формат диска |
|-------|------------------------------|-------------|
| 1     | /APP1/IFD/GPS/{ushort = 25}    | ascii       |
| 2     | /КСМП/ексиф: Гпсдестдистанцереф | Юникод     |



 

### <a name="remove-paths"></a>Удалить пути



| Заказ | Путь                         |
|-------|------------------------------|
| 1     | /APP1/IFD/GPS/{ushort = 25}    |
| 2     | /КСМП/ексиф: гпсдестдистанцереф |



 

### <a name="tiff-policies"></a>Политики TIFF

### <a name="read-paths"></a>Пути чтения



| Заказ | Путь                             | Формат диска |
|-------|----------------------------------|-------------|
| 1     | /ИФД/ГПС/{ушорт = 25}             | ascii       |
| 2     | /ИФД/КСМП/ексиф: Гпсдестдистанцереф | Юникод     |



 

### <a name="write-paths"></a>Пути записи



| Заказ | Путь                             | Формат диска |
|-------|----------------------------------|-------------|
| 1     | /ИФД/ГПС/{ушорт = 25}             | ascii       |
| 2     | /ИФД/КСМП/ексиф: Гпсдестдистанцереф | Юникод     |



 

### <a name="remove-paths"></a>Удалить пути



| Заказ | Путь                             |
|-------|----------------------------------|
| 1     | /ИФД/ГПС/{ушорт = 25}             |
| 2     | /ИФД/КСМП/ексиф: гпсдестдистанцереф |



 

## <a name="remarks"></a>Комментарии

## <a name="related-topics"></a>См. также

<dl> <dt>

[System. GPS. Дестдистанцереф](../properties/props-system-gps-destdistanceref.md)
</dt> </dl>

 

 
