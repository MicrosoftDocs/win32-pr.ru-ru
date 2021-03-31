---
description: Политика метаданных фотографии для свойства System. photo. Камерамодел.
ms.assetid: ff85e6ee-dc75-45bc-a406-2290b012c22d
title: Политика метаданных фото для System. photo. Камерамодел
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2cf9cbb2906f15d02e8d72219862c607d0f515a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912623"
---
# <a name="systemphotocameramodel-photo-metadata-policy"></a>Политика метаданных фото для System. photo. Камерамодел

Политика метаданных фотографии для свойства [System. photo. камерамодел](../properties/props-system-photo-cameramodel.md) .

### <a name="pkey"></a>PKEY

\_Камерамодел фото на PKEY \_

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
| 1     | /APP1/IFD/{ushort = 272} | ascii       |
| 2     | /КСМП/Тифф: модель        | Юникод     |
| 3     | /КСМП/Тифф: модель        | Юникод     |



 

### <a name="write-paths"></a>Пути записи



| Заказ | Путь                   | Формат диска |
|-------|------------------------|-------------|
| 1     | /APP1/IFD/{ushort = 272} | ascii       |
| 2     | /КСМП/Тифф: модель        | Юникод     |
| 3     | /КСМП/Тифф: модель        | Юникод     |



 

### <a name="remove-paths"></a>Удалить пути



| Заказ | Путь                   |
|-------|------------------------|
| 1     | /APP1/IFD/{ushort = 272} |
| 2     | /КСМП/Тифф: модель        |
| 3     | /КСМП/Тифф: модель        |



 

### <a name="tiff-policy"></a>Политика TIFF

### <a name="read-paths"></a>Пути чтения



| Заказ | Путь                | Формат диска |
|-------|---------------------|-------------|
| 1     | /ИФД/{ушорт = 272}   | ascii       |
| 2     | /ИФД/КСМП/Тифф: модель | Юникод     |
| 3     | /ИФД/КСМП/Тифф: модель | Юникод     |



 

### <a name="write-paths"></a>Пути записи



| Заказ | Путь                | Формат диска |
|-------|---------------------|-------------|
| 1     | /ИФД/{ушорт = 272}   | ascii       |
| 2     | /ИФД/КСМП/Тифф: модель | Юникод     |
| 3     | /ИФД/КСМП/Тифф: модель | Юникод     |



 

### <a name="remove-paths"></a>Удалить пути



| Заказ | Путь                |
|-------|---------------------|
| 1     | /ИФД/{ушорт = 272}   |
| 2     | /ИФД/КСМП/Тифф: модель |
| 3     | /ИФД/КСМП/Тифф: модель |



 

## <a name="remarks"></a>Комментарии

## <a name="related-topics"></a>См. также

<dl> <dt>

[System. photo. Камерамодел](../properties/props-system-photo-cameramodel.md)
</dt> </dl>

 

 
