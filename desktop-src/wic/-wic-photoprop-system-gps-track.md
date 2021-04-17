---
description: Политика метаданных фотографии для свойства System. GPS. Track.
ms.assetid: ac9e14a0-55f1-437e-9d27-df0fa09671c1
title: Политика метаданных фотографии System. GPS. Track
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 773c65eec8b165c51456f3871309644638c1e2da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703268"
---
# <a name="systemgpstrack-photo-metadata-policy"></a>Политика метаданных фотографии System. GPS. Track

Политика метаданных фотографии для свойства [System. GPS. Track](../properties/props-system-gps-track.md) .

### <a name="pkey"></a>PKEY

Подпрограмма \_ записи GPS "PKEY" \_

### <a name="containers"></a>Контейнеры

JPEG, TIFF

### <a name="read-only"></a>Только для чтения

Да

### <a name="output-propvariant-type"></a>Тип выходного ПРОПВАРИАНТ

VT \_ R8

### <a name="conflict-resolution-policy"></a>Политика разрешения конфликтов

Это значение формируется из System. GPS. Траккнумератор и System. GPS. Траккденоминатор. Он не может быть записан напрямую. Выверяются значения из разных схем.

### <a name="jpeg-policy"></a>Политика JPEG

### <a name="read-paths"></a>Пути чтения



| Заказ | Путь                      | Формат диска |
|-------|---------------------------|-------------|
| 1     | /APP1/IFD/GPS/{ushort = 15} |             |
| 2     | /КСМП/ексиф: Гпстракк        |             |



 

### <a name="write-paths"></a>Пути записи



| Заказ | Путь                      | Формат диска |
|-------|---------------------------|-------------|
| 1     | /APP1/IFD/GPS/{ushort = 15} |             |
| 2     | /КСМП/ексиф: Гпстракк        |             |



 

### <a name="remove-paths"></a>Удалить пути



| Заказ | Путь                      |
|-------|---------------------------|
| 1     | /APP1/IFD/GPS/{ushort = 15} |
| 2     | /КСМП/ексиф: гпстракк        |



 

### <a name="tiff-policies"></a>Политики TIFF

### <a name="read-paths"></a>Пути чтения



| Заказ | Путь                   | Формат диска |
|-------|------------------------|-------------|
| 1     | /ИФД/ГПС/{ушорт = 15}   |             |
| 2     | /ИФД/КСМП/ексиф: Гпстракк |             |



 

### <a name="write-paths"></a>Пути записи



| Заказ | Путь                   | Формат диска |
|-------|------------------------|-------------|
| 1     | /ИФД/ГПС/{ушорт = 15}   |             |
| 2     | /ИФД/КСМП/ексиф: Гпстракк |             |



 

### <a name="remove-paths"></a>Удалить пути



| Заказ | Путь                   |
|-------|------------------------|
| 1     | /ИФД/ГПС/{ушорт = 15}   |
| 2     | /ИФД/КСМП/ексиф: гпстракк |



 

## <a name="remarks"></a>Комментарии

## <a name="related-topics"></a>См. также

<dl> <dt>

[System. GPS. Track](../properties/props-system-gps-track.md)
</dt> </dl>

 

 
