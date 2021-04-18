---
description: Политика метаданных фотографии для свойства System. GPS. Дестдистанце.
ms.assetid: 1bd72acb-f462-454d-aec2-72d5b4517de3
title: Политика метаданных фотографии System. GPS. Дестдистанце
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecc71c89ae6270f5babf08637f54baaf2cb57aae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683780"
---
# <a name="systemgpsdestdistance-photo-metadata-policy"></a>Политика метаданных фотографии System. GPS. Дестдистанце

Политика метаданных фотографии для свойства [System. GPS. дестдистанце](../properties/props-system-gps-destdistance.md) .

### <a name="pkey"></a>PKEY

PKEY \_ GPS \_ дестдистанце

### <a name="containers"></a>Контейнеры

JPEG, TIFF

### <a name="read-only"></a>Только для чтения

Да

### <a name="output-propvariant-type"></a>Тип выходного ПРОПВАРИАНТ

VT \_ R8

### <a name="conflict-resolution-policy"></a>Политика разрешения конфликтов

Это значение формируется из System. GPS. Дестдистанценумератор и System. GPS. Дестдистанцеденоминатор. Он не может быть записан напрямую. Выверяются значения из разных схем.

### <a name="jpeg-policy"></a>Политика JPEG

### <a name="read-paths"></a>Пути чтения



| Заказ | Путь                      | Формат диска |
|-------|---------------------------|-------------|
| 1     | /APP1/IFD/GPS/{ushort = 26} |             |
| 2     | /КСМП/ексиф: Гпсдестдистанце |             |



 

### <a name="write-paths"></a>Пути записи



| Заказ | Путь                      | Формат диска |
|-------|---------------------------|-------------|
| 1     | /APP1/IFD/GPS/{ushort = 26} |             |
| 2     | /КСМП/ексиф: Гпсдестдистанце |             |



 

### <a name="remove-paths"></a>Удалить пути



| Заказ | Путь                      |
|-------|---------------------------|
| 1     | /APP1/IFD/GPS/{ushort = 26} |
| 2     | /КСМП/ексиф: гпсдестдистанце |



 

### <a name="tiff-policies"></a>Политики TIFF

### <a name="read-paths"></a>Пути чтения



| Заказ | Путь                          | Формат диска |
|-------|-------------------------------|-------------|
| 1     | /ИФД/ГПС/{ушорт = 26}          |             |
| 2     | /ИФД/КСМП/ексиф: Гпсдестдистанце |             |



 

### <a name="write-paths"></a>Пути записи



| Заказ | Путь                          | Формат диска |
|-------|-------------------------------|-------------|
| 1     | /ИФД/ГПС/{ушорт = 26}          |             |
| 2     | /ИФД/КСМП/ексиф: Гпсдестдистанце |             |



 

### <a name="remove-paths"></a>Удалить пути



| Заказ | Путь                          |
|-------|-------------------------------|
| 1     | /ИФД/ГПС/{ушорт = 26}          |
| 2     | /ИФД/КСМП/ексиф: гпсдестдистанце |



 

## <a name="remarks"></a>Комментарии

## <a name="related-topics"></a>См. также

<dl> <dt>

[System. GPS. Дестдистанце](../properties/props-system-gps-destdistance.md)
</dt> </dl>

 

 
