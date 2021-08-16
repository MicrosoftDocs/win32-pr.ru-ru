---
description: Политика метаданных фотографии для свойства System. GPS. Дестлатитуде.
ms.assetid: 05284291-977d-49b8-ad92-365f68384960
title: Политика метаданных фотографии System. GPS. Дестлатитуде
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d57cce67b13235933816e244e17b5c761e1f0d230055eb82d683eb610579e5aa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119882354"
---
# <a name="systemgpsdestlatitude-photo-metadata-policy"></a>Политика метаданных фотографии System. GPS. Дестлатитуде

Политика метаданных фотографии для свойства [System. GPS. дестлатитуде](../properties/props-system-gps-destlatitude.md) .

### <a name="pkey"></a>PKEY

PKEY \_ GPS \_ дестлатитуде

### <a name="containers"></a>Контейнеры

JPEG, TIFF

### <a name="read-only"></a>Только для чтения

Да

### <a name="output-propvariant-type"></a>Тип выходного ПРОПВАРИАНТ

VT \_ вектор \| VT \_ R8

### <a name="input-propvariant-type"></a>Тип входного ПРОПВАРИАНТ

VT \_ вектор \| VT \_ R8

### <a name="conflict-resolution-policy"></a>Политика разрешения конфликтов

Это значение формируется из System. GPS. Дестлатитуденумератор и System. GPS. Дестлатитудеденоминатор. Он не может быть записан напрямую. Выверяются значения из разных схем.

### <a name="jpeg-policy"></a>Политика JPEG

### <a name="read-paths"></a>Пути чтения



| Номер | Путь                      | Формат диска |
|-------|---------------------------|-------------|
| 1     | /APP1/IFD/GPS/{ushort = 20} |             |
| 2     | /КСМП/ексиф: Гпсдестлатитуде |             |



 

### <a name="write-paths"></a>Пути записи



| Номер | Путь                      | Формат диска |
|-------|---------------------------|-------------|
| 1     | /APP1/IFD/GPS/{ushort = 20} |             |
| 2     | /КСМП/ексиф: Гпсдестлатитуде |             |



 

### <a name="remove-paths"></a>Удалить пути



| Номер | Путь                      |
|-------|---------------------------|
| 1     | /APP1/IFD/GPS/{ushort = 20} |
| 2     | /КСМП/ексиф: гпсдестлатитуде |



 

### <a name="tiff-policies"></a>Политики TIFF

### <a name="read-paths"></a>Пути чтения



| Номер | Путь                          | Формат диска |
|-------|-------------------------------|-------------|
| 1     | /ИФД/ГПС/{ушорт = 20}          |             |
| 2     | /ИФД/КСМП/ексиф: Гпсдестлатитуде |             |



 

### <a name="write-paths"></a>Пути записи



| Номер | Путь                          | Формат диска |
|-------|-------------------------------|-------------|
| 1     | /ИФД/ГПС/{ушорт = 20}          |             |
| 2     | /ИФД/КСМП/ексиф: Гпсдестлатитуде |             |



 

### <a name="remove-paths"></a>Удалить пути



| Номер | Путь                          |
|-------|-------------------------------|
| 1     | /ИФД/ГПС/{ушорт = 20}          |
| 2     | /ИФД/КСМП/ексиф: гпсдестлатитуде |



 

## <a name="remarks"></a>Remarks

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[System. GPS. Дестлатитуде](../properties/props-system-gps-destlatitude.md)
</dt> </dl>

 

 
