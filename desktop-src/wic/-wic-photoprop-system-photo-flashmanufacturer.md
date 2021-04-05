---
description: Политика метаданных фотографии для свойства System. photo. Флашмануфактурер.
ms.assetid: f62e85ec-2dc6-456b-a43b-7b76d162b608
title: Политика метаданных фото для System. photo. Флашмануфактурер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa1e785dfd00662acf065021a3c80de5c587586c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081445"
---
# <a name="systemphotoflashmanufacturer-photo-metadata-policy"></a>Политика метаданных фото для System. photo. Флашмануфактурер

Политика метаданных фотографии для свойства [System. photo. флашмануфактурер](../properties/props-system-photo-flashmanufacturer.md) .

### <a name="pkey"></a>PKEY

\_Флашмануфактурер фото на PKEY \_

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



| Заказ | Путь                                  | Формат диска | Формат данных | Обязательно |
|-------|---------------------------------------|-------------|-------------|----------|
| 1     | /КСМП/микрософтфото: Флашмануфактурер | Юникод     |             | Да      |



 

### <a name="precedence-of-paths-tiff"></a>Приоритет путей (TIFF)

Если файл имеет формат TIFF, то при чтении или записи данных обработчик будет использовать следующий порядок приоритета.



| Заказ | Путь                                      | Формат диска | Формат данных | Обязательно |
|-------|-------------------------------------------|-------------|-------------|----------|
| 1     | /ИФД/КСМП/микрософтфото: Флашмануфактурер | Юникод     |             | Да      |



 

## <a name="remarks"></a>Комментарии

## <a name="related-topics"></a>См. также

<dl> <dt>

[System. photo. Флашмануфактурер](../properties/props-system-photo-flashmanufacturer.md)
</dt> </dl>

 

 
