---
description: Политика метаданных фотографии для свойства System. GPS. VersionID.
ms.assetid: d3c88243-8744-4bb3-ab47-38b5354f6f7e
title: Политика метаданных фотографии System. GPS. VersionID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48ca5bd1885f0ac5c3dc14dbb5e859de3f8a26cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702313"
---
# <a name="systemgpsversionid-photo-metadata-policy"></a>Политика метаданных фотографии System. GPS. VersionID

Политика метаданных фотографии для свойства [System. GPS. VersionID](../properties/props-system-gps-versionid.md) .

### <a name="pkey"></a>PKEY

PKEY \_ GPS \_ VersionID

### <a name="containers"></a>Контейнеры

JPEG, TIFF

### <a name="read-only"></a>Только для чтения

Нет

### <a name="output-propvariant-type"></a>Тип выходного ПРОПВАРИАНТ

\_ \| Пользовательский интерфейс VT ВЕКТОРа VT \_

### <a name="input-type"></a>Тип входных данных

Буфер

### <a name="conflict-resolution-policy"></a>Политика разрешения конфликтов

Выверяются значения из разных схем.

### <a name="jpeg-policies"></a>Политики JPEG

### <a name="read-paths"></a>Пути чтения



| Заказ | Путь                     | Формат диска |
|-------|--------------------------|-------------|
| 1     | /APP1/IFD/GPS/{ushort = 0} |             |
| 2     | /КСМП/ексиф: Гпсверсионид   | Юникод     |



 

### <a name="write-paths"></a>Пути записи



| Заказ | Путь                     | Формат диска |
|-------|--------------------------|-------------|
| 1     | /APP1/IFD/GPS/{ushort = 0} |             |
| 2     | /КСМП/ексиф: Гпсверсионид   | Юникод     |



 

### <a name="remove-paths"></a>Удалить пути



| Заказ | Путь                     |
|-------|--------------------------|
| 1     | /APP1/IFD/GPS/{ushort = 0} |
| 2     | /КСМП/ексиф: гпсверсионид   |



 

### <a name="tiff-policies"></a>Политики TIFF

### <a name="read-paths"></a>Пути чтения



| Заказ | Путь                       | Формат диска |
|-------|----------------------------|-------------|
| 1     | /ИФД/ГПС/{ушорт = 0}        |             |
| 2     | /ИФД/КСМП/ексиф: Гпсверсионид | Юникод     |



 

### <a name="write-paths"></a>Пути записи



| Заказ | Путь                       | Формат диска |
|-------|----------------------------|-------------|
| 1     | /ИФД/ГПС/{ушорт = 0}        |             |
| 2     | /ИФД/КСМП/ексиф: Гпсверсионид | Юникод     |



 

### <a name="remove-paths"></a>Удалить пути



| Заказ | Путь                       |
|-------|----------------------------|
| 1     | /ИФД/ГПС/{ушорт = 0}        |
| 2     | /ИФД/КСМП/ексиф: гпсверсионид |



 

## <a name="remarks"></a>Комментарии

## <a name="related-topics"></a>См. также

<dl> <dt>

[System. GPS. VersionID](../properties/props-system-gps-versionid.md)
</dt> </dl>

 

 
