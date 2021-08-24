---
description: Политика метаданных фотографии для свойства System. photo. Ленсмануфактурер.
ms.assetid: ee25da96-982f-475e-8957-e24ef7721b78
title: Политика метаданных фото для System. photo. Ленсмануфактурер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f6beebc06ce690b05da62c023480bec25b675a7a9ec6093cec1752ac3a0e343
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119881989"
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



| Номер | Путь                                 | Формат диска | Обязательно |
|-------|--------------------------------------|-------------|----------|
| 1     | /КСМП/микрософтфото: Ленсмануфактурер | Юникод     | Да      |



 

### <a name="precedence-of-paths-tiff"></a>Приоритет путей (TIFF)

Если файл имеет формат TIFF, то при чтении или записи данных обработчик будет использовать следующий порядок приоритета.



| Номер | Путь                                     | Формат диска | Обязательно |
|-------|------------------------------------------|-------------|----------|
| 1     | /ИФД/КСМП/микрософтфото: Ленсмануфактурер | Юникод     | Да      |



 

## <a name="remarks"></a>Remarks

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[System. photo. Ленсмануфактурер](../properties/props-system-photo-lensmanufacturer.md)
</dt> </dl>

 

 
