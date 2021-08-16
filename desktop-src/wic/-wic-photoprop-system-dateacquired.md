---
description: Политика метаданных фотографии для свойства System. Датеаккуиред.
ms.assetid: 04a61ecc-d168-4f93-b143-3e6ba8aaf322
title: Политика метаданных фотографии System. Датеаккуиред
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c95b8f68d99476db0832a321de1f61c6f3c4dc6be6f10d679735bd51fc92ce7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119087885"
---
# <a name="systemdateacquired-photo-metadata-policy"></a>Политика метаданных фотографии System. Датеаккуиред

Политика метаданных фотографии для свойства [System. датеаккуиред](../properties/props-system-dateacquired.md) .

### <a name="pkey"></a>PKEY

PKEY \_ датеаккуиред

### <a name="containers"></a>Контейнеры

JPEG, TIFF

### <a name="read-only"></a>Только для чтения

Нет

### <a name="output-propvariant-type"></a>Тип выходного ПРОПВАРИАНТ

VT \_ fileTime

### <a name="input-propvariant-type"></a>Тип входного ПРОПВАРИАНТ

VT \_ fileTime

### <a name="conflict-resolution-policy"></a>Политика разрешения конфликтов

Выверяются значения из разных схем.

### <a name="precedence-of-paths-jpeg"></a>Приоритет путей (JPEG)

Если файл имеет формат JPEG, обработчик выполняет поиск данных в следующем порядке:



| Номер | Путь                             | Формат диска                        | Обязательно |
|-------|----------------------------------|------------------------------------|----------|
| 1     | /КСМП/микрософтфото: Датеаккуиред | Строка Юникода в формате даты XMP. | Да      |



 

### <a name="precedence-of-paths-tiff"></a>Приоритет путей (TIFF)

Если файл имеет формат TIFF, обработчик выполняет поиск данных в следующем порядке:



| Номер | Путь                                 | Формат диска                        | Обязательно |
|-------|--------------------------------------|------------------------------------|----------|
| 1     | /ИФД/КСМП/микрософтфото: Датеаккуиред | Строка Юникода в формате даты XMP. | Да      |



 

## <a name="remarks"></a>Remarks

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[System. Датеаккуиред](../properties/props-system-dateacquired.md)
</dt> </dl>

 

 
