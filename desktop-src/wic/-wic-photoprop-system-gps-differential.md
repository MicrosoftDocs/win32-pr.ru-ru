---
description: Политика метаданных фотографии для свойства System. GPS. DIFFERENTIAL.
ms.assetid: 330d1f88-5f54-4e29-b57f-eb7112203e04
title: Политика метаданных фотографии System. GPS. Differential
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dc3f114683d324a067fe4ce4034e2de5cfc88da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348575"
---
# <a name="systemgpsdifferential-photo-metadata-policy"></a>Политика метаданных фотографии System. GPS. Differential

Политика метаданных фотографии для свойства [System. GPS. Differential](../properties/props-system-gps-differential.md) .

### <a name="pkey"></a>PKEY

\_Разностная копия GPS "PKEY" \_

### <a name="containers"></a>Контейнеры

JPEG, TIFF

### <a name="read-only"></a>Только для чтения

Нет

### <a name="output-propvariant-type"></a>Тип выходного ПРОПВАРИАНТ

VT \_ UI2

### <a name="input-propvariant-type"></a>Тип входного ПРОПВАРИАНТ

\_Все они принимают VT UI1, VT \_ UI2 и VT \_ UI4.

### <a name="conflict-resolution-policy"></a>Политика разрешения конфликтов

Выверяются значения из разных схем.

### <a name="jpeg-policies"></a>Политики JPEG

### <a name="read-paths"></a>Пути чтения



| Заказ | Путь                      | Формат диска |
|-------|---------------------------|-------------|
| 1     | /APP1/IFD/GPS/{ushort = 30} | ushort      |
| 2     | /КСМП/ексиф: Гпсдифферентиал | Юникод     |



 

### <a name="write-paths"></a>Пути записи



| Заказ | Путь                      | Формат диска |
|-------|---------------------------|-------------|
| 1     | /APP1/IFD/GPS/{ushort = 30} | ushort      |
| 2     | /КСМП/ексиф: Гпсдифферентиал | Юникод     |



 

### <a name="remove-paths"></a>Удалить пути



| Заказ | Путь                      |
|-------|---------------------------|
| 1     | /APP1/IFD/GPS/{ushort = 30} |
| 2     | /КСМП/ексиф: гпсдифферентиал |



 

### <a name="tiff-policies"></a>Политики TIFF

### <a name="read-paths"></a>Пути чтения



| Заказ | Путь                          | Формат диска |
|-------|-------------------------------|-------------|
| 1     | /ИФД/ГПС/{ушорт = 30}          | ushort      |
| 2     | /ИФД/КСМП/ексиф: Гпсдифферентиал | Юникод     |



 

### <a name="write-paths"></a>Пути записи



| Заказ | Путь                          | Формат диска |
|-------|-------------------------------|-------------|
| 1     | /ИФД/ГПС/{ушорт = 30}          | ushort      |
| 2     | /ИФД/КСМП/ексиф: Гпсдифферентиал | Юникод     |



 

### <a name="remove-paths"></a>Удалить пути



| Заказ | Путь                          |
|-------|-------------------------------|
| 1     | /ИФД/ГПС/{ушорт = 30}          |
| 2     | /ИФД/КСМП/ексиф: гпсдифферентиал |



 

## <a name="remarks"></a>Комментарии

## <a name="related-topics"></a>См. также

<dl> <dt>

[System. GPS. Differential](../properties/props-system-gps-differential.md)
</dt> </dl>

 

 
