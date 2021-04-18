---
description: Политика метаданных фотографии для свойства System. GPS. Имгдиректион.
ms.assetid: c9a0f5de-4010-4251-a5d5-8728b7ae6d33
title: Политика метаданных фотографии System. GPS. Имгдиректион
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 013edd632f98f1359c4f3c04856b0409c70eaa56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712795"
---
# <a name="systemgpsimgdirection-photo-metadata-policy"></a>Политика метаданных фотографии System. GPS. Имгдиректион

Политика метаданных фотографии для свойства [System. GPS. имгдиректион](../properties/props-system-gps-imgdirection.md) .

### <a name="pkey"></a>PKEY

PKEY \_ GPS \_ имгдиректион

### <a name="containers"></a>Контейнеры

JPEG, TIFF

### <a name="read-only"></a>Только для чтения

Да

### <a name="output-propvariant-type"></a>Тип выходного ПРОПВАРИАНТ

VT \_ R8

### <a name="conflict-resolution-policy"></a>Политика разрешения конфликтов

Это значение можно записать с помощью записи в System. GPS. Имгдиректионнумератор и System. GPS. Имгдиректионденоминатор. Он не может быть записан напрямую. Выверяются значения из разных схем.

### <a name="jpeg-policy"></a>Политика JPEG

### <a name="read-paths"></a>Пути чтения



| Заказ | Путь                      | Формат диска |
|-------|---------------------------|-------------|
| 1     | /APP1/IFD/GPS/{ushort = 17} |             |
| 2     | /КСМП/ексиф: Гпсимгдиректион |             |



 

### <a name="write-paths"></a>Пути записи



| Заказ | Путь                      | Формат диска |
|-------|---------------------------|-------------|
| 1     | /APP1/IFD/GPS/{ushort = 17} |             |
| 2     | /КСМП/ексиф: Гпсимгдиректион |             |



 

### <a name="remove-paths"></a>Удалить пути



| Заказ | Путь                      |
|-------|---------------------------|
| 1     | /APP1/IFD/GPS/{ushort = 17} |
| 2     | /КСМП/ексиф: гпсимгдиректион |



 

### <a name="tiff-policies"></a>Политики TIFF

### <a name="read-paths"></a>Пути чтения



| Заказ | Путь                          | Формат диска |
|-------|-------------------------------|-------------|
| 1     | /ИФД/ГПС/{ушорт = 17}          |             |
| 2     | /ИФД/КСМП/ексиф: Гпсимгдиректион |             |



 

### <a name="write-paths"></a>Пути записи



| Заказ | Путь                          | Формат диска |
|-------|-------------------------------|-------------|
| 1     | /ИФД/ГПС/{ушорт = 17}          |             |
| 2     | /ИФД/КСМП/ексиф: Гпсимгдиректион |             |



 

### <a name="remove-paths"></a>Удалить пути



| Заказ | Путь                          |
|-------|-------------------------------|
| 1     | /ИФД/ГПС/{ушорт = 17}          |
| 2     | /ИФД/КСМП/ексиф: гпсимгдиректион |



 

## <a name="remarks"></a>Комментарии

## <a name="related-topics"></a>См. также

<dl> <dt>

[System. GPS. Имгдиректион](../properties/props-system-gps-imgdirection.md)
</dt> </dl>

 

 
