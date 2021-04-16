---
description: Политика метаданных фотографии для свойства System. photo. Флашмодел.
ms.assetid: ef322823-1b87-40ea-a5e3-e7551f14e44d
title: Политика метаданных фото для System. photo. Флашмодел
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01ade3769cb0d852239af84b769b85d5b3849589
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712301"
---
# <a name="systemphotoflashmodel-photo-metadata-policy"></a>Политика метаданных фото для System. photo. Флашмодел

Политика метаданных фотографии для свойства [System. photo. флашмодел](../properties/props-system-photo-flashmodel.md) .

### <a name="pkey"></a>PKEY

\_Флашмодел фото на PKEY \_

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

Если файл имеет формат JPEG, обработчик будет использовать следующий путь при чтении или записи данных.



| Заказ | Путь                           | Формат диска | Формат данных | Обязательно |
|-------|--------------------------------|-------------|-------------|----------|
| 1     | /КСМП/микрософтфото: Флашмодел | Юникод     |             | Да      |



 

### <a name="precedence-of-paths-tiff"></a>Приоритет путей (TIFF)

Если файл имеет формат TIFF, то при чтении или записи данных обработчик будет использовать следующий порядок приоритета.



| Заказ | Путь                               | Формат диска | Формат данных | Обязательно |
|-------|------------------------------------|-------------|-------------|----------|
| 1     | /ИФД/КСМП/микрософтфото: Флашмодел | Юникод     |             | Да      |



 

## <a name="remarks"></a>Комментарии

## <a name="related-topics"></a>См. также

<dl> <dt>

[System. photo. Флашмодел](../properties/props-system-photo-flashmodel.md)
</dt> </dl>

 

 
