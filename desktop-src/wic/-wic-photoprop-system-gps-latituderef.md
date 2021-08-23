---
description: Политика метаданных фотографии для свойства System. GPS. Латитудереф.
ms.assetid: 057015fd-38b7-4053-b611-72565975cc58
title: Политика метаданных фотографии System. GPS. Латитудереф
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04412af5359e39eaf8e033b059b1c5460e33f6d7537c4763b009b11010fbe87a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119087252"
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



| Номер | Путь                         | Формат диска | Обязательно |
|-------|------------------------------|-------------|----------|
| 1     | /КСМП/ексиф: Гпслатитудереф     | Юникод     | Да      |
| 2     | /APP1/IFD/GPS/ \\ {UShort = 1 \\ } | ASCII       | Нет       |



 

### <a name="precedence-of-paths-tiff"></a>Приоритет путей (TIFF)

Если файл имеет формат TIFF, обработчик будет считывать, записывать и удалять данные в следующем порядке:



| Номер | Путь                         | Формат диска | Обязательно |
|-------|------------------------------|-------------|----------|
| 1     | /ИФД/КСМП/ексиф: Гпслатитудереф | Юникод     | Да      |
| 2     | /ИФД/ГПС/ \\ {UShort = 1 \\ }      | ASCII       | Нет       |



 

## <a name="remarks"></a>Remarks

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[System. GPS. Латитудереф](../properties/props-system-gps-latitude.md)
</dt> </dl>

 

 
