---
description: Политика метаданных фотографии для свойства System. Comment.
ms.assetid: 02a6ac18-ad69-4880-a267-8330d648c0d9
title: Политика метаданных фотографии System. Comment
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2aa1a62fd5afa131a714c365ed2fda2c307bc955
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883902"
---
# <a name="systemcomment-photo-metadata-policy"></a>Политика метаданных фотографии System. Comment

Политика метаданных фотографии для свойства [System. Comment](../properties/props-system-comment.md) .

### <a name="pkey"></a>PKEY

\_Комментарий PKEY

### <a name="containers"></a>Контейнеры

JPEG, TIFF

### <a name="read-only"></a>Только для чтения

Нет

### <a name="output-propvariant-type"></a>Тип выходного ПРОПВАРИАНТ

VT \_ LPWSTR

### <a name="input-propvariant-type"></a>Тип входного ПРОПВАРИАНТ

VT \_ LPWSTR или VT \_ LPSTR

### <a name="conflict-resolution-policy"></a>Политика разрешения конфликтов

Выверяются значения из разных схем.

### <a name="jpeg-policy"></a>Политика JPEG

### <a name="read-paths"></a>Пути чтения



| Порядок | путь                                | Формат диска    |
|-------|-------------------------------------|----------------|
| 1     | /APP1/IFD/{ushort = 40092}            | байт в Юникоде \_ |
| 2     | /APP1/IFD/{ushort = 37510}            | Юникод        |
| 3     | /КСМП/ &lt; ксмпалт &gt; EXIF: усеркоммент | Юникод        |



 

### <a name="write-paths"></a>Пути записи



| Порядок | путь                     | Формат диска    |
|-------|--------------------------|----------------|
| 1     | /APP1/IFD/{ushort = 40092} | байт в Юникоде \_ |



 

### <a name="remove-paths"></a>Удалить пути



| Порядок | путь                          |
|-------|-------------------------------|
| 1     | /APP1/IFD/{ushort = 40092}      |
| 2     | /APP1/IFD/EXIF/{ushort = 37510} |
| 3     | /КСМП/ексиф: Усеркоммент         |



 

### <a name="tiff-policy"></a>Политика TIFF

### <a name="read-paths"></a>Пути чтения



| Порядок | путь                                    | Формат диска    |
|-------|-----------------------------------------|----------------|
| 1     | /ИФД/{ушорт = 40092}                     | байт в Юникоде \_ |
| 2     | /ИФД/{ушорт = 37510}                     | Юникод        |
| 3     | /ИФД/КСМП/ &lt; ксмпалт &gt; EXIF: усеркоммент | Юникод        |



 

### <a name="write-paths"></a>Пути записи



| Порядок | путь                | Формат диска    |
|-------|---------------------|----------------|
| 1     | /ИФД/{ушорт = 40092} | байт в Юникоде \_ |



 

### <a name="remove-paths"></a>Удалить пути



| Порядок | путь                      |
|-------|---------------------------|
| 1     | /ИФД/{ушорт = 40092}       |
| 2     | /ИФД/{ушорт = 37510}       |
| 3     | /ИФД/КСМП/ексиф: Усеркоммент |



 

## <a name="remarks"></a>Комментарии

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[System. комментарий](../properties/props-system-comment.md)
</dt> </dl>

 

 
