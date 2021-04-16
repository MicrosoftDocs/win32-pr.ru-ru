---
description: Политика метаданных фотографии для свойства System. photo. Камерамануфактурер.
ms.assetid: 6710161c-4835-4385-9d4c-566acc000925
title: Политика метаданных фото для System. photo. Камерамануфактурер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd1d2765b6c787b7d7ad421300f1c3492669830b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702905"
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



| Заказ | Путь                   | Формат диска |
|-------|------------------------|-------------|
| 1     | /APP1/IFD/{ushort = 271} | ascii       |
| 2     | /КСМП/Тифф: make         | Юникод     |
| 3     | /КСМП/Тифф: make         | Юникод     |



 

### <a name="write-paths"></a>Пути записи



| Заказ | Путь                   | Формат диска |
|-------|------------------------|-------------|
| 1     | /APP1/IFD/{ushort = 271} | ascii       |
| 2     | /КСМП/Тифф: make         | Юникод     |
| 3     | /КСМП/Тифф: make         | Юникод     |



 

### <a name="remove-paths"></a>Удалить пути



| Заказ | Путь                   |
|-------|------------------------|
| 1     | /APP1/IFD/{ushort = 271} |
| 2     | /КСМП/Тифф: make         |
| 3     | /КСМП/Тифф: make         |



 

### <a name="tiff-policy"></a>Политика TIFF

### <a name="read-paths"></a>Пути чтения



| Заказ | Путь               | Формат диска |
|-------|--------------------|-------------|
| 1     | /ИФД/{ушорт = 271}  | ascii       |
| 2     | /ИФД/КСМП/Тифф: make | Юникод     |
| 3     | /ИФД/КСМП/Тифф: make | Юникод     |



 

### <a name="write-paths"></a>Пути записи



| Заказ | Путь               | Формат диска |
|-------|--------------------|-------------|
| 1     | /ИФД/{ушорт = 271}  | ascii       |
| 2     | /ИФД/КСМП/Тифф: make | Юникод     |
| 3     | /ИФД/КСМП/Тифф: make | Юникод     |



 

### <a name="remove-paths"></a>Удалить пути



| Заказ | Путь               |
|-------|--------------------|
| 1     | /ИФД/{ушорт = 271}  |
| 2     | /ИФД/КСМП/Тифф: make |
| 3     | /ИФД/КСМП/Тифф: make |



 

## <a name="remarks"></a>Комментарии

## <a name="related-topics"></a>См. также

<dl> <dt>

[System. photo. Камерамануфактурер](../properties/props-system-photo-cameramanufacturer.md)
</dt> </dl>

 

 
