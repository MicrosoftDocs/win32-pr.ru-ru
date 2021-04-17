---
description: Политика метаданных фотографии для свойства System. GPS. Лонгитудереф.
ms.assetid: 6e7b3b87-70e5-4c6a-a9b3-959eab38f1f0
title: Политика метаданных фотографии System. GPS. Лонгитудереф
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72a93d37b59ca7c77bc05e049860cf4e2608eb60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674274"
---
# <a name="systemgpslongituderef-photo-metadata-policy"></a>Политика метаданных фотографии System. GPS. Лонгитудереф

Политика метаданных фотографии для свойства [System. GPS. лонгитудереф](../properties/props-system-gps-longituderef.md) .

### <a name="pkey"></a>PKEY

PKEY \_ GPS \_ лонгитудереф

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

### <a name="precedence-of-paths-jpeg"></a>Приоритет путей (JPEG)

Если файл имеет формат JPEG, обработчик будет считывать, записывать и удалять данные в следующем порядке:



| Заказ | Путь                         | Формат диска | Обязательно |
|-------|------------------------------|-------------|----------|
| 1     | /КСМП/ексиф: Гпслонгитудереф    | Юникод     | Да      |
| 2     | /APP1/IFD/GPS/ \\ {UShort = 3 \\ } | ASCII       | Нет       |



 

### <a name="precedence-of-paths-tiff"></a>Приоритет путей (TIFF)

Если файл имеет формат TIFF, обработчик будет считывать, записывать и удалять данные в следующем порядке:



| Заказ | Путь                          | Формат диска | Обязательно |
|-------|-------------------------------|-------------|----------|
| 1     | /ИФД/КСМП/ексиф: Гпслонгитудереф | Юникод     | Да      |
| 2     | /ИФД/ГПС/ \\ {UShort = 3 \\ }       | ASCII       | Нет       |



 

## <a name="remarks"></a>Remarks

## <a name="related-topics"></a>См. также

<dl> <dt>

[System. GPS. Лонгитудереф](../properties/props-system-gps-longituderef.md)
</dt> </dl>

 

 
