---
description: Политика метаданных фотографии для свойства System. GPS. DOP.
ms.assetid: 62efd1cc-a2ae-4e53-a0f2-4822b8c91c42
title: Политика метаданных фотографии System. GPS. DOP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c33f3bfc6b958593748396124a8cfd1a7de73fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999420"
---
# <a name="systemgpsdop-photo-metadata-policy"></a>Политика метаданных фотографии System. GPS. DOP

Политика метаданных фотографии для свойства [System. GPS. DOP](../properties/props-system-gps-dop.md) .

### <a name="pkey"></a>PKEY

PKEY \_ GPS \_ DOP

### <a name="containers"></a>Контейнеры

JPEG, TIFF

### <a name="read-only"></a>Только для чтения

Да

### <a name="output-propvariant-type"></a>Тип выходного ПРОПВАРИАНТ

VT \_ R8

### <a name="conflict-resolution-policy"></a>Политика разрешения конфликтов

Это значение можно записать с помощью записи в System. GPS. Допнумератор и System. GPS. Допденоминатор. Он не может быть записан напрямую. Выверяются значения из разных схем.

### <a name="precedence-of-paths-jpeg"></a>Приоритет путей (JPEG)

Если файл имеет формат JPEG, обработчик будет считывать, записывать и удалять данные в следующем порядке:



| Заказ | Путь                          | Формат диска   | Обязательно |
|-------|-------------------------------|---------------|----------|
| 1     | /КСМП/ексиф: ГПСДОП              | Рациональное XMP  | Да      |
| 2     | /APP1/IFD/GPS/ \\ {UShort = 11 \\ } | Рациональное воссебе EXIF | Нет       |



 

### <a name="precedence-of-paths-tiff"></a>Приоритет путей (TIFF)

Если файл имеет формат TIFF, обработчик будет считывать, записывать и удалять данные в следующем порядке:



| Заказ | Путь                     | Формат диска   | Обязательно |
|-------|--------------------------|---------------|----------|
| 1     | /ИФД/КСМП/ексиф: Гпсдоп     | Рациональное XMP  | Да      |
| 2     | /ИФД/ГПС/ \\ {UShort = 11 \\ } | Рациональное воссебе EXIF | Нет       |



 

## <a name="remarks"></a>Remarks

## <a name="related-topics"></a>См. также

<dl> <dt>

[System. GPS. DOP](../properties/props-system-gps-dop.md)
</dt> </dl>

 

 
