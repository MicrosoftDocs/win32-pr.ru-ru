---
description: Политика метаданных фотографии для свойства System. GPS. DIFFERENTIAL.
ms.assetid: 330d1f88-5f54-4e29-b57f-eb7112203e04
title: Политика метаданных фотографии System. GPS. Differential
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 728df47fd8e6e9748b7208b79444ba8fa257fa49c92587df199441de941f4fdd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119931804"
---
# <a name="systemgpsdifferential-photo-metadata-policy"></a>Политика метаданных фотографии System. GPS. Differential

Политика метаданных фотографии для свойства [System. GPS. Differential](../properties/props-system-gps-differential.md) .

### <a name="pkey"></a>PKEY

\_Разностная копия GPS "PKEY" \_

### <a name="containers"></a>Контейнеры

JPEG, TIFF

### <a name="read-only"></a>Только для чтения

Нет

### <a name="output-propvariant-type"></a>Тип выходного ПРОПВАРИАНТ

VT \_ UI2

### <a name="input-propvariant-type"></a>Тип входного ПРОПВАРИАНТ

\_Все они принимают VT UI1, VT \_ UI2 и VT \_ UI4.

### <a name="conflict-resolution-policy"></a>Политика разрешения конфликтов

Выверяются значения из разных схем.

### <a name="jpeg-policies"></a>Политики JPEG

### <a name="read-paths"></a>Пути чтения



| Номер | Путь                      | Формат диска |
|-------|---------------------------|-------------|
| 1     | /APP1/IFD/GPS/{ushort = 30} | ushort      |
| 2     | /КСМП/ексиф: Гпсдифферентиал | Юникод     |



 

### <a name="write-paths"></a>Пути записи



| Номер | Путь                      | Формат диска |
|-------|---------------------------|-------------|
| 1     | /APP1/IFD/GPS/{ushort = 30} | ushort      |
| 2     | /КСМП/ексиф: Гпсдифферентиал | Юникод     |



 

### <a name="remove-paths"></a>Удалить пути



| Номер | Путь                      |
|-------|---------------------------|
| 1     | /APP1/IFD/GPS/{ushort = 30} |
| 2     | /КСМП/ексиф: гпсдифферентиал |



 

### <a name="tiff-policies"></a>Политики TIFF

### <a name="read-paths"></a>Пути чтения



| Номер | Путь                          | Формат диска |
|-------|-------------------------------|-------------|
| 1     | /ИФД/ГПС/{ушорт = 30}          | ushort      |
| 2     | /ИФД/КСМП/ексиф: Гпсдифферентиал | Юникод     |



 

### <a name="write-paths"></a>Пути записи



| Номер | Путь                          | Формат диска |
|-------|-------------------------------|-------------|
| 1     | /ИФД/ГПС/{ушорт = 30}          | ushort      |
| 2     | /ИФД/КСМП/ексиф: Гпсдифферентиал | Юникод     |



 

### <a name="remove-paths"></a>Удалить пути



| Номер | Путь                          |
|-------|-------------------------------|
| 1     | /ИФД/ГПС/{ушорт = 30}          |
| 2     | /ИФД/КСМП/ексиф: гпсдифферентиал |



 

## <a name="remarks"></a>Remarks

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[System. GPS. Differential](../properties/props-system-gps-differential.md)
</dt> </dl>

 

 
