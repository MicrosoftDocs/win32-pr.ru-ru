---
description: Политика метаданных фотографии для свойства System. photo. Ленсмодел.
ms.assetid: 39aeff17-e8d3-4ceb-86a1-1749d2ca98d6
title: Политика метаданных фото для System. photo. Ленсмодел
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8a5249136346407ab9fcd1e4802d6910d3e514a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081306"
---
# <a name="systemphotolensmodel-photo-metadata-policy"></a>Политика метаданных фото для System. photo. Ленсмодел

Политика метаданных фотографии для свойства [System. photo. ленсмодел](../properties/props-system-photo-lensmodel.md) .

### <a name="pkey"></a>PKEY

\_Ленсмодел фото на PKEY \_

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



| Заказ | Путь                          | Формат диска | Обязательно |
|-------|-------------------------------|-------------|----------|
| 1     | /КСМП/микрософтфото: Ленсмодел | Юникод     | Да      |



 

### <a name="precedence-of-paths-tiff"></a>Приоритет путей (TIFF)

Если файл имеет формат TIFF, то при чтении или записи данных обработчик будет использовать следующий порядок приоритета.



| Заказ | Путь                              | Формат диска | Обязательно |
|-------|-----------------------------------|-------------|----------|
| 1     | /ИФД/КСМП/микрософтфото: Ленсмодел | Юникод     | Да      |



 

## <a name="remarks"></a>Комментарии

## <a name="related-topics"></a>См. также

<dl> <dt>

[System. photo. Ленсмодел](../properties/props-system-photo-lensmodel.md)
</dt> </dl>

 

 
