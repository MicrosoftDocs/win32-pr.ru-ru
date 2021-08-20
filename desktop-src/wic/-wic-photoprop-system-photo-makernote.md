---
description: Политика метаданных фотографии для свойства System. photo. Макерноте.
ms.assetid: e1018bc6-3fd2-4212-afee-6811bfe99f14
title: Политика метаданных фото для System. photo. Макерноте
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 368c6e6cc89f5e1353d460b003b718c768f11896547e36b86807edeb6099aef5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118032561"
---
# <a name="systemphotomakernote-photo-metadata-policy"></a>Политика метаданных фото для System. photo. Макерноте

Политика метаданных фотографии для свойства [System. photo. макерноте](../properties/props-system-photo-makernote.md) .

### <a name="pkey"></a>PKEY

\_Макерноте фото на PKEY \_

### <a name="containers"></a>Контейнеры

JPEG, TIFF

### <a name="read-only"></a>Только для чтения

Нет

### <a name="output-propvariant-type"></a>Тип выходного ПРОПВАРИАНТ

\_Векторный \| VTUI1 VT

### <a name="input-type"></a>Тип входных данных

Буфер

### <a name="conflict-resolution-policy"></a>Политика разрешения конфликтов

Выверяются значения из разных схем.

### <a name="jpeg-policy"></a>Политика JPEG

### <a name="read-paths"></a>Пути чтения



| Номер | Путь                          | Формат диска |
|-------|-------------------------------|-------------|
| 1     | /APP1/IFD/EXIF/{ushort = 37500} |             |



 

### <a name="write-paths"></a>Пути записи



| Номер | Путь                          | Формат диска |
|-------|-------------------------------|-------------|
| 1     | /APP1/IFD/EXIF/{ushort = 37500} |             |



 

### <a name="remove-paths"></a>Удалить пути



| Номер | Путь                          |
|-------|-------------------------------|
| 1     | /APP1/IFD/EXIF/{ushort = 37500} |



 

### <a name="tiff-policies"></a>Политики TIFF

### <a name="read-paths"></a>Пути чтения



| Номер | Путь                     | Формат диска |
|-------|--------------------------|-------------|
| 1     | /ИФД/ексиф/{ушорт = 37500} |             |



 

### <a name="write-paths"></a>Пути записи



| Номер | Путь                     | Формат диска |
|-------|--------------------------|-------------|
| 1     | /ИФД/ексиф/{ушорт = 37500} |             |



 

### <a name="remove-paths"></a>Удалить пути



| Номер | Путь                     |
|-------|--------------------------|
| 1     | /ИФД/ексиф/{ушорт = 37500} |



 

## <a name="remarks"></a>Remarks

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[System. photo. Макерноте](../properties/props-system-photo-makernote.md)
</dt> </dl>

 

 
