---
description: Политика метаданных фотографии для свойства System. рейтингов.
ms.assetid: e4d2c12e-617a-431e-9062-62acf6ef21c8
title: Политика метаданных фотографии System. рейтингов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47c4f7d89b1ff1ea8326c2d26fba0d331db1eab1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347175"
---
# <a name="systemrating-photo-metadata-policy"></a>Политика метаданных фотографии System. рейтингов

Политика метаданных фотографии для свойства [System. рейтингов](../properties/props-system-rating.md) .

### <a name="pkey"></a>PKEY

\_Оценка PKEY

### <a name="containers"></a>Контейнеры

JPEG, TIFF

### <a name="read-only"></a>Только для чтения

Нет

### <a name="output-propvariant-type"></a>Тип выходного ПРОПВАРИАНТ

VT \_ UI4

### <a name="input-propvariant-type"></a>Тип входного ПРОПВАРИАНТ

Может быть VT \_ UI1, VT \_ UI2 или VT \_ UI4. Значение может находиться в диапазоне от 0 до 99.

### <a name="conflict-resolution-policy"></a>Политика разрешения конфликтов

Выверяются значения из разных схем.

### <a name="jpeg-policy"></a>Политика JPEG

### <a name="read-paths"></a>Пути чтения



| Заказ | Путь                       | Формат диска |
|-------|----------------------------|-------------|
| 1     | /APP1/IFD/{ushort = 18249}   | ushort      |
| 2     | /КСМП/микрософтфото: Оценка | Юникод     |



 

### <a name="write-paths"></a>Пути записи



| Заказ | Путь                       | Формат диска |
|-------|----------------------------|-------------|
| 1     | /APP1/IFD/{ushort = 18249}   | ushort      |
| 2     | /КСМП/микрософтфото: Оценка | Юникод     |



 

### <a name="remove-paths"></a>Удалить пути



| Заказ | Путь                       |
|-------|----------------------------|
| 1     | /APP1/IFD/{ushort = 18249}   |
| 2     | /КСМП/микрософтфото: Оценка |



 

### <a name="tiff-policies"></a>Политики TIFF

### <a name="read-paths"></a>Пути чтения



| Заказ | Путь                           | Формат диска |
|-------|--------------------------------|-------------|
| 1     | /ИФД/{ушорт = 18249}            | ushort      |
| 2     | /ИФД/КСМП/микрософтфото: Оценка | Юникод     |



 

### <a name="write-paths"></a>Пути записи



| Заказ | Путь                           | Формат диска |
|-------|--------------------------------|-------------|
| 1     | /ИФД/{ушорт = 18249}            | ushort      |
| 2     | /ИФД/КСМП/микрософтфото: Оценка | Юникод     |



 

### <a name="remove-paths"></a>Удалить пути



| Заказ | Путь                           |
|-------|--------------------------------|
| 1     | /ИФД/{ушорт = 18249}            |
| 2     | /ИФД/КСМП/микрософтфото: Оценка |



 

## <a name="remarks"></a>Комментарии

## <a name="related-topics"></a>См. также

<dl> <dt>

[System. Оценка](../properties/props-system-rating.md)
</dt> </dl>

 

 
