---
description: Представляет контейнер для характеристик поддерживаемого диапазона частоты.
ms.assetid: eb07c10b-8d92-40bb-8a93-ebc5db46cfd3
title: Класс Фрекуенциранжедескриптор
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FrequencyRangeDescriptor
- FrequencyRangeDescriptor.Origin
- FrequencyRangeDescriptor.MinVSyncNumerator
- FrequencyRangeDescriptor.MinVSyncDenominator
- FrequencyRangeDescriptor.MaxVSyncNumerator
- FrequencyRangeDescriptor.MaxVSyncDenominator
- FrequencyRangeDescriptor.MinHSyncNumerator
- FrequencyRangeDescriptor.MinHSyncDenominator
- FrequencyRangeDescriptor.MaxHSyncNumerator
- FrequencyRangeDescriptor.MaxHSyncDenominator
- FrequencyRangeDescriptor.ConstraintType
- FrequencyRangeDescriptor.ActiveWidth
- FrequencyRangeDescriptor.ActiveHeight
- FrequencyRangeDescriptor.MaxPixelRate
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: d18bee8a69fd8663ea54973d6e4e8219f5f74e27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692273"
---
# <a name="frequencyrangedescriptor-class"></a>Класс Фрекуенциранжедескриптор

Класс WMI **фрекуенциранжедескриптор** представляет контейнер для характеристик поддерживаемого диапазона частоты. Экземпляры этого класса являются элементами массива **мониторфрекранжес** в [**вмимониторлистедфрекуенциранжес**](wmimonitorlistedfrequencyranges.md).

## <a name="syntax"></a>Синтаксис

``` syntax
class FrequencyRangeDescriptor
{
  uint8  Origin;
  uint32 MinVSyncNumerator;
  uint32 MinVSyncDenominator;
  uint32 MaxVSyncNumerator;
  uint32 MaxVSyncDenominator;
  uint32 MinHSyncNumerator;
  uint32 MinHSyncDenominator;
  uint32 MaxHSyncNumerator;
  uint32 MaxHSyncDenominator;
  uint32 ConstraintType;
  uint32 ActiveWidth;
  uint32 ActiveHeight;
  uint32 MaxPixelRate;
};
```

## <a name="members"></a>Члены

Класс **фрекуенциранжедескриптор** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **фрекуенциранжедескриптор** имеет следующие свойства.

<dl> <dt>

**активехеигхт**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Высота активного изображения в пикселях.

</dd> <dt>

**активевидс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Ширина (в пикселях) активного изображения.

</dd> <dt>

**ConstraintType**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Тип ограничения для диапазона частот.

</dd> <dt>

**максхсинкденоминатор**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Максимальный делитель горизонтальной синхронизации.

</dd> <dt>

**максхсинкнумератор**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Максимальный числитель по горизонтальной синхронизации в килохертз (кГц).

</dd> <dt>

**макспикселрате**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Максимальная пиксельная скорость в герцах (Гц).

</dd> <dt>

**максвсинкденоминатор**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Максимальный делитель вертикальной синхронизации.

</dd> <dt>

**максвсинкнумератор**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Максимальный вертикальный числитель синхронизации в герцах (Гц).

</dd> <dt>

**минхсинкденоминатор**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Минимальный знаменатель горизонтальной синхронизации.

</dd> <dt>

**минхсинкнумератор**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Минимальный числитель по горизонтальной синхронизации в, килохертз (кГц).

</dd> <dt>

**минвсинкденоминатор**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Минимальный знаменатель синхронизации по вертикали.

</dd> <dt>

**минвсинкнумератор**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Минимальный числитель синхронизации по вертикали, в герцах (Гц).

</dd> <dt>

**Лета**
</dt> <dd> <dl> <dt>

Тип данных: **Uint8**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Лета.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                               |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                         |
| Пространство имен<br/>                | Корневой \\ инструментарий WMI<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>Вмикоре. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WmiProv.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**мсмониторкласс**](msmonitorclass.md)
</dt> </dl>

 

 




