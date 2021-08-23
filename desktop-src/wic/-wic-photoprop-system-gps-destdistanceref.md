---
description: Политика метаданных фотографии для свойства System. GPS. Дестдистанцереф.
ms.assetid: eb671f34-7366-4182-b72e-0dd7830751e0
title: Политика метаданных фотографии System. GPS. Дестдистанцереф
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0d7973a3be36f9a7624ed8679f364c898d69b622de067bdd2595f3b919a964f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118964983"
---
# <a name="systemgpsdestdistanceref-photo-metadata-policy"></a>Политика метаданных фотографии System. GPS. Дестдистанцереф

Политика метаданных фотографии для свойства [System. GPS. дестдистанцереф](../properties/props-system-gps-destdistanceref.md) .

### <a name="pkey"></a>PKEY

PKEY \_ дестдистанцереф

### <a name="containers"></a>Контейнеры

JPEG, TIFF

### <a name="read-only"></a>Только для чтения

Нет

### <a name="output-propvariant-type"></a>Тип выходного ПРОПВАРИАНТ

VT \_ LPWSTR

### <a name="input-type"></a>Тип входных данных

\_Принимаются VT LPWSTR или VT \_ LPSTR.

### <a name="conflict-resolution-policy"></a>Политика разрешения конфликтов

Выверяются значения из разных схем.

### <a name="jpeg-policies"></a>Политики JPEG

### <a name="read-paths"></a>Пути чтения



| Номер | Путь                         | Формат диска |
|-------|------------------------------|-------------|
| 1     | /APP1/IFD/GPS/{ushort = 25}    | ascii       |
| 2     | /КСМП/ексиф: Гпсдестдистанцереф | Юникод     |



 

### <a name="write-paths"></a>Пути записи



| Номер | Путь                         | Формат диска |
|-------|------------------------------|-------------|
| 1     | /APP1/IFD/GPS/{ushort = 25}    | ascii       |
| 2     | /КСМП/ексиф: Гпсдестдистанцереф | Юникод     |



 

### <a name="remove-paths"></a>Удалить пути



| Номер | Путь                         |
|-------|------------------------------|
| 1     | /APP1/IFD/GPS/{ushort = 25}    |
| 2     | /КСМП/ексиф: гпсдестдистанцереф |



 

### <a name="tiff-policies"></a>Политики TIFF

### <a name="read-paths"></a>Пути чтения



| Номер | Путь                             | Формат диска |
|-------|----------------------------------|-------------|
| 1     | /ИФД/ГПС/{ушорт = 25}             | ascii       |
| 2     | /ИФД/КСМП/ексиф: Гпсдестдистанцереф | Юникод     |



 

### <a name="write-paths"></a>Пути записи



| Номер | Путь                             | Формат диска |
|-------|----------------------------------|-------------|
| 1     | /ИФД/ГПС/{ушорт = 25}             | ascii       |
| 2     | /ИФД/КСМП/ексиф: Гпсдестдистанцереф | Юникод     |



 

### <a name="remove-paths"></a>Удалить пути



| Номер | Путь                             |
|-------|----------------------------------|
| 1     | /ИФД/ГПС/{ушорт = 25}             |
| 2     | /ИФД/КСМП/ексиф: гпсдестдистанцереф |



 

## <a name="remarks"></a>Remarks

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[System. GPS. Дестдистанцереф](../properties/props-system-gps-destdistanceref.md)
</dt> </dl>

 

 
