---
description: Политика метаданных фотографии для свойства System. GPS. Имгдиректионреф.
ms.assetid: 74ae0989-6d53-4d72-abe9-84f40c0c884a
title: Политика метаданных фотографии System. GPS. Имгдиректионреф
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e735f91133d4ec473537f063e30d2d48f801a99f8f6bc80fa228b98a9bd95437
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117667901"
---
# <a name="systemgpsimgdirectionref-photo-metadata-policy"></a>Политика метаданных фотографии System. GPS. Имгдиректионреф

Политика метаданных фотографии для свойства [System. GPS. имгдиректионреф](../properties/props-system-gps-imgdirectionref.md) .

### <a name="pkey"></a>PKEY

PKEY \_ , GPS. имгдиректионреф

### <a name="containers"></a>Контейнеры

JPEG, TIFF

### <a name="read-only"></a>Только для чтения

Нет

### <a name="output-propvariant-type"></a>Тип выходного ПРОПВАРИАНТ

VT \_ LPWSTR

### <a name="input-type"></a>Тип входных данных

VT \_ LPWSTR является предпочтительным, но \_ также принимается VT LPSTR.

### <a name="conflict-resolution-policy"></a>Политика разрешения конфликтов

Выверяются значения из разных схем.

### <a name="jpeg-policies"></a>Политики JPEG

### <a name="read-paths"></a>Пути чтения



| Номер | Путь                         | Формат диска |
|-------|------------------------------|-------------|
| 1     | /APP1/IFD/GPS/{ushort = 16}    | ascii       |
| 2     | /КСМП/ексиф: Гпсимгдиректионреф | Юникод     |



 

### <a name="write-paths"></a>Пути записи



| Номер | Путь                         | Формат диска |
|-------|------------------------------|-------------|
| 1     | /APP1/IFD/GPS/{ushort = 16}    | ascii       |
| 2     | /КСМП/ексиф: Гпсимгдиректионреф | Юникод     |



 

### <a name="remove-paths"></a>Удалить пути



| Номер | Путь                         |
|-------|------------------------------|
| 1     | /APP1/IFD/GPS/{ushort = 16}    |
| 2     | /КСМП/ексиф: гпсимгдиректионреф |



 

### <a name="tiff-policies"></a>Политики TIFF

### <a name="read-paths"></a>Пути чтения



| Номер | Путь                             | Формат диска |
|-------|----------------------------------|-------------|
| 1     | /ИФД/ГПС/{ушорт = 16}             | ascii       |
| 2     | /ИФД/КСМП/ексиф: Гпсимгдиректионреф | Юникод     |



 

### <a name="write-paths"></a>Пути записи



| Номер | Путь                             | Формат диска |
|-------|----------------------------------|-------------|
| 1     | /ИФД/ГПС/{ушорт = 16}             | ascii       |
| 2     | /ИФД/КСМП/ексиф: Гпсимгдиректионреф | Юникод     |



 

### <a name="remove-paths"></a>Удалить пути



| Номер | Путь                             |
|-------|----------------------------------|
| 1     | /ИФД/ГПС/{ушорт = 16}             |
| 2     | /ИФД/КСМП/ексиф: гпсимгдиректионреф |



 

## <a name="remarks"></a>Remarks

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[System. GPS. Имгдиректионреф](../properties/props-system-gps-imgdirectionref.md)
</dt> </dl>

 

 
