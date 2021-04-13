---
description: Политика метаданных фотографии для свойства System. GPS. Дестбеаринг.
ms.assetid: ccc31b3d-27fd-4a8c-a304-852cf6114ec5
title: Политика метаданных фотографии System. GPS. Дестбеаринг
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01a084a0633579afe646403fb4dcad0ca8a1b9ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348585"
---
# <a name="systemgpsdestbearing-photo-metadata-policy"></a>Политика метаданных фотографии System. GPS. Дестбеаринг

Политика метаданных фотографии для свойства [System. GPS. дестбеаринг](../properties/props-system-gps-destbearing.md) .

### <a name="pkey"></a>PKEY

PKEY \_ GPS \_ дестбеаринг

### <a name="containers"></a>Контейнеры

JPEG, TIFF

### <a name="read-only"></a>Только для чтения

Да

### <a name="output-propvariant-type"></a>Тип выходного ПРОПВАРИАНТ

VT \_ R8

### <a name="conflict-resolution-policy"></a>Политика разрешения конфликтов

Это значение можно записать с помощью записи в System. GPS. Дестбеарингнумератор и System. GPS. Дестбеарингденоминатор. Он не может быть записан напрямую. Выверяются значения из разных схем.

### <a name="jpeg-policy"></a>Политика JPEG

### <a name="read-paths"></a>Пути чтения



| Заказ | Путь                      | Формат диска |
|-------|---------------------------|-------------|
| 1     | /APP1/IFD/GPS/{ushort = 24} |             |
| 2     | /КСМП/ексиф: Гпсдестбеаринг  |             |



 

### <a name="write-paths"></a>Пути записи



| Заказ | Путь                      | Формат диска |
|-------|---------------------------|-------------|
| 1     | /APP1/IFD/GPS/{ushort = 24} |             |
| 2     | /КСМП/ексиф: Гпсдестбеаринг  |             |



 

### <a name="remove-paths"></a>Удалить пути



| Заказ | Путь                      | Формат диска |
|-------|---------------------------|-------------|
| 1     | /APP1/IFD/GPS/{ushort = 24} |             |
| 2     | /КСМП/ексиф: гпсдестбеаринг  |             |



 

### <a name="tiff-policies"></a>Политики TIFF

### <a name="read-paths"></a>Пути чтения



| Заказ | Путь                         | Формат диска |
|-------|------------------------------|-------------|
| 1     | /ИФД/ГПС/{ушорт = 24}         |             |
| 2     | /ИФД/КСМП/ексиф: Гпсдестбеаринг |             |



 

### <a name="write-paths"></a>Пути записи



| Заказ | Путь                         | Формат диска |
|-------|------------------------------|-------------|
| 1     | /ИФД/ГПС/{ушорт = 24}         |             |
| 2     | /ИФД/КСМП/ексиф: Гпсдестбеаринг |             |



 

### <a name="remove-paths"></a>Удалить пути



| Заказ | Путь                         |
|-------|------------------------------|
| 1     | /ИФД/ГПС/{ушорт = 24}         |
| 2     | /ИФД/КСМП/ексиф: гпсдестбеаринг |



 

## <a name="remarks"></a>Комментарии

## <a name="related-topics"></a>См. также

<dl> <dt>

[System. GPS. Дестбеаринг](../properties/props-system-gps-destbearing.md)
</dt> </dl>

 

 
