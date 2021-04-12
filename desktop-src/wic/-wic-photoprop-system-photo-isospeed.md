---
description: Политика метаданных фотографии для свойства System. photo. Исоспид.
ms.assetid: 22b5552c-41b1-4090-a827-b920dcbba5e9
title: Политика метаданных фото для System. photo. Исоспид
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2988f774f70721ab1817ffaf605098ab1164316a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346602"
---
# <a name="systemphotoisospeed-photo-metadata-policy"></a>Политика метаданных фото для System. photo. Исоспид

Политика метаданных фотографии для свойства [System. photo. исоспид](../properties/props-system-photo-focallengthinfilm.md) .

### <a name="pkey"></a>PKEY

\_Исоспид фото на PKEY \_

### <a name="containers"></a>Контейнеры

JPEG, TIFF

### <a name="read-only"></a>Только для чтения

Нет

### <a name="output-propvariant-type"></a>Тип выходного ПРОПВАРИАНТ

VT \_ UI2

### <a name="input-type"></a>Тип входных данных

UShort

### <a name="conflict-resolution-policy"></a>Политика разрешения конфликтов

Выверяются значения из разных схем.

### <a name="jpeg-policy"></a>Политика JPEG

### <a name="read-paths"></a>Пути чтения



| Заказ | Путь                                    | Формат диска |
|-------|-----------------------------------------|-------------|
| 1     | /APP1/IFD/EXIF/{ushort = 34855}           | ushort      |
| 2     | /КСМП/ <xmpseq> EXIF: исоспидратингс | Юникод     |
| 3     | /КСМП/ексиф: Исоспид                      | Юникод     |



 

### <a name="write-paths"></a>Пути записи



| Заказ | Путь                                    | Формат диска |
|-------|-----------------------------------------|-------------|
| 1     | /APP1/IFD/EXIF/{ushort = 34855}           | ushort      |
| 2     | /КСМП/ <xmpseq> EXIF: исоспидратингс | Юникод     |
| 3     | /КСМП/ексиф: Исоспид                      | Юникод     |



 

### <a name="remove-paths"></a>Удалить пути



| Заказ | Путь                                    |
|-------|-----------------------------------------|
| 1     | /APP1/IFD/EXIF/{ushort = 34855}           |
| 2     | /КСМП/ <xmpseq> EXIF: исоспидратингс |
| 3     | /КСМП/ексиф: исоспид                      |



 

### <a name="tiff-policies"></a>Политики TIFF

### <a name="read-paths"></a>Пути чтения



| Заказ | Путь                                        | Формат диска |
|-------|---------------------------------------------|-------------|
| 1     | /ИФД/ексиф/{ушорт = 34855}                    | ushort      |
| 2     | /ИФД/КСМП/ <xmpseq> EXIF: исоспидратингс | Юникод     |
| 3     | /ИФД/КСМП/ексиф: Исоспид                      | Юникод     |



 

### <a name="write-paths"></a>Пути записи



| Заказ | Путь                                        | Формат диска |
|-------|---------------------------------------------|-------------|
| 1     | /ИФД/ексиф/{ушорт = 34855}                    | ushort      |
| 2     | /ИФД/КСМП/ <xmpseq> EXIF: исоспидратингс | Юникод     |
| 3     | /ИФД/КСМП/ексиф: Исоспид                      | Юникод     |



 

### <a name="remove-paths"></a>Удалить пути



| Заказ | Путь                                        |
|-------|---------------------------------------------|
| 1     | /ИФД/ексиф/{ушорт = 34855}                    |
| 2     | /ИФД/КСМП/ <xmpseq> EXIF: исоспидратингс |
| 3     | /ИФД/КСМП/ексиф: исоспид                      |



 

## <a name="remarks"></a>Комментарии

## <a name="related-topics"></a>См. также

<dl> <dt>

[System. photo. Исоспид](../properties/props-system-photo-focallengthinfilm.md)
</dt> </dl>

 

 
