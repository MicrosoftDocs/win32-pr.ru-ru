---
description: Политика метаданных фотографии для свойства System. Датеаккуиред.
ms.assetid: 04a61ecc-d168-4f93-b143-3e6ba8aaf322
title: Политика метаданных фотографии System. Датеаккуиред
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f126ccb4424d1489f671f61f719a505559a78c8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272298"
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



| Заказ | Путь                             | Формат диска                        | Обязательно |
|-------|----------------------------------|------------------------------------|----------|
| 1     | /КСМП/микрософтфото: Датеаккуиред | Строка Юникода в формате даты XMP. | Да      |



 

### <a name="precedence-of-paths-tiff"></a>Приоритет путей (TIFF)

Если файл имеет формат TIFF, обработчик выполняет поиск данных в следующем порядке:



| Заказ | Путь                                 | Формат диска                        | Обязательно |
|-------|--------------------------------------|------------------------------------|----------|
| 1     | /ИФД/КСМП/микрософтфото: Датеаккуиред | Строка Юникода в формате даты XMP. | Да      |



 

## <a name="remarks"></a>Комментарии

## <a name="related-topics"></a>См. также

<dl> <dt>

[System. Датеаккуиред](../properties/props-system-dateacquired.md)
</dt> </dl>

 

 
