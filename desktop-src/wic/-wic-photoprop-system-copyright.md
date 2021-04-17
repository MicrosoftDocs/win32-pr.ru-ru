---
description: Политика метаданных фотографии для свойства System. Copyright.
ms.assetid: 84d2f55b-5ca4-4912-b038-c18a72e6fc34
title: Политика метаданных по System. © Photo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fc65024458d88088e3c0cbeccc3bc9ea0211910
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712803"
---
# <a name="systemcopyright-photo-metadata-policy"></a>Политика метаданных по System. © Photo

Политика метаданных фотографии для свойства [System. Copyright](../properties/props-system-copyright.md) .

### <a name="pkey"></a>PKEY

\_Авторские права PKEY

### <a name="containers"></a>Контейнеры

JPEG, TIFF

### <a name="read-only"></a>Только для чтения

Нет

### <a name="output-propvariant-type"></a>Тип выходного ПРОПВАРИАНТ

VT \_ LPWSTR

### <a name="input-propvariant-type"></a>Тип входного ПРОПВАРИАНТ

Строка

### <a name="conflict-resolution-policy"></a>Политика разрешения конфликтов

Выверяются значения из разных схем.

### <a name="jpeg-policy"></a>Политика JPEG

### <a name="read-paths"></a>Пути чтения



| Заказ | Путь                                      | Формат диска |
|-------|-------------------------------------------|-------------|
|       | /APP1/IFD/{ushort = 33432}                  | ascii       |
|       | уведомление/APP13/IRB/8bimiptc/IPTC/Copyright |             |
|       | /КСМП/ <xmpalt> DC: права              | Юникод     |
|       | /КСМП/ДК: права доступа                            | Юникод     |
|       | уведомление/APP13/IRB/8bimiptc/IPTC/Copyright |             |



 

### <a name="write-paths"></a>Пути записи



| Заказ | Путь                                      | Формат диска |
|-------|-------------------------------------------|-------------|
|       | /КСМП/ДК: права доступа                            | Юникод     |
|       | /КСМП/ <xmpalt> DC: права              | Юникод     |
|       | уведомление/APP13/IRB/8bimiptc/IPTC/Copyright |             |
|       | /APP1/IFD/{ushort = 33432}                  | ascii       |



 

### <a name="remove-paths"></a>Удалить пути



| Заказ | Путь                                      |
|-------|-------------------------------------------|
|       | /КСМП/ДК: права доступа                            |
|       | уведомление/APP13/IRB/8bimiptc/IPTC/Copyright |
|       | /APP1/IFD/{ushort = 33432}                  |



 

### <a name="tiff-policy"></a>Политика TIFF

### <a name="read-paths"></a>Пути чтения



| Заказ | Путь                                    | Формат диска |
|-------|-----------------------------------------|-------------|
|       | /ИФД/{ушорт = 33432}                     | ascii       |
|       | уведомление/ИФД/иптк/копиригхт              |             |
|       | /ИФД/КСМП/ <xmpalt> DC: права        | Юникод     |
|       | /ИФД/КСМП/ДК: права доступа                      | Юникод     |
|       | уведомление/ИФД/иптк/копиригхт              |             |
|       | уведомление/IFD/IRB/8bimiptc/IPTC/Copyright |             |



 

### <a name="write-paths"></a>Пути записи



| Заказ | Путь                                    | Формат диска |
|-------|-----------------------------------------|-------------|
|       | /ИФД/КСМП/ДК: права доступа                      | Юникод     |
|       | /ИФД/КСМП/ <xmpalt> DC: права        | Юникод     |
|       | уведомление/ИФД/иптк/копиригхт              |             |
|       | уведомление/IFD/IRB/8bimiptc/IPTC/Copyright |             |
|       | /ИФД/{ушорт = 33432}                     | ascii       |



 

### <a name="remove-paths"></a>Удалить пути



| Заказ | Путь                                    |
|-------|-----------------------------------------|
|       | /ИФД/КСМП/ДК: права доступа                      |
|       | уведомление/ИФД/иптк/копиригхт              |
|       | уведомление/IFD/IRB/8bimiptc/IPTC/Copyright |
|       | /ИФД/{ушорт = 33432}                     |



 

## <a name="remarks"></a>Комментарии

## <a name="related-topics"></a>См. также

<dl> <dt>

[System. ©](../properties/props-system-copyright.md)
</dt> </dl>

 

 
