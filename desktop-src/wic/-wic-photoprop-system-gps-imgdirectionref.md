---
description: Политика метаданных фотографии для свойства System. GPS. Имгдиректионреф.
ms.assetid: 74ae0989-6d53-4d72-abe9-84f40c0c884a
title: Политика метаданных фотографии System. GPS. Имгдиректионреф
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80276ca8d1981935004dbec49fef588fcde330ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272295"
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



| Заказ | Путь                         | Формат диска |
|-------|------------------------------|-------------|
| 1     | /APP1/IFD/GPS/{ushort = 16}    | ascii       |
| 2     | /КСМП/ексиф: Гпсимгдиректионреф | Юникод     |



 

### <a name="write-paths"></a>Пути записи



| Заказ | Путь                         | Формат диска |
|-------|------------------------------|-------------|
| 1     | /APP1/IFD/GPS/{ushort = 16}    | ascii       |
| 2     | /КСМП/ексиф: Гпсимгдиректионреф | Юникод     |



 

### <a name="remove-paths"></a>Удалить пути



| Заказ | Путь                         |
|-------|------------------------------|
| 1     | /APP1/IFD/GPS/{ushort = 16}    |
| 2     | /КСМП/ексиф: гпсимгдиректионреф |



 

### <a name="tiff-policies"></a>Политики TIFF

### <a name="read-paths"></a>Пути чтения



| Заказ | Путь                             | Формат диска |
|-------|----------------------------------|-------------|
| 1     | /ИФД/ГПС/{ушорт = 16}             | ascii       |
| 2     | /ИФД/КСМП/ексиф: Гпсимгдиректионреф | Юникод     |



 

### <a name="write-paths"></a>Пути записи



| Заказ | Путь                             | Формат диска |
|-------|----------------------------------|-------------|
| 1     | /ИФД/ГПС/{ушорт = 16}             | ascii       |
| 2     | /ИФД/КСМП/ексиф: Гпсимгдиректионреф | Юникод     |



 

### <a name="remove-paths"></a>Удалить пути



| Заказ | Путь                             |
|-------|----------------------------------|
| 1     | /ИФД/ГПС/{ушорт = 16}             |
| 2     | /ИФД/КСМП/ексиф: гпсимгдиректионреф |



 

## <a name="remarks"></a>Комментарии

## <a name="related-topics"></a>См. также

<dl> <dt>

[System. GPS. Имгдиректионреф](../properties/props-system-gps-imgdirectionref.md)
</dt> </dl>

 

 
