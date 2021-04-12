---
description: Политика метаданных фотографии для свойства System. photo. Ленсмануфактурер.
ms.assetid: ee25da96-982f-475e-8957-e24ef7721b78
title: Политика метаданных фото для System. photo. Ленсмануфактурер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6696e7113a14a9b5b26a26f38258f30a5ba82cf3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265861"
---
# <a name="systemphotolensmanufacturer-photo-metadata-policy"></a>Политика метаданных фото для System. photo. Ленсмануфактурер

Политика метаданных фотографии для свойства [System. photo. ленсмануфактурер](../properties/props-system-photo-lensmanufacturer.md) .

### <a name="pkey"></a>PKEY

\_Ленсмануфактурер фото на PKEY \_

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



| Заказ | Путь                                 | Формат диска | Обязательно |
|-------|--------------------------------------|-------------|----------|
| 1     | /КСМП/микрософтфото: Ленсмануфактурер | Юникод     | Да      |



 

### <a name="precedence-of-paths-tiff"></a>Приоритет путей (TIFF)

Если файл имеет формат TIFF, то при чтении или записи данных обработчик будет использовать следующий порядок приоритета.



| Заказ | Путь                                     | Формат диска | Обязательно |
|-------|------------------------------------------|-------------|----------|
| 1     | /ИФД/КСМП/микрософтфото: Ленсмануфактурер | Юникод     | Да      |



 

## <a name="remarks"></a>Комментарии

## <a name="related-topics"></a>См. также

<dl> <dt>

[System. photo. Ленсмануфактурер](../properties/props-system-photo-lensmanufacturer.md)
</dt> </dl>

 

 
