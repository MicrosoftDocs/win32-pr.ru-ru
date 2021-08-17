---
description: Политика метаданных фотографии для свойства System. photo. Orientation.
ms.assetid: 27e6d4f5-39d5-4cb4-88bc-b0d61ccaa2f3
title: Политика метаданных фотографии System. photo. Orientation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87f9496942e6be971e0e047596125669fc9112cf82bce6eb02ec7e1cdbddc4de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119087070"
---
# <a name="systemphotoorientation-photo-metadata-policy"></a>Политика метаданных фотографии System. photo. Orientation

Политика метаданных фотографии для свойства [System. photo. Orientation](../properties/props-system-photo-meteringmode.md) .

### <a name="pkey"></a>PKEY

\_Ориентация фотографии \_ PKEY

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



| Номер | Путь                   | Формат диска |
|-------|------------------------|-------------|
| 1     | /APP1/IFD/{ushort = 274} | ushort      |
| 2     | /КСМП/Тифф: ориентация  | Юникод     |



 

### <a name="write-paths"></a>Пути записи



| Номер | Путь                   | Формат диска |
|-------|------------------------|-------------|
| 1     | /APP1/IFD/{ushort = 274} | ushort      |
| 2     | /КСМП/Тифф: ориентация  | Юникод     |



 

### <a name="remove-paths"></a>Удалить пути



| Номер | Путь                   |
|-------|------------------------|
| 1     | /APP1/IFD/{ushort = 274} |
| 2     | /КСМП/Тифф: ориентация  |



 

### <a name="tiff-policies"></a>Политики TIFF

### <a name="read-paths"></a>Пути чтения



| Номер | Путь                      | Формат диска |
|-------|---------------------------|-------------|
| 1     | /ИФД/{ушорт = 274}         | ushort      |
| 2     | /ИФД/КСМП/Тифф: ориентация | Юникод     |



 

### <a name="write-paths"></a>Пути записи



| Номер | Путь                      | Формат диска |
|-------|---------------------------|-------------|
| 1     | /ИФД/{ушорт = 274}         | ushort      |
| 2     | /ИФД/КСМП/Тифф: ориентация | Юникод     |



 

### <a name="remove-paths"></a>Удалить пути



| Номер | Путь                      |
|-------|---------------------------|
| 1     | /ИФД/{ушорт = 274}         |
| 2     | /ИФД/КСМП/Тифф: ориентация |



 

## <a name="remarks"></a>Remarks

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[System. фото. Orientation](../properties/props-system-photo-meteringmode.md)
</dt> </dl>

 

 
