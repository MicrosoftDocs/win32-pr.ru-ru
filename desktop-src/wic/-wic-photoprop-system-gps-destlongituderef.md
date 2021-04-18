---
description: Политика метаданных фотографии для свойства System. GPS. Дестлонгитудереф.
ms.assetid: 2a0abb9b-41e3-49ba-a60b-3096d9c032bd
title: Политика метаданных фотографии System. GPS. Дестлонгитудереф
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8139fcf5218d9863393888d7ab7b188a53e7f55f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712691"
---
# <a name="systemgpsdestlongituderef-photo-metadata-policy"></a>Политика метаданных фотографии System. GPS. Дестлонгитудереф

Политика метаданных фотографии для свойства [System. GPS. дестлонгитудереф](../properties/props-system-gps-destlongituderef.md) .

### <a name="pkey"></a>PKEY

PKEY \_ , GPS. дестлонгитудереф

### <a name="containers"></a>Контейнеры

JPEG, TIFF

### <a name="read-only"></a>Только для чтения

Нет

### <a name="output-propvariant-type"></a>Тип выходного ПРОПВАРИАНТ

VT \_ LPWSTR

### <a name="input-propvariant-type"></a>Тип входного ПРОПВАРИАНТ

VT \_ LPWSTR является предпочтительным, но \_ также принимается VT LPSTR.

### <a name="conflict-resolution-policy"></a>Политика разрешения конфликтов

Выверяются значения из разных схем.

### <a name="precedence-of-paths-jpeg"></a>Приоритет путей (JPEG)

Если файл имеет формат JPEG, обработчик будет считывать, записывать и удалять данные в следующем порядке:



| Заказ | Путь                          | Формат диска | Обязательно |
|-------|-------------------------------|-------------|----------|
| 1     | /КСМП/ексиф: Гпсдестлонгитудереф | Юникод     | Да      |
| 2     | /APP1/IFD/GPS/ \\ {UShort = 21 \\ } | ASCII       | Нет       |



 

### <a name="precedence-of-paths-tiff"></a>Приоритет путей (TIFF)

Если файл имеет формат TIFF, обработчик будет считывать, записывать и удалять данные в следующем порядке:



| Заказ | Путь                              | Формат диска | Обязательно |
|-------|-----------------------------------|-------------|----------|
| 1     | /ИФД/КСМП/ексиф: Гпсдестлонгитудереф | Юникод     | Да      |
| 2     | /ИФД/ГПС/ \\ {UShort = 21 \\ }          | ASCII       | Нет       |



 

## <a name="remarks"></a>Remarks

## <a name="related-topics"></a>См. также

<dl> <dt>

[System. GPS. Дестлонгитудереф](../properties/props-system-gps-destlongituderef.md)
</dt> </dl>

 

 
