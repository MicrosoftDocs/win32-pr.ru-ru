---
description: Политика метаданных фотографии для свойства System. GPS. Спидреф.
ms.assetid: 45fea6be-1e63-4244-a93d-d446e315ddd4
title: Политика метаданных фотографии System. GPS. Спидреф
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c7b60a0c8decaf5ecc30f9017a0aadc61bb9fe4814240fb7ab2e022d6a2873f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119549494"
---
# <a name="systemgpsspeedref-photo-metadata-policy"></a>Политика метаданных фотографии System. GPS. Спидреф

Политика метаданных фотографии для свойства [System. GPS. спидреф](../properties/props-system-gps-speedref.md) .

### <a name="pkey"></a>PKEY

PKEY \_ GPS \_ спидреф

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
| 1     | /APP1/IFD/GPS/{ushort = 12} | ascii       |
| 2     | /КСМП/ексиф: Гпсспидреф     | Юникод     |



 

### <a name="write-paths"></a>Пути записи



| Номер | Путь                      | Формат диска |
|-------|---------------------------|-------------|
| 1     | /APP1/IFD/GPS/{ushort = 12} | ascii       |
| 2     | /КСМП/ексиф: Гпсспидреф     | Юникод     |



 

### <a name="remove-paths"></a>Удалить пути



| Номер | Путь                      | Формат диска |
|-------|---------------------------|-------------|
| 1     | /APP1/IFD/GPS/{ushort = 12} |             |
| 2     | /КСМП/ексиф: гпсспидреф     |             |



 

### <a name="tiff-policies"></a>Политики TIFF

### <a name="read-paths"></a>Пути чтения



| Номер | Путь                      |         |
|-------|---------------------------|---------|
| 1     | /ИФД/ГПС/{ушорт = 12}      | ascii   |
| 2     | /ИФД/КСМП/ексиф: Гпсспидреф | Юникод |



 

### <a name="write-paths"></a>Пути записи



| Номер | Путь                      | Формат диска |
|-------|---------------------------|-------------|
| 1     | /ИФД/ГПС/{ушорт = 12}      | ascii       |
| 2     | /ИФД/КСМП/ексиф: Гпсспидреф | Юникод     |



 

### <a name="remove-paths"></a>Удалить пути



| Номер | Путь                      |
|-------|---------------------------|
| 1     | /ИФД/ГПС/{ушорт = 12}      |
| 2     | /ИФД/КСМП/ексиф: гпсспидреф |



 

## <a name="remarks"></a>Remarks

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[System. GPS. Спидреф](../properties/props-system-gps-speedref.md)
</dt> </dl>

 

 
