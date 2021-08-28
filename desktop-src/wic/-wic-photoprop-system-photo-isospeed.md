---
description: Политика метаданных фотографии для свойства System. photo. Исоспид.
ms.assetid: 22b5552c-41b1-4090-a827-b920dcbba5e9
title: Политика метаданных фото для System. photo. Исоспид
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6612bffdeaafb69ea1b1122a1d75c00214d366e9
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881641"
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



| Порядок | путь                                    | Формат диска |
|-------|-----------------------------------------|-------------|
| 1     | /APP1/IFD/EXIF/{ushort = 34855}           | ushort      |
| 2     | /КСМП/ &lt; ксмпсек &gt; EXIF: исоспидратингс | Юникод     |
| 3     | /КСМП/ексиф: Исоспид                      | Юникод     |



 

### <a name="write-paths"></a>Пути записи



| Порядок | путь                                    | Формат диска |
|-------|-----------------------------------------|-------------|
| 1     | /APP1/IFD/EXIF/{ushort = 34855}           | ushort      |
| 2     | /КСМП/ &lt; ксмпсек &gt; EXIF: исоспидратингс | Юникод     |
| 3     | /КСМП/ексиф: Исоспид                      | Юникод     |



 

### <a name="remove-paths"></a>Удалить пути



| Порядок | путь                                    |
|-------|-----------------------------------------|
| 1     | /APP1/IFD/EXIF/{ushort = 34855}           |
| 2     | /КСМП/ &lt; ксмпсек &gt; EXIF: исоспидратингс |
| 3     | /КСМП/ексиф: исоспид                      |



 

### <a name="tiff-policies"></a>Политики TIFF

### <a name="read-paths"></a>Пути чтения



| Порядок | путь                                        | Формат диска |
|-------|---------------------------------------------|-------------|
| 1     | /ИФД/ексиф/{ушорт = 34855}                    | ushort      |
| 2     | /ИФД/КСМП/ &lt; ксмпсек &gt; EXIF: исоспидратингс | Юникод     |
| 3     | /ИФД/КСМП/ексиф: Исоспид                      | Юникод     |



 

### <a name="write-paths"></a>Пути записи



| Порядок | путь                                        | Формат диска |
|-------|---------------------------------------------|-------------|
| 1     | /ИФД/ексиф/{ушорт = 34855}                    | ushort      |
| 2     | /ИФД/КСМП/ &lt; ксмпсек &gt; EXIF: исоспидратингс | Юникод     |
| 3     | /ИФД/КСМП/ексиф: Исоспид                      | Юникод     |



 

### <a name="remove-paths"></a>Удалить пути



| Порядок | путь                                        |
|-------|---------------------------------------------|
| 1     | /ИФД/ексиф/{ушорт = 34855}                    |
| 2     | /ИФД/КСМП/ &lt; ксмпсек &gt; EXIF: исоспидратингс |
| 3     | /ИФД/КСМП/ексиф: исоспид                      |



 

## <a name="remarks"></a>Комментарии

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[System. photo. Исоспид](../properties/props-system-photo-focallengthinfilm.md)
</dt> </dl>

 

 
