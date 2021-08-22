---
description: Политика метаданных фотографии для свойства System. photo. Шуттерспид.
ms.assetid: f320944c-978d-4a3c-9bf8-5c5652123e29
title: Политика метаданных фото для System. photo. Шуттерспид
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ad11550a19cd043fd5d182b2cf508aec3e26c64a0dc2ee1d1c24576ebf18f8e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118710103"
---
# <a name="systemphotoshutterspeed-photo-metadata-policy"></a>Политика метаданных фото для System. photo. Шуттерспид

Политика метаданных фотографии для свойства [System. photo. шуттерспид](../properties/props-system-photo-shutterspeed.md) .

### <a name="pkey"></a>PKEY

\_Шуттерспид фото на PKEY \_

### <a name="containers"></a>Контейнеры

JPEG, TIFF

### <a name="read-only"></a>Только для чтения

Да

### <a name="output-propvariant-type"></a>Тип выходного ПРОПВАРИАНТ

VT \_ R8

### <a name="conflict-resolution-policy"></a>Политика разрешения конфликтов

Это значение формируется из System. photo. Шуттерспиднумератор и System. photo. Шуттерспидденоминатор. Он не может быть записан напрямую. Выверяются значения из разных схем.

### <a name="jpeg-policy"></a>Политика JPEG

### <a name="read-paths"></a>Пути чтения



| Номер | Путь                          | Формат диска |
|-------|-------------------------------|-------------|
| 1     | /APP1/IFD/EXIF/{ushort = 37377} |             |
| 2     | /КСМП/ексиф: Шуттерспидвалуе   |             |



 

### <a name="write-paths"></a>Пути записи



| Номер | Путь                          | Формат диска |
|-------|-------------------------------|-------------|
| 1     | /APP1/IFD/EXIF/{ushort = 37377} |             |
| 2     | /КСМП/ексиф: Шуттерспидвалуе   |             |



 

### <a name="remove-paths"></a>Удалить пути



| Номер | Путь                          |
|-------|-------------------------------|
| 1     | /APP1/IFD/EXIF/{ushort = 37377} |
| 2     | /КСМП/ексиф: шуттерспидвалуе   |



 

### <a name="tiff-policies"></a>Политики TIFF

### <a name="read-paths"></a>Пути чтения



| Номер | Путь                            | Формат диска |
|-------|---------------------------------|-------------|
| 1     | /ИФД/ексиф/{ушорт = 37377}        |             |
| 2     | /ИФД/КСМП/ексиф: Шуттерспидвалуе |             |



 

### <a name="write-paths"></a>Пути записи



| Номер | Путь                            | Формат диска |
|-------|---------------------------------|-------------|
| 1     | /ИФД/ексиф/{ушорт = 37377}        |             |
| 2     | /ИФД/КСМП/ексиф: Шуттерспидвалуе |             |



 

### <a name="remove-paths"></a>Удалить пути



| Номер | Путь                            |
|-------|---------------------------------|
| 1     | /ИФД/ексиф/{ушорт = 37377}        |
| 2     | /ИФД/КСМП/ексиф: шуттерспидвалуе |



 

## <a name="remarks"></a>Remarks

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[System. photo. Шуттерспид](../properties/props-system-photo-shutterspeed.md)
</dt> </dl>

 

 
