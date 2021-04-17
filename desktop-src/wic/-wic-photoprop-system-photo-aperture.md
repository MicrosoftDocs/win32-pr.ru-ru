---
description: Политика метаданных фотографии для свойства System. photo. апертуры.
ms.assetid: 3048eb9d-4ed4-4b5b-960e-9d0fd6704041
title: Политика метаданных фотографии System. photo. апертуры
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc02826b0602d0052f129640901ac3564a0eadb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684292"
---
# <a name="systemphotoaperture-photo-metadata-policy"></a>Политика метаданных фотографии System. photo. апертуры

Политика метаданных фотографии для свойства [System. photo. апертуры](../properties/props-system-photo-aperture.md) .

### <a name="pkey"></a>PKEY

\_ \_ Фотоапертура PKEY

### <a name="containers"></a>Контейнеры

JPEG, TIFF

### <a name="read-only"></a>Только для чтения

Да

### <a name="output-propvariant-type"></a>Тип выходного ПРОПВАРИАНТ

VT \_ R8

### <a name="conflict-resolution-policy"></a>Политика разрешения конфликтов

Это значение формируется из System. photo. Апертуренумератор и System. photo. Апертуреденоминатор. Он не может быть записан напрямую. Выверяются значения из разных схем.

### <a name="jpeg-policy"></a>Политика JPEG

### <a name="read-paths"></a>Пути чтения



| Заказ | Путь                          | Формат диска |
|-------|-------------------------------|-------------|
| 1     | /APP1/IFD/EXIF/{ushort = 37378} |             |
| 2     | /КСМП/ексиф: Апертуревалуе       |             |



 

### <a name="write-paths"></a>Пути записи



| Заказ | Путь                          | Формат диска |
|-------|-------------------------------|-------------|
| 1     | /APP1/IFD/EXIF/{ushort = 37378} |             |
| 2     | /КСМП/ексиф: Апертуревалуе       |             |



 

### <a name="remove-paths"></a>Удалить пути



| Заказ | Путь                          |
|-------|-------------------------------|
| 1     | /APP1/IFD/EXIF/{ushort = 37378} |
| 2     | /КСМП/ексиф: апертуревалуе       |



 

### <a name="tiff-policies"></a>Политики TIFF

### <a name="read-paths"></a>Пути чтения



| Заказ | Путь                        | Формат диска |
|-------|-----------------------------|-------------|
| 1     | /ИФД/ексиф/{ушорт = 37378}    |             |
| 2     | /ИФД/КСМП/ексиф: Апертуревалуе |             |



 

### <a name="write-paths"></a>Пути записи



| Заказ | Путь                        | Формат диска |
|-------|-----------------------------|-------------|
| 1     | /ИФД/ексиф/{ушорт = 37378}    |             |
| 2     | /ИФД/КСМП/ексиф: Апертуревалуе |             |



 

### <a name="remove-paths"></a>Удалить пути



| Заказ | Путь                        |
|-------|-----------------------------|
| 1     | /ИФД/ексиф/{ушорт = 37378}    |
| 2     | /ИФД/КСМП/ексиф: апертуревалуе |



 

## <a name="remarks"></a>Комментарии

## <a name="related-topics"></a>См. также

<dl> <dt>

[System. photo. Апертура](../properties/props-system-photo-aperture.md)
</dt> </dl>

 

 
