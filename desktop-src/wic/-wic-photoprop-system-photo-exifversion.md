---
description: Политика метаданных фотографии для свойства System. photo. Ексифверсион.
ms.assetid: 0f9c5ea8-918f-4101-8492-3f408145a73e
title: Политика метаданных фото для System. photo. Ексифверсион
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1eb823db41cb54a06fba235df5be4bb4acd55ea4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272092"
---
# <a name="systemphotoexifversion-photo-metadata-policy"></a>Политика метаданных фото для System. photo. Ексифверсион

Политика метаданных фотографии для свойства [System. photo. ексифверсион](../properties/props-system-photo-exifversion.md) .

### <a name="pkey"></a>PKEY

\_Ексифверсион фото на PKEY \_

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

### <a name="jpeg-policy"></a>Политика JPEG

### <a name="read-paths"></a>Пути чтения



| Заказ | Путь                          | Формат диска   |
|-------|-------------------------------|---------------|
| 1     | /APP1/IFD/EXIF/{ushort = 36864} | \_версия EXIF |
| 2     | /КСМП/ексиф: Ексифверсион         | Юникод       |



 

### <a name="write-paths"></a>Пути записи



| Заказ | Путь                          | Формат диска   |
|-------|-------------------------------|---------------|
| 1     | /APP1/IFD/EXIF/{ushort = 36864} | \_версия EXIF |
| 2     | /КСМП/ексиф: Ексифверсион         | Юникод       |



 

### <a name="remove-paths"></a>Удалить пути



| Заказ | Путь                          |
|-------|-------------------------------|
| 1     | /APP1/IFD/EXIF/{ushort = 36864} |
| 2     | /КСМП/ексиф: Ексифверсион         |



 

### <a name="tiff-policy"></a>Политика TIFF

### <a name="read-paths"></a>Пути чтения



| Заказ | Путь                      | Формат диска   |
|-------|---------------------------|---------------|
| 1     | /ИФД/ексиф/{ушорт = 36864}  | \_версия EXIF |
| 2     | /ИФД/КСМП/ексиф: Ексифверсион | Юникод       |



 

### <a name="write-paths"></a>Пути записи



| Заказ | Путь                      | Формат диска   |
|-------|---------------------------|---------------|
| 1     | /ИФД/ексиф/{ушорт = 36864}  | \_версия EXIF |
| 2     | /ИФД/КСМП/ексиф: Ексифверсион | Юникод       |



 

### <a name="remove-paths"></a>Удалить пути



| Заказ | Путь                      |
|-------|---------------------------|
| 1     | /ИФД/ексиф/{ушорт = 36864}  |
| 2     | /ИФД/КСМП/ексиф: Ексифверсион |



 

## <a name="remarks"></a>Комментарии

## <a name="related-topics"></a>См. также

<dl> <dt>

[System. photo. Ексифверсион](../properties/props-system-photo-exifversion.md)
</dt> </dl>

 

 
