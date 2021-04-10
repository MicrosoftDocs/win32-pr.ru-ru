---
description: Политика метаданных фотографии для свойства System. GPS. Латитудереф.
ms.assetid: 057015fd-38b7-4053-b611-72565975cc58
title: Политика метаданных фотографии System. GPS. Латитудереф
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 782fbcecbed90c9c75c1ae5fe9d5409496f842a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265997"
---
# <a name="systemgpslatituderef-photo-metadata-policy"></a>Политика метаданных фотографии System. GPS. Латитудереф

Политика метаданных фотографии для свойства [System. GPS. латитудереф](../properties/props-system-gps-latitude.md) .

### <a name="pkey"></a>PKEY

PKEY \_ GPS \_ латитудереф

### <a name="containers"></a>Контейнеры

JPEG, TIFF

### <a name="read-only"></a>Только для чтения

Нет

### <a name="output-propvariant-type"></a>Тип выходного ПРОПВАРИАНТ

VT \_ LPWSTR

### <a name="input-type"></a>Тип входных данных

VT \_ LPWSTR является предпочтительным, но \_ также принимается VT LPSTR.

### <a name="conflict-resolution-policy"></a>Политика разрешения конфликтов

Выверяются значения из разных схем.

### <a name="precedence-of-paths-jpeg"></a>Приоритет путей (JPEG)

Если файл имеет формат JPEG, обработчик будет считывать, записывать и удалять данные в следующем порядке:



| Заказ | Путь                         | Формат диска | Обязательно |
|-------|------------------------------|-------------|----------|
| 1     | /КСМП/ексиф: Гпслатитудереф     | Юникод     | Да      |
| 2     | /APP1/IFD/GPS/ \\ {UShort = 1 \\ } | ASCII       | Нет       |



 

### <a name="precedence-of-paths-tiff"></a>Приоритет путей (TIFF)

Если файл имеет формат TIFF, обработчик будет считывать, записывать и удалять данные в следующем порядке:



| Заказ | Путь                         | Формат диска | Обязательно |
|-------|------------------------------|-------------|----------|
| 1     | /ИФД/КСМП/ексиф: Гпслатитудереф | Юникод     | Да      |
| 2     | /ИФД/ГПС/ \\ {UShort = 1 \\ }      | ASCII       | Нет       |



 

## <a name="remarks"></a>Remarks

## <a name="related-topics"></a>См. также

<dl> <dt>

[System. GPS. Латитудереф](../properties/props-system-gps-latitude.md)
</dt> </dl>

 

 
