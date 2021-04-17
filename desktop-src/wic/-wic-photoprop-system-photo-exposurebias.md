---
description: Политика метаданных фотографии для свойства System. photo. Експосуребиас.
ms.assetid: 00ebe037-0116-4d75-868b-d75b3e58a84d
title: Политика метаданных фото для System. photo. Експосуребиас
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 709aa21da7cec56d36b5de643681a592873717bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674006"
---
# <a name="systemphotoexposurebias-photo-metadata-policy"></a>Политика метаданных фото для System. photo. Експосуребиас

Политика метаданных фотографии для свойства [System. photo. експосуребиас](../properties/props-system-photo-exposurebias.md) .

### <a name="pkey"></a>PKEY

\_Експосуребиас фото на PKEY \_

### <a name="containers"></a>Контейнеры

JPEG, TIFF

### <a name="read-only"></a>Только для чтения

Да

### <a name="output-propvariant-type"></a>Тип выходного ПРОПВАРИАНТ

VT \_ R8

### <a name="conflict-resolution-policy"></a>Политика разрешения конфликтов

Это значение формируется из System. photo. Експосуребиаснумератор и System. photo. Експосуребиасденоминатор. Он не может быть записан напрямую. Выверяются значения из разных схем.

### <a name="jpeg-policy"></a>Политика JPEG

### <a name="read-paths"></a>Пути чтения



| Заказ | Путь                          | Формат диска |
|-------|-------------------------------|-------------|
| 1     | /APP1/IFD/EXIF/{ushort = 37380} |             |
| 2     | /КСМП/ексиф: Експосуребиасвалуе   |             |



 

### <a name="write-paths"></a>Пути записи



| Заказ | Путь                          | Формат диска |
|-------|-------------------------------|-------------|
| 1     | /APP1/IFD/EXIF/{ushort = 37380} |             |
| 2     | /КСМП/ексиф: Експосуребиасвалуе   |             |



 

### <a name="remove-paths"></a>Удалить пути



| Заказ | Путь                          |
|-------|-------------------------------|
| 1     | /APP1/IFD/EXIF/{ushort = 37380} |
| 2     | /КСМП/ексиф: експосуребиасвалуе   |



 

### <a name="tiff-policies"></a>Политики TIFF

### <a name="read-paths"></a>Пути чтения



| Заказ | Путь                            | Формат диска |
|-------|---------------------------------|-------------|
| 1     | /ИФД/ексиф/{ушорт = 37380}        |             |
| 2     | /ИФД/КСМП/ексиф: Експосуребиасвалуе |             |



 

### <a name="write-paths"></a>Пути записи



| Заказ | Путь                            | Формат диска |
|-------|---------------------------------|-------------|
| 1     | /ИФД/ексиф/{ушорт = 37380}        |             |
| 2     | /ИФД/КСМП/ексиф: Експосуребиасвалуе |             |



 

### <a name="remove-paths"></a>Удалить пути



| Заказ | Путь                            |
|-------|---------------------------------|
| 1     | /ИФД/ексиф/{ушорт = 37380}        |
| 2     | /ИФД/КСМП/ексиф: експосуребиасвалуе |



 

## <a name="remarks"></a>Комментарии

## <a name="related-topics"></a>См. также

<dl> <dt>

[System. photo. Експосуребиас](../properties/props-system-photo-exposurebias.md)
</dt> </dl>

 

 
