---
description: Политика метаданных фотографии для свойства System. GPS. Track.
ms.assetid: ac9e14a0-55f1-437e-9d27-df0fa09671c1
title: Политика метаданных фотографии System. GPS. Track
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c89aee05d0c55e78fe4e55d7eacd8a8d0992fcb8d9f56312164c652cbc0bd81c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118205535"
---
# <a name="systemgpstrack-photo-metadata-policy"></a>Политика метаданных фотографии System. GPS. Track

Политика метаданных фотографии для свойства [System. GPS. Track](../properties/props-system-gps-track.md) .

### <a name="pkey"></a>PKEY

Подпрограмма \_ записи GPS "PKEY" \_

### <a name="containers"></a>Контейнеры

JPEG, TIFF

### <a name="read-only"></a>Только для чтения

Да

### <a name="output-propvariant-type"></a>Тип выходного ПРОПВАРИАНТ

VT \_ R8

### <a name="conflict-resolution-policy"></a>Политика разрешения конфликтов

Это значение формируется из System. GPS. Траккнумератор и System. GPS. Траккденоминатор. Он не может быть записан напрямую. Выверяются значения из разных схем.

### <a name="jpeg-policy"></a>Политика JPEG

### <a name="read-paths"></a>Пути чтения



| Номер | Путь                      | Формат диска |
|-------|---------------------------|-------------|
| 1     | /APP1/IFD/GPS/{ushort = 15} |             |
| 2     | /КСМП/ексиф: Гпстракк        |             |



 

### <a name="write-paths"></a>Пути записи



| Номер | Путь                      | Формат диска |
|-------|---------------------------|-------------|
| 1     | /APP1/IFD/GPS/{ushort = 15} |             |
| 2     | /КСМП/ексиф: Гпстракк        |             |



 

### <a name="remove-paths"></a>Удалить пути



| Номер | Путь                      |
|-------|---------------------------|
| 1     | /APP1/IFD/GPS/{ushort = 15} |
| 2     | /КСМП/ексиф: гпстракк        |



 

### <a name="tiff-policies"></a>Политики TIFF

### <a name="read-paths"></a>Пути чтения



| Номер | Путь                   | Формат диска |
|-------|------------------------|-------------|
| 1     | /ИФД/ГПС/{ушорт = 15}   |             |
| 2     | /ИФД/КСМП/ексиф: Гпстракк |             |



 

### <a name="write-paths"></a>Пути записи



| Номер | Путь                   | Формат диска |
|-------|------------------------|-------------|
| 1     | /ИФД/ГПС/{ушорт = 15}   |             |
| 2     | /ИФД/КСМП/ексиф: Гпстракк |             |



 

### <a name="remove-paths"></a>Удалить пути



| Номер | Путь                   |
|-------|------------------------|
| 1     | /ИФД/ГПС/{ушорт = 15}   |
| 2     | /ИФД/КСМП/ексиф: гпстракк |



 

## <a name="remarks"></a>Remarks

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[System. GPS. Track](../properties/props-system-gps-track.md)
</dt> </dl>

 

 
