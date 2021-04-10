---
description: Политика метаданных фотографии для свойства System. GPS. Меасуремоде.
ms.assetid: 911a0d81-bd12-4155-b45a-ae1a18f2dd07
title: Политика метаданных фотографии System. GPS. Меасуремоде
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a9449ca9a7d1ee5ef213c37562392be2842a09f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998643"
---
# <a name="systemgpsmeasuremode-photo-metadata-policy"></a>Политика метаданных фотографии System. GPS. Меасуремоде

Политика метаданных фотографии для свойства [System. GPS. меасуремоде](../properties/props-system-gps-measuremode.md) .

### <a name="pkey"></a>PKEY

PKEY \_ GPS \_ меасуремоде

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



| Заказ | Путь                      | Формат диска |
|-------|---------------------------|-------------|
| 1     | /APP1/IFD/GPS/{ushort = 10} | ascii       |
| 2     | /КСМП/ексиф: Гпсмеасуремоде  | Юникод     |



 

### <a name="write-paths"></a>Пути записи



| Заказ | Путь                      | Формат диска |
|-------|---------------------------|-------------|
| 1     | /APP1/IFD/GPS/{ushort = 10} | ascii       |
| 2     | /КСМП/ексиф: Гпсмеасуремоде  | Юникод     |



 

### <a name="remove-paths"></a>Удалить пути



| Заказ | Путь                      |
|-------|---------------------------|
| 1     | /APP1/IFD/GPS/{ushort = 10} |
| 2     | /КСМП/ексиф: гпсмеасуремоде  |



 

### <a name="tiff-policies"></a>Политики TIFF

### <a name="read-paths"></a>Пути чтения



| Заказ | Путь                         | Формат диска |
|-------|------------------------------|-------------|
| 1     | /ИФД/ГПС/{ушорт = 10}         | ascii       |
| 2     | /ИФД/КСМП/ексиф: Гпсмеасуремоде | Юникод     |



 

### <a name="write-paths"></a>Пути записи



| Заказ | Путь                         | Формат диска |
|-------|------------------------------|-------------|
| 1     | /ИФД/ГПС/{ушорт = 10}         | ascii       |
| 2     | /ИФД/КСМП/ексиф: Гпсмеасуремоде | Юникод     |



 

### <a name="remove-paths"></a>Удалить пути



| Заказ | Путь                         |
|-------|------------------------------|
| 1     | /ИФД/ГПС/{ушорт = 10}         |
| 2     | /ИФД/КСМП/ексиф: гпсмеасуремоде |



 

## <a name="remarks"></a>Комментарии

## <a name="related-topics"></a>См. также

<dl> <dt>

[System. GPS. Меасуремоде](../properties/props-system-gps-measuremode.md)
</dt> </dl>

 

 
