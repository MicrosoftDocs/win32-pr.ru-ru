---
description: Политика метаданных фотографии для свойства System. GPS. Процессингмесод.
ms.assetid: 840021a8-ec1d-4916-93b2-7cc1803e2d8c
title: Политика метаданных фотографии System. GPS. Процессингмесод
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02bf1484eb8e8a53c65a9cd43c54b076e418d4eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674387"
---
# <a name="systemgpsprocessingmethod-photo-metadata-policy"></a>Политика метаданных фотографии System. GPS. Процессингмесод

Политика метаданных фотографии для свойства [System. GPS. процессингмесод](../properties/props-system-gps-processingmethod.md) .

### <a name="pkey"></a>PKEY

PKEY \_ GPS \_ процессингмесод

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



| Заказ | Путь                          | Формат диска |
|-------|-------------------------------|-------------|
| 1     | /APP1/IFD/GPS/{ushort = 27}     |             |
| 2     | /КСМП/ексиф: Гпспроцессингмесод | Юникод     |



 

### <a name="write-paths"></a>Пути записи



| Заказ | Путь                          | Формат диска |
|-------|-------------------------------|-------------|
| 1     | /APP1/IFD/GPS/{ushort = 27}     |             |
| 2     | /КСМП/ексиф: Гпспроцессингмесод | Юникод     |



 

### <a name="remove-paths"></a>Удалить пути



| Заказ | Путь                          |
|-------|-------------------------------|
| 1     | /APP1/IFD/GPS/{ushort = 27}     |
| 2     | /КСМП/ексиф: гпспроцессингмесод |



 

### <a name="tiff-policies"></a>Политики TIFF

### <a name="read-paths"></a>Пути чтения



| Заказ | Путь                              | Формат диска |
|-------|-----------------------------------|-------------|
| 1     | /ИФД/КСМП/ексиф: Гпспроцессингмесод | Юникод     |
| 2     | /ИФД/ГПС/{ушорт = 27}              |             |



 

### <a name="write-paths"></a>Пути записи



| Заказ | Путь                              | Формат диска |
|-------|-----------------------------------|-------------|
| 1     | /ИФД/КСМП/ексиф: Гпспроцессингмесод | Юникод     |
| 2     | /ИФД/ГПС/{ушорт = 27}              |             |



 

### <a name="remove-paths"></a>Удалить пути



| Заказ | Путь                              |
|-------|-----------------------------------|
| 1     | /ИФД/КСМП/ексиф: гпспроцессингмесод |
| 2     | /ИФД/ГПС/{ушорт = 27}              |



 

## <a name="remarks"></a>Комментарии

## <a name="related-topics"></a>См. также

<dl> <dt>

[System. GPS. Процессингмесод](../properties/props-system-gps-processingmethod.md)
</dt> </dl>

 

 
