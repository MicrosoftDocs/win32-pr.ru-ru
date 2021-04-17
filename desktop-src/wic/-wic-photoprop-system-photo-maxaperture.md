---
description: Политика метаданных фотографии для свойства System. photo. Максапертуре.
ms.assetid: 9d12d265-0b0a-44d9-bbf6-ca7d748382ee
title: Политика метаданных фото для System. photo. Максапертуре
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9f3dab4d5ebf89033de03dfce887a7cea10fa11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674001"
---
# <a name="systemphotomaxaperture-photo-metadata-policy"></a>Политика метаданных фото для System. photo. Максапертуре

Политика метаданных фотографии для свойства [System. photo. максапертуре](../properties/props-system-photo-maxaperture.md) .

### <a name="pkey"></a>PKEY

\_Максапертуре фото на PKEY \_

### <a name="containers"></a>Контейнеры

JPEG, TIFF

### <a name="read-only"></a>Только для чтения

Да

### <a name="output-propvariant-type"></a>Тип выходного ПРОПВАРИАНТ

VT \_ R8

### <a name="input-type"></a>Тип входных данных

Double

### <a name="conflict-resolution-policy"></a>Политика разрешения конфликтов

Это значение формируется из System. photo. Максапертуренумератор и System. photo. Максапертуреденоминатор. Он не может быть записан напрямую. Выверяются значения из разных схем.

### <a name="jpeg-policy"></a>Политика JPEG

### <a name="read-paths"></a>Пути чтения



| Заказ | Путь                          | Формат диска |
|-------|-------------------------------|-------------|
| 1     | /APP1/IFD/EXIF/{ushort = 37381} |             |
| 2     | /КСМП/ексиф: Максапертуревалуе    |             |



 

### <a name="write-paths"></a>Пути записи



| Заказ | Путь                          | Формат диска |
|-------|-------------------------------|-------------|
| 1     | /APP1/IFD/EXIF/{ushort = 37381} |             |
| 2     | /КСМП/ексиф: Максапертуревалуе    |             |



 

### <a name="remove-paths"></a>Удалить пути



| Заказ | Путь                          |
|-------|-------------------------------|
| 1     | /APP1/IFD/EXIF/{ushort = 37381} |
| 2     | /КСМП/ексиф: максапертуревалуе    |



 

### <a name="tiff-policies"></a>Политики TIFF

### <a name="read-paths"></a>Пути чтения



| Заказ | Путь                           | Формат диска |
|-------|--------------------------------|-------------|
| 1     | /ИФД/ексиф/{ушорт = 37381}       |             |
| 2     | /ИФД/КСМП/ексиф: Максапертуревалуе |             |



 

### <a name="write-paths"></a>Пути записи



| Заказ | Путь                           | Формат диска |
|-------|--------------------------------|-------------|
| 1     | /ИФД/ексиф/{ушорт = 37381}       |             |
| 2     | /ИФД/КСМП/ексиф: Максапертуревалуе |             |



 

### <a name="remove-paths"></a>Удалить пути



| Заказ | Путь                           |
|-------|--------------------------------|
| 1     | /ИФД/ексиф/{ушорт = 37381}       |
| 2     | /ИФД/КСМП/ексиф: максапертуревалуе |



 

## <a name="remarks"></a>Комментарии

## <a name="related-topics"></a>См. также

<dl> <dt>

[System. photo. Максапертуре](../properties/props-system-photo-maxaperture.md)
</dt> </dl>

 

 
