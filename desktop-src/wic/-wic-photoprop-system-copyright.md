---
description: Политика метаданных фотографии для свойства System. Copyright.
ms.assetid: 84d2f55b-5ca4-4912-b038-c18a72e6fc34
title: Политика метаданных по System. © Photo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3e17190205b3df5c2ede9b1a7db231d0fdbbe21
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882695"
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



| Порядок | путь                                      | Формат диска |
|-------|-------------------------------------------|-------------|
|       | /APP1/IFD/{ushort = 33432}                  | ascii       |
|       | уведомление/APP13/IRB/8bimiptc/IPTC/Copyright |             |
|       | /КСМП/ &lt; ксмпалт &gt; DC: права              | Юникод     |
|       | /КСМП/ДК: права доступа                            | Юникод     |
|       | уведомление/APP13/IRB/8bimiptc/IPTC/Copyright |             |



 

### <a name="write-paths"></a>Пути записи



| Порядок | путь                                      | Формат диска |
|-------|-------------------------------------------|-------------|
|       | /КСМП/ДК: права доступа                            | Юникод     |
|       | /КСМП/ &lt; ксмпалт &gt; DC: права              | Юникод     |
|       | уведомление/APP13/IRB/8bimiptc/IPTC/Copyright |             |
|       | /APP1/IFD/{ushort = 33432}                  | ascii       |



 

### <a name="remove-paths"></a>Удалить пути



| Порядок | путь                                      |
|-------|-------------------------------------------|
|       | /КСМП/ДК: права доступа                            |
|       | уведомление/APP13/IRB/8bimiptc/IPTC/Copyright |
|       | /APP1/IFD/{ushort = 33432}                  |



 

### <a name="tiff-policy"></a>Политика TIFF

### <a name="read-paths"></a>Пути чтения



| Порядок | путь                                    | Формат диска |
|-------|-----------------------------------------|-------------|
|       | /ИФД/{ушорт = 33432}                     | ascii       |
|       | уведомление/ИФД/иптк/копиригхт              |             |
|       | /ИФД/КСМП/ &lt; ксмпалт &gt; DC: права        | Юникод     |
|       | /ИФД/КСМП/ДК: права доступа                      | Юникод     |
|       | уведомление/ИФД/иптк/копиригхт              |             |
|       | уведомление/IFD/IRB/8bimiptc/IPTC/Copyright |             |



 

### <a name="write-paths"></a>Пути записи



| Порядок | путь                                    | Формат диска |
|-------|-----------------------------------------|-------------|
|       | /ИФД/КСМП/ДК: права доступа                      | Юникод     |
|       | /ИФД/КСМП/ &lt; ксмпалт &gt; DC: права        | Юникод     |
|       | уведомление/ИФД/иптк/копиригхт              |             |
|       | уведомление/IFD/IRB/8bimiptc/IPTC/Copyright |             |
|       | /ИФД/{ушорт = 33432}                     | ascii       |



 

### <a name="remove-paths"></a>Удалить пути



| Порядок | путь                                    |
|-------|-----------------------------------------|
|       | /ИФД/КСМП/ДК: права доступа                      |
|       | уведомление/ИФД/иптк/копиригхт              |
|       | уведомление/IFD/IRB/8bimiptc/IPTC/Copyright |
|       | /ИФД/{ушорт = 33432}                     |



 

## <a name="remarks"></a>Комментарии

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[System. ©](../properties/props-system-copyright.md)
</dt> </dl>

 

 
