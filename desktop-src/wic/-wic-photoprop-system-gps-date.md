---
description: Политика метаданных фотографии для свойства System. GPS. Date.
ms.assetid: 75047658-b6f3-454e-961a-89016c244bf6
title: Политика метаданных фотографии System. GPS. Date
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c736c79cd76d2d070d727dc024925717b386cac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272297"
---
# <a name="systemgpsdate-photo-metadata-policy"></a>Политика метаданных фотографии System. GPS. Date

Политика метаданных фотографии для свойства [System. GPS. Date](../properties/props-system-gps-date.md) .

### <a name="pkey"></a>PKEY

Дата и время \_ GPS \_

### <a name="containers"></a>Контейнеры

JPEG, TIFF

### <a name="read-only"></a>Только для чтения

Нет

### <a name="input-type"></a>Тип входных данных

Строка.

### <a name="conflict-resolution-policy"></a>Политика разрешения конфликтов

Выверяются значения из разных схем.

### <a name="jpeg-policies"></a>Политики JPEG

### <a name="read-paths"></a>Пути чтения



| Заказ | Путь                      | Формат диска |
|-------|---------------------------|-------------|
| 1     | /APP1/IFD/GPS/{ushort = 29} | ascii       |
| 2     | /КСМП/ексиф: Гпстиместамп    | Юникод     |



 

### <a name="write-paths"></a>Пути записи



| Заказ | Путь                      | Формат диска |
|-------|---------------------------|-------------|
| 1     | /APP1/IFD/GPS/{ushort = 29} | ascii       |
| 2     | /КСМП/ексиф: Гпстиместамп    | Юникод     |



 

### <a name="remove-paths"></a>Удалить пути



| Заказ | Путь                      |
|-------|---------------------------|
| 1     | /APP1/IFD/GPS/{ushort = 29} |
| 2     | /КСМП/ексиф: Гпстиместамп    |



 

### <a name="tiff-policies"></a>Политики TIFF

### <a name="read-paths"></a>Пути чтения



| Заказ | Путь                       | Формат диска |
|-------|----------------------------|-------------|
| 1     | /ИФД/ГПС/{ушорт = 29}       | ascii       |
| 2     | /ИФД/КСМП/ексиф: Гпстиместамп | Юникод     |



 

### <a name="write-paths"></a>Пути записи



| Заказ | Путь                       | Формат диска |
|-------|----------------------------|-------------|
| 1     | /ИФД/ГПС/{ушорт = 29}       | ascii       |
| 2     | /ИФД/КСМП/ексиф: Гпстиместамп | Юникод     |



 

### <a name="remove-paths"></a>Удалить пути



| Заказ | Путь                       |
|-------|----------------------------|
| 1     | /ИФД/ГПС/{ушорт = 29}       |
| 2     | /ИФД/КСМП/ексиф: Гпстиместамп |



 

## <a name="remarks"></a>Комментарии

## <a name="related-topics"></a>См. также

<dl> <dt>

[System. GPS. Date](../properties/props-system-gps-date.md)
</dt> </dl>

 

 
