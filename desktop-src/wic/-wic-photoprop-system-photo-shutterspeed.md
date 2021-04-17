---
description: Политика метаданных фотографии для свойства System. photo. Шуттерспид.
ms.assetid: f320944c-978d-4a3c-9bf8-5c5652123e29
title: Политика метаданных фото для System. photo. Шуттерспид
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8df8c9e7fda5643fed022f67c3b6b7846e7a72f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674127"
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



| Заказ | Путь                          | Формат диска |
|-------|-------------------------------|-------------|
| 1     | /APP1/IFD/EXIF/{ushort = 37377} |             |
| 2     | /КСМП/ексиф: Шуттерспидвалуе   |             |



 

### <a name="write-paths"></a>Пути записи



| Заказ | Путь                          | Формат диска |
|-------|-------------------------------|-------------|
| 1     | /APP1/IFD/EXIF/{ushort = 37377} |             |
| 2     | /КСМП/ексиф: Шуттерспидвалуе   |             |



 

### <a name="remove-paths"></a>Удалить пути



| Заказ | Путь                          |
|-------|-------------------------------|
| 1     | /APP1/IFD/EXIF/{ushort = 37377} |
| 2     | /КСМП/ексиф: шуттерспидвалуе   |



 

### <a name="tiff-policies"></a>Политики TIFF

### <a name="read-paths"></a>Пути чтения



| Заказ | Путь                            | Формат диска |
|-------|---------------------------------|-------------|
| 1     | /ИФД/ексиф/{ушорт = 37377}        |             |
| 2     | /ИФД/КСМП/ексиф: Шуттерспидвалуе |             |



 

### <a name="write-paths"></a>Пути записи



| Заказ | Путь                            | Формат диска |
|-------|---------------------------------|-------------|
| 1     | /ИФД/ексиф/{ушорт = 37377}        |             |
| 2     | /ИФД/КСМП/ексиф: Шуттерспидвалуе |             |



 

### <a name="remove-paths"></a>Удалить пути



| Заказ | Путь                            |
|-------|---------------------------------|
| 1     | /ИФД/ексиф/{ушорт = 37377}        |
| 2     | /ИФД/КСМП/ексиф: шуттерспидвалуе |



 

## <a name="remarks"></a>Комментарии

## <a name="related-topics"></a>См. также

<dl> <dt>

[System. photo. Шуттерспид](../properties/props-system-photo-shutterspeed.md)
</dt> </dl>

 

 
