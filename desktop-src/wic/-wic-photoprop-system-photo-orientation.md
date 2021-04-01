---
description: Политика метаданных фотографии для свойства System. photo. Orientation.
ms.assetid: 27e6d4f5-39d5-4cb4-88bc-b0d61ccaa2f3
title: Политика метаданных фотографии System. photo. Orientation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a28f4f350cd1a4c24d71ec737b4679aea2f7cab5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081305"
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



| Заказ | Путь                   | Формат диска |
|-------|------------------------|-------------|
| 1     | /APP1/IFD/{ushort = 274} | ushort      |
| 2     | /КСМП/Тифф: ориентация  | Юникод     |



 

### <a name="write-paths"></a>Пути записи



| Заказ | Путь                   | Формат диска |
|-------|------------------------|-------------|
| 1     | /APP1/IFD/{ushort = 274} | ushort      |
| 2     | /КСМП/Тифф: ориентация  | Юникод     |



 

### <a name="remove-paths"></a>Удалить пути



| Заказ | Путь                   |
|-------|------------------------|
| 1     | /APP1/IFD/{ushort = 274} |
| 2     | /КСМП/Тифф: ориентация  |



 

### <a name="tiff-policies"></a>Политики TIFF

### <a name="read-paths"></a>Пути чтения



| Заказ | Путь                      | Формат диска |
|-------|---------------------------|-------------|
| 1     | /ИФД/{ушорт = 274}         | ushort      |
| 2     | /ИФД/КСМП/Тифф: ориентация | Юникод     |



 

### <a name="write-paths"></a>Пути записи



| Заказ | Путь                      | Формат диска |
|-------|---------------------------|-------------|
| 1     | /ИФД/{ушорт = 274}         | ushort      |
| 2     | /ИФД/КСМП/Тифф: ориентация | Юникод     |



 

### <a name="remove-paths"></a>Удалить пути



| Заказ | Путь                      |
|-------|---------------------------|
| 1     | /ИФД/{ушорт = 274}         |
| 2     | /ИФД/КСМП/Тифф: ориентация |



 

## <a name="remarks"></a>Комментарии

## <a name="related-topics"></a>См. также

<dl> <dt>

[System. фото. Orientation](../properties/props-system-photo-meteringmode.md)
</dt> </dl>

 

 
