---
description: Политика метаданных фотографии для свойства System. GPS. status.
ms.assetid: 74ea0384-3b1f-4d5e-8713-7b3936813a3a
title: Политика метаданных фотографии System. GPS. status
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a99237b9fe14d9adbc97dd5de95158a8aa714caaa4a0a8440d9f3798a2155d20
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118710519"
---
# <a name="systemgpsstatus-photo-metadata-policy"></a>Политика метаданных фотографии System. GPS. status

Политика метаданных фотографии для свойства [System. GPS. status](../properties/props-system-gps-status.md) .

### <a name="pkey"></a>PKEY

\_Состояние состояния GPS "PKEY" \_

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



| Номер | Путь                     | Формат диска |
|-------|--------------------------|-------------|
| 1     | /APP1/IFD/GPS/{ushort = 9} | ascii       |
| 2     | /КСМП/ексиф: Гпсстатус      | Юникод     |



 

### <a name="write-paths"></a>Пути записи



| Номер | Путь                     | Формат диска |
|-------|--------------------------|-------------|
| 1     | /APP1/IFD/GPS/{ushort = 9} | ascii       |
| 2     | /КСМП/ексиф: Гпсстатус      | Юникод     |



 

### <a name="remove-paths"></a>Удалить пути



| Номер | Путь                     |
|-------|--------------------------|
| 1     | /APP1/IFD/GPS/{ushort = 9} |
| 2     | /КСМП/ексиф: гпсстатус      |



 

### <a name="tiff-policies"></a>Политики TIFF

### <a name="read-paths"></a>Пути чтения



| Номер | Путь                    | Формат диска |
|-------|-------------------------|-------------|
| 1     | /ИФД/ГПС/{ушорт = 9}     | ascii       |
| 2     | /ИФД/КСМП/ексиф: Гпсстатус | Юникод     |



 

### <a name="write-paths"></a>Пути записи



| Номер | Путь                    | Формат диска |
|-------|-------------------------|-------------|
| 1     | /ИФД/ГПС/{ушорт = 9}     | ascii       |
| 2     | /ИФД/КСМП/ексиф: Гпсстатус | Юникод     |



 

### <a name="remove-paths"></a>Удалить пути



| Номер | Путь                    |
|-------|-------------------------|
| 1     | /ИФД/ГПС/{ушорт = 9}     |
| 2     | /ИФД/КСМП/ексиф: гпсстатус |



 

## <a name="remarks"></a>Remarks

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[System. GPS. status](../properties/props-system-gps-status.md)
</dt> </dl>

 

 
