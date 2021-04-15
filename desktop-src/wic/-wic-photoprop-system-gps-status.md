---
description: Политика метаданных фотографии для свойства System. GPS. status.
ms.assetid: 74ea0384-3b1f-4d5e-8713-7b3936813a3a
title: Политика метаданных фотографии System. GPS. status
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dac08139a267052f8d6dd3dc463e2a2768309a41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683570"
---
# <a name="systemgpsstatus-photo-metadata-policy"></a>Политика метаданных фотографии System. GPS. status

Политика метаданных фотографии для свойства [System. GPS. status](../properties/props-system-gps-status.md) .

### <a name="pkey"></a>PKEY

\_Состояние состояния GPS "PKEY" \_

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



| Заказ | Путь                     | Формат диска |
|-------|--------------------------|-------------|
| 1     | /APP1/IFD/GPS/{ushort = 9} | ascii       |
| 2     | /КСМП/ексиф: Гпсстатус      | Юникод     |



 

### <a name="write-paths"></a>Пути записи



| Заказ | Путь                     | Формат диска |
|-------|--------------------------|-------------|
| 1     | /APP1/IFD/GPS/{ushort = 9} | ascii       |
| 2     | /КСМП/ексиф: Гпсстатус      | Юникод     |



 

### <a name="remove-paths"></a>Удалить пути



| Заказ | Путь                     |
|-------|--------------------------|
| 1     | /APP1/IFD/GPS/{ushort = 9} |
| 2     | /КСМП/ексиф: гпсстатус      |



 

### <a name="tiff-policies"></a>Политики TIFF

### <a name="read-paths"></a>Пути чтения



| Заказ | Путь                    | Формат диска |
|-------|-------------------------|-------------|
| 1     | /ИФД/ГПС/{ушорт = 9}     | ascii       |
| 2     | /ИФД/КСМП/ексиф: Гпсстатус | Юникод     |



 

### <a name="write-paths"></a>Пути записи



| Заказ | Путь                    | Формат диска |
|-------|-------------------------|-------------|
| 1     | /ИФД/ГПС/{ушорт = 9}     | ascii       |
| 2     | /ИФД/КСМП/ексиф: Гпсстатус | Юникод     |



 

### <a name="remove-paths"></a>Удалить пути



| Заказ | Путь                    |
|-------|-------------------------|
| 1     | /ИФД/ГПС/{ушорт = 9}     |
| 2     | /ИФД/КСМП/ексиф: гпсстатус |



 

## <a name="remarks"></a>Комментарии

## <a name="related-topics"></a>См. также

<dl> <dt>

[System. GPS. status](../properties/props-system-gps-status.md)
</dt> </dl>

 

 
