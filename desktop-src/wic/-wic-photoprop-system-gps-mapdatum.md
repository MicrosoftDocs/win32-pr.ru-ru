---
description: Политика метаданных фотографии для свойства System. GPS. Мапдатум.
ms.assetid: be31e98f-5114-4693-a9ef-37fea334875b
title: Политика метаданных фотографии System. GPS. Мапдатум
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb7a279c79da3d2b1dd20563af35bd34233a1a2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674273"
---
# <a name="systemgpsmapdatum-photo-metadata-policy"></a>Политика метаданных фотографии System. GPS. Мапдатум

Политика метаданных фотографии для свойства [System. GPS. мапдатум](../properties/props-system-gps-mapdatum.md) .

### <a name="pkey"></a>PKEY

PKEY \_ GPS \_ мапдатум

### <a name="containers"></a>Контейнеры

JPEG, TIFF

### <a name="read-only"></a>Только для чтения

Нет

### <a name="output-propvariant-type"></a>Тип выходного ПРОПВАРИАНТ

VT \_ LPWSTR

### <a name="input-type"></a>Тип входных данных

VT \_ LPWSTR является предпочтительным, но \_ также принимается VT LPSTR

### <a name="conflict-resolution-policy"></a>Политика разрешения конфликтов

Выверяются значения из разных схем.

### <a name="precedence-of-paths-jpeg"></a>Приоритет путей (JPEG)

Если файл имеет формат JPEG, обработчик будет считывать, записывать и удалять данные в следующем порядке:



| Заказ | Путь                          | Формат диска | Обязательно |
|-------|-------------------------------|-------------|----------|
| 1     | /КСМП/ексиф: Гпсмапдатум         | Юникод     | Да      |
| 2     | /APP1/IFD/GPS/ \\ {UShort = 18 \\ } | ASCII       | Нет       |



 

### <a name="precedence-of-paths-tiff"></a>Приоритет путей (TIFF)

Если файл имеет формат TIFF, обработчик будет считывать, записывать и удалять данные в следующем порядке:



| Заказ | Путь                      | Формат диска | Обязательно |
|-------|---------------------------|-------------|----------|
| 1     | /ИФД/КСМП/ексиф: Гпсмапдатум | Юникод     | Да      |
| 2     | /ИФД/ГПС/ \\ {UShort = 18 \\ }  | ASCII       | Нет       |



 

## <a name="remarks"></a>Remarks

## <a name="related-topics"></a>См. также

<dl> <dt>

[System. GPS. Мапдатум](../properties/props-system-gps-mapdatum.md)
</dt> </dl>

 

 
