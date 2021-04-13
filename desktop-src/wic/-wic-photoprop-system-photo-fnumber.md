---
description: Политика метаданных фотографии для свойства System. photo. Фнумбер.
ms.assetid: 434d52cb-c98d-4860-87f7-4aedab7f8188
title: Политика метаданных фото для System. photo. Фнумбер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c518ef2a05dde8fd7e812d1d76a79cbe3efb4217
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265289"
---
# <a name="systemphotofnumber-photo-metadata-policy"></a>Политика метаданных фото для System. photo. Фнумбер

Политика метаданных фотографии для свойства [System. photo. фнумбер](../properties/props-system-photo-fnumber.md) .

### <a name="pkey"></a>PKEY

\_Фнумбер фото на PKEY \_

### <a name="containers"></a>Контейнеры

JPEG, TIFF

### <a name="read-only"></a>Только для чтения

Да

### <a name="output-propvariant-type"></a>Тип выходного ПРОПВАРИАНТ

VT \_ R8

### <a name="conflict-resolution-policy"></a>Политика разрешения конфликтов

Это значение формируется из System. photo. Фнумбернумератор и System. photo. Фнумберденоминатор. Он не может быть записан напрямую. Выверяются значения из разных схем.

### <a name="jpeg-policy"></a>Политика JPEG

### <a name="read-paths"></a>Пути чтения



| Заказ | Путь                          | Формат диска |
|-------|-------------------------------|-------------|
| 1     | /APP1/IFD/EXIF/{ushort = 33437} |             |
| 2     | /КСМП/ексиф: Фнумбер             |             |



 

### <a name="write-paths"></a>Пути записи



|       |                               |             |     |
|-------|-------------------------------|-------------|-----|
| Заказ | Путь                          | Формат диска |     |
| 1     | /APP1/IFD/EXIF/{ushort = 33437} |             |     |
| 2     | /КСМП/ексиф: Фнумбер             |             |     |



 

### <a name="remove-paths"></a>Удалить пути



| Заказ | Путь                          |
|-------|-------------------------------|
| 1     | /APP1/IFD/EXIF/{ushort = 33437} |
| 2     | /КСМП/ексиф: фнумбер             |



 

### <a name="tiff-policies"></a>Политики TIFF

### <a name="read-paths"></a>Пути чтения



| Заказ | Путь                     | Формат диска |
|-------|--------------------------|-------------|
| 1     | /ИФД/ексиф/{ушорт = 33437} |             |
| 2     | /ИФД/КСМП/ексиф: Фнумбер    |             |



 

### <a name="write-paths"></a>Пути записи



| Заказ | Путь                     | Формат диска |
|-------|--------------------------|-------------|
| 1     | /ИФД/ексиф/{ушорт = 33437} |             |
| 2     | /ИФД/КСМП/ексиф: Фнумбер    |             |



 

### <a name="remove-paths"></a>Удалить пути



| Заказ | Путь                     |
|-------|--------------------------|
| 1     | /ИФД/ексиф/{ушорт = 33437} |
| 2     | /ИФД/КСМП/ексиф: фнумбер    |



 

## <a name="remarks"></a>Комментарии

## <a name="related-topics"></a>См. также

<dl> <dt>

[System. photo. Фнумбер](../properties/props-system-photo-fnumber.md)
</dt> </dl>

 

 
