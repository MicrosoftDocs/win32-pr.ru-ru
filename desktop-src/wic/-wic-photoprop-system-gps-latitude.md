---
description: Политика метаданных фотографии для свойства System. GPS. Широта.
ms.assetid: 0f8cea07-da96-4d2a-8444-6073b51e1236
title: Политика метаданных фотографии System. GPS. Широта
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5320869c1e8fd0d4b17bb17da455fc939bf44b9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702786"
---
# <a name="systemgpslatitude-photo-metadata-policy"></a>Политика метаданных фотографии System. GPS. Широта

Политика метаданных фотографии для свойства [System. GPS. Широта](../properties/props-system-gps-latitude.md) .

### <a name="pkey"></a>PKEY

PKEY \_ GPS, \_ Широта

### <a name="containers"></a>Контейнеры

JPEG, TIFF

### <a name="read-only"></a>Только для чтения

Да

### <a name="output-propvariant-type"></a>Тип выходного ПРОПВАРИАНТ

VT \_ вектор \| VT \_ R8

### <a name="conflict-resolution-policy"></a>Политика разрешения конфликтов

Это значение можно записать с помощью записи в System. GPS. Латитуденумератор и System. GPS. Латитудеденоминатор. Он не может быть записан напрямую. Выверяются значения из разных схем.

### <a name="jpeg-policy"></a>Политика JPEG

### <a name="read-paths"></a>Пути чтения



| Заказ | Путь                     | Формат диска |
|-------|--------------------------|-------------|
| 1     | /APP1/IFD/GPS/{ushort = 2} |             |
| 2     | /КСМП/ексиф: Гпслатитуде    |             |



 

### <a name="write-paths"></a>Пути записи



| Заказ | Путь                     | Формат диска |
|-------|--------------------------|-------------|
| 1     | /APP1/IFD/GPS/{ushort = 2} |             |
| 2     | /КСМП/ексиф: Гпслатитуде    |             |



 

### <a name="remove-paths"></a>Удалить пути



| Заказ | Путь                     |
|-------|--------------------------|
| 1     | /APP1/IFD/GPS/{ushort = 2} |
| 2     | /КСМП/ексиф: гпслатитуде    |



 

### <a name="tiff-policies"></a>Политики TIFF

### <a name="read-paths"></a>Пути чтения



| Заказ | Путь                      | Формат диска |
|-------|---------------------------|-------------|
| 1     | /ИФД/ГПС/{ушорт = 2}       |             |
| 2     | /ИФД/КСМП/ексиф: Гпслатитуде |             |



 

### <a name="write-paths"></a>Пути записи



| Заказ | Путь                      | Формат диска |
|-------|---------------------------|-------------|
| 1     | /ИФД/ГПС/{ушорт = 2}       |             |
| 2     | /ИФД/КСМП/ексиф: Гпслатитуде |             |



 

### <a name="remove-paths"></a>Удалить пути



| Заказ | Путь                      |
|-------|---------------------------|
| 1     | /ИФД/ГПС/{ушорт = 2}       |
| 2     | /ИФД/КСМП/ексиф: гпслатитуде |



 

## <a name="remarks"></a>Комментарии

## <a name="related-topics"></a>См. также

<dl> <dt>

[System. GPS. Широта](../properties/props-system-gps-latitude.md)
</dt> </dl>

 

 
