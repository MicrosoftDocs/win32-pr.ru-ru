---
description: Политика метаданных фотографии для свойства System. GPS. Меасуремоде.
ms.assetid: 911a0d81-bd12-4155-b45a-ae1a18f2dd07
title: Политика метаданных фотографии System. GPS. Меасуремоде
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 827cd278a71b23934fb0475e78d98b25a9f2b72d413b70f9abc60ba3dbe2c3fd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119882324"
---
# <a name="systemgpsmeasuremode-photo-metadata-policy"></a>Политика метаданных фотографии System. GPS. Меасуремоде

Политика метаданных фотографии для свойства [System. GPS. меасуремоде](../properties/props-system-gps-measuremode.md) .

### <a name="pkey"></a>PKEY

PKEY \_ GPS \_ меасуремоде

### <a name="containers"></a>Контейнеры

JPEG, TIFF

### <a name="read-only"></a>Только для чтения

Нет

### <a name="output-propvariant-type"></a>Тип выходного ПРОПВАРИАНТ

VT \_ LPWSTR

### <a name="input-propvariant-type"></a>Тип входного ПРОПВАРИАНТ

VT \_ LPWSTR является предпочтительным, но \_ также принимается VT LPSTR.

### <a name="conflict-resolution-policy"></a>Политика разрешения конфликтов

Выверяются значения из разных схем.

### <a name="jpeg-policies"></a>Политики JPEG

### <a name="read-paths"></a>Пути чтения



| Номер | Путь                      | Формат диска |
|-------|---------------------------|-------------|
| 1     | /APP1/IFD/GPS/{ushort = 10} | ascii       |
| 2     | /КСМП/ексиф: Гпсмеасуремоде  | Юникод     |



 

### <a name="write-paths"></a>Пути записи



| Номер | Путь                      | Формат диска |
|-------|---------------------------|-------------|
| 1     | /APP1/IFD/GPS/{ushort = 10} | ascii       |
| 2     | /КСМП/ексиф: Гпсмеасуремоде  | Юникод     |



 

### <a name="remove-paths"></a>Удалить пути



| Номер | Путь                      |
|-------|---------------------------|
| 1     | /APP1/IFD/GPS/{ushort = 10} |
| 2     | /КСМП/ексиф: гпсмеасуремоде  |



 

### <a name="tiff-policies"></a>Политики TIFF

### <a name="read-paths"></a>Пути чтения



| Номер | Путь                         | Формат диска |
|-------|------------------------------|-------------|
| 1     | /ИФД/ГПС/{ушорт = 10}         | ascii       |
| 2     | /ИФД/КСМП/ексиф: Гпсмеасуремоде | Юникод     |



 

### <a name="write-paths"></a>Пути записи



| Номер | Путь                         | Формат диска |
|-------|------------------------------|-------------|
| 1     | /ИФД/ГПС/{ушорт = 10}         | ascii       |
| 2     | /ИФД/КСМП/ексиф: Гпсмеасуремоде | Юникод     |



 

### <a name="remove-paths"></a>Удалить пути



| Номер | Путь                         |
|-------|------------------------------|
| 1     | /ИФД/ГПС/{ушорт = 10}         |
| 2     | /ИФД/КСМП/ексиф: гпсмеасуремоде |



 

## <a name="remarks"></a>Remarks

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[System. GPS. Меасуремоде](../properties/props-system-gps-measuremode.md)
</dt> </dl>

 

 
