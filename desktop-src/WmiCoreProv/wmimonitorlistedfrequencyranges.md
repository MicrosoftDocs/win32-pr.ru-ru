---
description: Список частотных диапазонов, поддерживаемых монитором.
ms.assetid: e4713650-5f8c-4808-8b4f-1d29c54ab4e3
title: Класс Вмимониторлистедфрекуенциранжес
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorListedFrequencyRanges
- WmiMonitorListedFrequencyRanges.Active
- WmiMonitorListedFrequencyRanges.InstanceName
- WmiMonitorListedFrequencyRanges.NumOfMonitorFreqRanges
- WmiMonitorListedFrequencyRanges.MonitorFreqRanges
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 41b49c293d5661d523138b01c093fce627e5bedf3d1e783dccb8248edf88546c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051142"
---
# <a name="wmimonitorlistedfrequencyranges-class"></a>Класс Вмимониторлистедфрекуенциранжес

Класс WMI **вмимониторлистедфрекуенциранжес** перечисляет диапазоны частот, поддерживаемые монитором. эти диапазоны находятся в определении видеовходов с расширенным расширенным отображаемым идентификационными данными (E-EDID), а также в файле Windows INF, содержащем данные драйвера устройства.

## <a name="syntax"></a>Синтаксис

``` syntax
class WmiMonitorListedFrequencyRanges : MSMonitorClass
{
  boolean                  Active;
  string                   InstanceName;
  uint16                   NumOfMonitorFreqRanges;
  FrequencyRangeDescriptor MonitorFreqRanges[];
};
```

## <a name="members"></a>Члены

Класс **вмимониторлистедфрекуенциранжес** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **вмимониторлистедфрекуенциранжес** имеет следующие свойства.

<dl> <dt>

**Активен**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает активный монитор.

</dd> <dt>

**InstanceName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **ключ**
</dt> </dl>

Имя конкретного экземпляра монитора.

</dd> <dt>

**мониторфрекранжес**
</dt> <dd> <dl> <dt>

Тип данных: массив **фрекуенциранжедескриптор**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Список диапазонов частот монитора, представленных экземплярами класса [**фрекуенциранжедескриптор**](frequencyrangedescriptor.md) .

</dd> <dt>

**нумофмониторфрекранжес**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Число перечисленных поддерживаемых диапазонов частоты мониторов.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                               |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                         |
| Пространство имен<br/>                | Корневой \\ инструментарий WMI<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>Вмикоре. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WmiProv.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**мсмониторкласс**](msmonitorclass.md)
</dt> </dl>

 

 




