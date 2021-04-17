---
description: Политика метаданных фотографии для свойства System. GPS. Дестлатитудереф.
ms.assetid: 8a13642a-0d29-4193-9784-f716bc428c72
title: Политика метаданных фотографии System. GPS. Дестлатитудереф
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 838e4688f0c3342091e5995885689a44fab38739
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683779"
---
# <a name="systemgpsdestlatituderef-photo-metadata-policy"></a>Политика метаданных фотографии System. GPS. Дестлатитудереф

Политика метаданных фотографии для свойства [System. GPS. дестлатитудереф](../properties/props-system-gps-destlatituderef.md) .

### <a name="pkey"></a>PKEY

PKEY \_ GPS \_ дестлатитудереф

### <a name="containers"></a>Контейнеры

JPEG, TIFF

### <a name="read-only"></a>Только для чтения

Нет

### <a name="output-propvariant-type"></a>Тип выходного ПРОПВАРИАНТ

VT \_ LPWSTR

### <a name="input-type"></a>Тип входных данных

VT \_ LPWSTR является предпочтительным, но технология VT \_ LPSTR принимается.

### <a name="conflict-resolution-policy"></a>Политика разрешения конфликтов

Выверяются значения из разных схем.

### <a name="precedence-of-paths-jpeg"></a>Приоритет путей (JPEG)

Если файл имеет формат JPEG, обработчик будет считывать, записывать и удалять данные в следующем порядке:



| Заказ | Путь                          | Формат диска | Обязательно |
|-------|-------------------------------|-------------|----------|
| 1     | /КСМП/ексиф: Гпсдестлатитудереф  | Юникод     | Да      |
| 2     | /APP1/IFD/GPS/ \\ {UShort = 19 \\ } | ASCII       | Нет       |



 

### <a name="precedence-of-paths-tiff"></a>Приоритет путей (TIFF)

Если файл имеет формат TIFF, обработчик будет считывать, записывать и удалять данные в следующем порядке:



| Заказ | Путь                             | Формат диска | Обязательно |
|-------|----------------------------------|-------------|----------|
| 1     | /ИФД/КСМП/ексиф: Гпсдестлатитудереф | Юникод     | Да      |
| 2     | /ИФД/ГПС/ \\ {UShort = 19 \\ }         | ASCII       | Нет       |



 

## <a name="remarks"></a>Remarks

## <a name="related-topics"></a>См. также

<dl> <dt>

[System. GPS. Дестлатитудереф](../properties/props-system-gps-destlatituderef.md)
</dt> </dl>

 

 
