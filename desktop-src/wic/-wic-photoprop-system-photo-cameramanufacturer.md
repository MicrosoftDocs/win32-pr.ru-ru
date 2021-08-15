---
description: Политика метаданных фотографии для свойства System. photo. Камерамануфактурер.
ms.assetid: 6710161c-4835-4385-9d4c-566acc000925
title: Политика метаданных фото для System. photo. Камерамануфактурер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37744420babedf6b398cdf3ab9007c3895c09d33b9254221b5ba4760ab917a0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119087090"
---
# <a name="systemphotocameramanufacturer-photo-metadata-policy"></a>Политика метаданных фото для System. photo. Камерамануфактурер

Политика метаданных фотографии для свойства [System. photo. камерамануфактурер](../properties/props-system-photo-cameramanufacturer.md) .

### <a name="pkey"></a>PKEY

\_Камерамануфактурер фото на PKEY \_

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



| Номер | Путь                   | Формат диска |
|-------|------------------------|-------------|
| 1     | /APP1/IFD/{ushort = 271} | ascii       |
| 2     | /КСМП/Тифф: make         | Юникод     |
| 3     | /КСМП/Тифф: make         | Юникод     |



 

### <a name="write-paths"></a>Пути записи



| Номер | Путь                   | Формат диска |
|-------|------------------------|-------------|
| 1     | /APP1/IFD/{ushort = 271} | ascii       |
| 2     | /КСМП/Тифф: make         | Юникод     |
| 3     | /КСМП/Тифф: make         | Юникод     |



 

### <a name="remove-paths"></a>Удалить пути



| Номер | Путь                   |
|-------|------------------------|
| 1     | /APP1/IFD/{ushort = 271} |
| 2     | /КСМП/Тифф: make         |
| 3     | /КСМП/Тифф: make         |



 

### <a name="tiff-policy"></a>Политика TIFF

### <a name="read-paths"></a>Пути чтения



| Номер | Путь               | Формат диска |
|-------|--------------------|-------------|
| 1     | /ИФД/{ушорт = 271}  | ascii       |
| 2     | /ИФД/КСМП/Тифф: make | Юникод     |
| 3     | /ИФД/КСМП/Тифф: make | Юникод     |



 

### <a name="write-paths"></a>Пути записи



| Номер | Путь               | Формат диска |
|-------|--------------------|-------------|
| 1     | /ИФД/{ушорт = 271}  | ascii       |
| 2     | /ИФД/КСМП/Тифф: make | Юникод     |
| 3     | /ИФД/КСМП/Тифф: make | Юникод     |



 

### <a name="remove-paths"></a>Удалить пути



| Номер | Путь               |
|-------|--------------------|
| 1     | /ИФД/{ушорт = 271}  |
| 2     | /ИФД/КСМП/Тифф: make |
| 3     | /ИФД/КСМП/Тифф: make |



 

## <a name="remarks"></a>Remarks

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[System. photo. Камерамануфактурер](../properties/props-system-photo-cameramanufacturer.md)
</dt> </dl>

 

 
