---
description: Политика метаданных фотографии для свойства System. GPS. Спидреф.
ms.assetid: 45fea6be-1e63-4244-a93d-d446e315ddd4
title: Политика метаданных фотографии System. GPS. Спидреф
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c454a016dd77345c0a85e0ca3df1ae52694bd81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693398"
---
# <a name="systemgpsspeedref-photo-metadata-policy"></a>Политика метаданных фотографии System. GPS. Спидреф

Политика метаданных фотографии для свойства [System. GPS. спидреф](../properties/props-system-gps-speedref.md) .

### <a name="pkey"></a>PKEY

PKEY \_ GPS \_ спидреф

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
| 1     | /APP1/IFD/GPS/{ushort = 12} | ascii       |
| 2     | /КСМП/ексиф: Гпсспидреф     | Юникод     |



 

### <a name="write-paths"></a>Пути записи



| Заказ | Путь                      | Формат диска |
|-------|---------------------------|-------------|
| 1     | /APP1/IFD/GPS/{ushort = 12} | ascii       |
| 2     | /КСМП/ексиф: Гпсспидреф     | Юникод     |



 

### <a name="remove-paths"></a>Удалить пути



| Заказ | Путь                      | Формат диска |
|-------|---------------------------|-------------|
| 1     | /APP1/IFD/GPS/{ushort = 12} |             |
| 2     | /КСМП/ексиф: гпсспидреф     |             |



 

### <a name="tiff-policies"></a>Политики TIFF

### <a name="read-paths"></a>Пути чтения



| Заказ | Путь                      |         |
|-------|---------------------------|---------|
| 1     | /ИФД/ГПС/{ушорт = 12}      | ascii   |
| 2     | /ИФД/КСМП/ексиф: Гпсспидреф | Юникод |



 

### <a name="write-paths"></a>Пути записи



| Заказ | Путь                      | Формат диска |
|-------|---------------------------|-------------|
| 1     | /ИФД/ГПС/{ушорт = 12}      | ascii       |
| 2     | /ИФД/КСМП/ексиф: Гпсспидреф | Юникод     |



 

### <a name="remove-paths"></a>Удалить пути



| Заказ | Путь                      |
|-------|---------------------------|
| 1     | /ИФД/ГПС/{ушорт = 12}      |
| 2     | /ИФД/КСМП/ексиф: гпсспидреф |



 

## <a name="remarks"></a>Комментарии

## <a name="related-topics"></a>См. также

<dl> <dt>

[System. GPS. Спидреф](../properties/props-system-gps-speedref.md)
</dt> </dl>

 

 
