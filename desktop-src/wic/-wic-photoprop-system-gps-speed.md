---
description: Политика метаданных фотографии для свойства System. GPS. Speed.
ms.assetid: 278826c2-3057-4da2-8c86-0e44471ad7b0
title: Политика метаданных фотографии System. GPS. Speed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26d89f755114a73ab17388a1718d5ad0cbdf5a2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693399"
---
# <a name="systemgpsspeed-photo-metadata-policy"></a>Политика метаданных фотографии System. GPS. Speed

Политика метаданных фотографии для свойства [System. GPS. Speed](../properties/props-system-gps-speed.md) .

### <a name="pkey"></a>PKEY

" \_ Высокая скорость" для GPS \_

### <a name="containers"></a>Контейнеры

JPEG, TIFF

### <a name="read-only"></a>Только для чтения

Да

### <a name="output-propvariant-type"></a>Тип выходного ПРОПВАРИАНТ

VT \_ R8

### <a name="conflict-resolution-policy"></a>Политика разрешения конфликтов

Это значение формируется из System. GPS. Спиднумератор и System. GPS. Спидденоминатор. Он не может быть записан напрямую. Выверяются значения из разных схем.

### <a name="jpeg-policy"></a>Политика JPEG

### <a name="read-paths"></a>Пути чтения



| Заказ | Путь                      | Формат диска |
|-------|---------------------------|-------------|
| 1     | /APP1/IFD/GPS/{ushort = 13} |             |
| 2     | /КСМП/ексиф: Гпсспид        |             |



 

### <a name="write-paths"></a>Пути записи



| Заказ | Путь                      | Формат диска |
|-------|---------------------------|-------------|
| 1     | /APP1/IFD/GPS/{ushort = 13} |             |
| 2     | /КСМП/ексиф: Гпсспид        |             |



 

### <a name="remove-paths"></a>Удалить пути



| Заказ | Путь                      |
|-------|---------------------------|
| 1     | /APP1/IFD/GPS/{ushort = 13} |
| 2     | /КСМП/ексиф: гпсспид        |



 

### <a name="tiff-policies"></a>Политики TIFF

### <a name="read-paths"></a>Пути чтения



| Заказ | Путь                   | Формат диска |
|-------|------------------------|-------------|
| 1     | /ИФД/ГПС/{ушорт = 13}   |             |
| 2     | /ИФД/КСМП/ексиф: Гпсспид |             |



 

### <a name="write-paths"></a>Пути записи



| Заказ | Путь                   | Формат диска |
|-------|------------------------|-------------|
| 1     | /ИФД/ГПС/{ушорт = 13}   |             |
| 2     | /ИФД/КСМП/ексиф: Гпсспид |             |



 

### <a name="remove-paths"></a>Удалить пути



| Заказ | Путь                   |
|-------|------------------------|
| 1     | /ИФД/ГПС/{ушорт = 13}   |
| 2     | /ИФД/КСМП/ексиф: гпсспид |



 

## <a name="remarks"></a>Комментарии

## <a name="related-topics"></a>См. также

<dl> <dt>

[System. GPS. Speed](../properties/props-system-gps-speed.md)
</dt> </dl>

 

 
