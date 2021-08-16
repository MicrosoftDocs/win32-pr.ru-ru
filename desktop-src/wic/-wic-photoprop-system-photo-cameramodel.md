---
description: Политика метаданных фотографии для свойства System. photo. Камерамодел.
ms.assetid: ff85e6ee-dc75-45bc-a406-2290b012c22d
title: Политика метаданных фото для System. photo. Камерамодел
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e205d4d886d050e45b958f2ba0f06c6411584c4a96a717378f243e5d1dd4fae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119882054"
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



| Номер | Путь                   | Формат диска |
|-------|------------------------|-------------|
| 1     | /APP1/IFD/{ushort = 272} | ascii       |
| 2     | /КСМП/Тифф: модель        | Юникод     |
| 3     | /КСМП/Тифф: модель        | Юникод     |



 

### <a name="write-paths"></a>Пути записи



| Номер | Путь                   | Формат диска |
|-------|------------------------|-------------|
| 1     | /APP1/IFD/{ushort = 272} | ascii       |
| 2     | /КСМП/Тифф: модель        | Юникод     |
| 3     | /КСМП/Тифф: модель        | Юникод     |



 

### <a name="remove-paths"></a>Удалить пути



| Номер | Путь                   |
|-------|------------------------|
| 1     | /APP1/IFD/{ushort = 272} |
| 2     | /КСМП/Тифф: модель        |
| 3     | /КСМП/Тифф: модель        |



 

### <a name="tiff-policy"></a>Политика TIFF

### <a name="read-paths"></a>Пути чтения



| Номер | Путь                | Формат диска |
|-------|---------------------|-------------|
| 1     | /ИФД/{ушорт = 272}   | ascii       |
| 2     | /ИФД/КСМП/Тифф: модель | Юникод     |
| 3     | /ИФД/КСМП/Тифф: модель | Юникод     |



 

### <a name="write-paths"></a>Пути записи



| Номер | Путь                | Формат диска |
|-------|---------------------|-------------|
| 1     | /ИФД/{ушорт = 272}   | ascii       |
| 2     | /ИФД/КСМП/Тифф: модель | Юникод     |
| 3     | /ИФД/КСМП/Тифф: модель | Юникод     |



 

### <a name="remove-paths"></a>Удалить пути



| Номер | Путь                |
|-------|---------------------|
| 1     | /ИФД/{ушорт = 272}   |
| 2     | /ИФД/КСМП/Тифф: модель |
| 3     | /ИФД/КСМП/Тифф: модель |



 

## <a name="remarks"></a>Remarks

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[System. photo. Камерамодел](../properties/props-system-photo-cameramodel.md)
</dt> </dl>

 

 
