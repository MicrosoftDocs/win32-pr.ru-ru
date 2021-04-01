---
description: Политика метаданных фотографии для свойства System. GPS. Дестлонгитуде.
ms.assetid: 885a522d-e1bf-43fb-a996-97e725b6cf0c
title: Политика метаданных фотографии System. GPS. Дестлонгитуде
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72e0a4f56e49dfbb3397b96cf7fae35a6065b7aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081310"
---
# <a name="systemgpsdestlongitude-photo-metadata-policy"></a>Политика метаданных фотографии System. GPS. Дестлонгитуде

Политика метаданных фотографии для свойства [System. GPS. дестлонгитуде](../properties/props-system-gps-destlongitude.md) .

### <a name="pkey"></a>PKEY

PKEY \_ GPS \_ дестлонгитуде

### <a name="containers"></a>Контейнеры

JPEG, TIFF

### <a name="read-only"></a>Только для чтения

Да

### <a name="output-propvariant-type"></a>Тип выходного ПРОПВАРИАНТ

VT \_ вектор \| VT \_ R8

### <a name="input-propvariant-type"></a>Тип входного ПРОПВАРИАНТ

VT \_ вектор \| VT \_ R8

### <a name="conflict-resolution-policy"></a>Политика разрешения конфликтов

Это значение формируется из System. GPS. Дестлонгитуденумератор и System. GPS. Дестлонгитудеденоминатор. Он не может быть записан напрямую. Выверяются значения из разных схем.

### <a name="jpeg-policy"></a>Политика JPEG

### <a name="read-paths"></a>Пути чтения



| Заказ | Путь                       | Формат диска |
|-------|----------------------------|-------------|
| 1     | /APP1/IFD/GPS/{ushort = 22}  |             |
| 2     | /КСМП/ексиф: Гпсдестлонгитуде |             |



 

### <a name="write-paths"></a>Пути записи



| Заказ | Путь                       | Формат диска |
|-------|----------------------------|-------------|
| 1     | /APP1/IFD/GPS/{ushort = 22}  |             |
| 2     | /КСМП/ексиф: Гпсдестлонгитуде |             |



 

### <a name="remove-paths"></a>Удалить пути



| Заказ | Путь                       |
|-------|----------------------------|
| 1     | /APP1/IFD/GPS/{ushort = 22}  |
| 2     | /КСМП/ексиф: гпсдестлонгитуде |



 

### <a name="tiff-policies"></a>Политики TIFF

### <a name="read-paths"></a>Пути чтения



| Заказ | Путь                           | Формат диска |
|-------|--------------------------------|-------------|
| 1     | /ИФД/ГПС/{ушорт = 22}           |             |
| 2     | /ИФД/КСМП/ексиф: Гпсдестлонгитуде |             |



 

### <a name="write-paths"></a>Пути записи



| Заказ | Путь                           | Формат диска |
|-------|--------------------------------|-------------|
| 1     | /ИФД/ГПС/{ушорт = 22}           |             |
| 2     | /ИФД/КСМП/ексиф: Гпсдестлонгитуде |             |



 

### <a name="remove-paths"></a>Удалить пути



| Заказ | Путь                           |
|-------|--------------------------------|
| 1     | /ИФД/ГПС/{ушорт = 22}           |
| 2     | /ИФД/КСМП/ексиф: гпсдестлонгитуде |



 

## <a name="remarks"></a>Комментарии

## <a name="related-topics"></a>См. также

<dl> <dt>

[System. GPS. Дестлонгитуде](../properties/props-system-gps-destlongitude.md)
</dt> </dl>

 

 
