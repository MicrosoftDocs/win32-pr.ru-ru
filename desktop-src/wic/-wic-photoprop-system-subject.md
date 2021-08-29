---
description: Политика метаданных фотографии для свойства System. Subject.
ms.assetid: 5ab7c74b-8a5e-4329-8a49-291470d406cc
title: Политика метаданных фотографии System. subject
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9321e866c34027df3e932f84d532162def959cbaf365bb4020c19647d547adea
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119881974"
---
# <a name="systemsubject-photo-metadata-policy"></a>Политика метаданных фотографии System. subject

Политика метаданных фотографии для свойства [System. subject](../properties/props-system-subject.md) .

### <a name="pkey"></a>PKEY

\_Тема PKEY

### <a name="containers"></a>Контейнеры

JPEG, TIFF

### <a name="read-only"></a>Только для чтения

Нет

### <a name="output-propvariant-type"></a>Тип выходного ПРОПВАРИАНТ

VT \_ LPWSTR

### <a name="input-propvariant-type"></a>Тип входного ПРОПВАРИАНТ

VT \_ LPWSTR или VT \_ LPWSTR

### <a name="conflict-resolution-policy"></a>Политика разрешения конфликтов

Выверяются значения из разных схем.

### <a name="jpeg-policy"></a>Политика JPEG

### <a name="read-paths"></a>Пути чтения



| Номер | Путь                     | Формат диска    |
|-------|--------------------------|----------------|
| 1     | /APP1/IFD/{ushort = 40095} | байт в Юникоде \_ |
| 2     | /APP1/IFD/{ushort = 270}   | ascii          |



 

### <a name="write-paths"></a>Пути записи



| Номер | Путь                     | Формат диска    |
|-------|--------------------------|----------------|
| 1     | /APP1/IFD/{ushort = 40095} | байт в Юникоде \_ |



 

### <a name="remove-paths"></a>Удалить пути



| Номер | Путь                     |
|-------|--------------------------|
| 1     | /APP1/IFD/{ushort = 40095} |
| 2     | /APP1/IFD/{ushort = 270}   |



 

### <a name="tiff-policy"></a>Политика TIFF

### <a name="read-paths"></a>Пути чтения



| Номер | Путь                | Формат диска    |
|-------|---------------------|----------------|
| 1     | /ИФД/{ушорт = 40095} | байт в Юникоде \_ |
| 2     | /ИФД/{ушорт = 270}   | ascii          |



 

### <a name="write-paths"></a>Пути записи



| Номер | Путь                | Формат диска    |
|-------|---------------------|----------------|
| 1     | /ИФД/{ушорт = 40095} | байт в Юникоде \_ |



 

### <a name="remove-paths"></a>Удалить пути



| Номер | Путь                |
|-------|---------------------|
| 1     | /ИФД/{ушорт = 40095} |
| 2     | /ИФД/{ушорт = 270}   |



 

## <a name="remarks"></a>Remarks

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[System. subject](../properties/props-system-subject.md)
</dt> </dl>

 

 
