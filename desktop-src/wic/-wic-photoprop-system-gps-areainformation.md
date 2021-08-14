---
description: Политика метаданных фотографии для свойства System. GPS. Ареаинформатион.
ms.assetid: d9ecb00b-1f97-4f53-909f-30231104d398
title: Политика метаданных фотографии System. GPS. Ареаинформатион
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4eee2cf4234902049241c833d1077814f5daf88187323c43bc1cb00f6f44aa6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118205525"
---
# <a name="systemgpsareainformation-photo-metadata-policy"></a>Политика метаданных фотографии System. GPS. Ареаинформатион

Политика метаданных фотографии для свойства [System. GPS. ареаинформатион](../properties/props-system-gps-areainformation.md) .

### <a name="pkey"></a>PKEY

PKEY \_ GPS \_ ареаинформатион

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

### <a name="jpeg-policies"></a>Политики JPEG

### <a name="read-paths"></a>Пути чтения



| Номер | Путь                         | Формат диска |
|-------|------------------------------|-------------|
| 1     | /APP1/IFD/GPS/{ushort = 28}    |             |
| 2     | /КСМП/ексиф: Гпсареаинформатион | Юникод     |



 

### <a name="write-paths"></a>Пути записи



| Номер | Путь                         | Формат диска |
|-------|------------------------------|-------------|
| 1     | /APP1/IFD/GPS/{ushort = 28}    |             |
| 2     | /КСМП/ексиф: Гпсареаинформатион | Юникод     |



 

### <a name="remove-paths"></a>Удалить пути



| Номер | Путь                         |
|-------|------------------------------|
| 1     | /APP1/IFD/GPS/{ushort = 28}    |
| 2     | /КСМП/ексиф: Гпсареаинформатион |



 

### <a name="tiff-policies"></a>Политики TIFF

### <a name="read-paths"></a>Пути чтения



| Номер | Путь                             | Формат диска |
|-------|----------------------------------|-------------|
| 1     | /ИФД/ГПС/{ушорт = 28}             |             |
| 2     | /ИФД/КСМП/ексиф: Гпсареаинформатион | Юникод     |



 

### <a name="write-paths"></a>Пути записи



| Номер | Путь                             | Формат диска |
|-------|----------------------------------|-------------|
| 1     | /ИФД/ГПС/{ушорт = 28}             |             |
| 2     | /ИФД/КСМП/ексиф: Гпсареаинформатион | Юникод     |



 

### <a name="remove-paths"></a>Удалить пути



| Номер | Путь                             |
|-------|----------------------------------|
| 1     | /ИФД/ГПС/{ушорт = 28}             |
| 2     | /ИФД/КСМП/ексиф: Гпсареаинформатион |



 

## <a name="remarks"></a>Remarks

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[System. GPS. Ареаинформатион](../properties/props-system-gps-areainformation.md)
</dt> </dl>

 

 
