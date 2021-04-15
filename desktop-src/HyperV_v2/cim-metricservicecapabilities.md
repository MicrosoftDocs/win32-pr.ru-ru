---
description: Описывает возможности \_ объекта МЕТРИКСЕРВИЦЕ CIM.
ms.assetid: 3b4da02f-5298-46d4-876c-404baca38c03
title: Класс CIM_MetricServiceCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricServiceCapabilities
- CIM_MetricServiceCapabilities.ControllableMetrics
- CIM_MetricServiceCapabilities.MetricsControlTypes
- CIM_MetricServiceCapabilities.ControllableManagedElements
- CIM_MetricServiceCapabilities.ManagedElementControlTypes
- CIM_MetricServiceCapabilities.SupportedMethods
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f878cb0e616cb710a33d350df866160fc0eebb83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683616"
---
# <a name="cim_metricservicecapabilities-class"></a>\_Класс CIM метриксервицекапабилитиес

Описывает возможности объекта [**\_ метриксервице CIM**](cim-metricservice.md) .

## <a name="syntax"></a>Синтаксис

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Metrics::BaseMetrics"), AMENDMENT]
class CIM_MetricServiceCapabilities : CIM_EnabledLogicalElementCapabilities
{
  string ControllableMetrics[];
  uint16 MetricsControlTypes[];
  string ControllableManagedElements[];
  uint16 ManagedElementControlTypes[];
  uint16 SupportedMethods[];
};
```

## <a name="members"></a>Члены

Класс **CIM \_ метриксервицекапабилитиес** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **CIM \_ метриксервицекапабилитиес** имеет следующие свойства.

<dl> <dt>

**контроллаблеманажеделементс**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный"), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ метриксервицекапабилитиес**.**Манажеделементконтролтипес**")
</dt> </dl>

Массив, содержащий идентификаторы экземпляров [**\_ манажеделемент CIM**](cim-managedelement.md) , управляемых службой метрик. Идентификаторы должны быть отформатированы как URI Web-Based Enterprise Management (WBEM). Чтобы использовать это свойство, служба метрик должна поддерживать включение или отключение по крайней мере одной метрики, определенной для экземпляра **CIM \_ манажеделемент** .

</dd> <dt>

**контроллаблеметрикс**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный"), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ метриксервицекапабилитиес**.**Метрикконтролтипес**")
</dt> </dl>

Массив, содержащий идентификаторы [**CIM \_ басеметрикдефинитион**](cim-basemetricdefinition.md) , определяющие метрики, управляемые службой метрик. Идентификаторы должны быть отформатированы как URI Web-Based Enterprise Management (WBEM).

Чтобы использовать это свойство, экземпляр [**CIM \_ басеметрикдефинитион**](cim-basemetricdefinition.md) должен быть связан с экземпляром [**CIM \_ метриксервице**](cim-metricservice.md) через класс [**CIM \_ сервицеаффектселемент**](cim-serviceaffectselement.md) . Кроме того, служба метрик должна поддерживать включение или отключение по крайней мере одной метрики, определенной экземпляром **CIM \_ басеметрикдефинитион** .

</dd> <dt>

**манажеделементконтролтипес**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16** , массив
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный"), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ метриксервицекапабилитиес**.**Контроллаблеманажеделементс**")
</dt> </dl>

Массив, указывающий типы элементов управления, поддерживаемые службой метрик для управляемых элементов в массиве **контроллаблеманажеделементс** . Этот массив соответствует массиву **контроллаблеманажеделементс** . Типы элементов управления в этом массиве связаны с метриками через массив **контроллаблеманажеделементс** .

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Неизвестно** (0)


</dt> <dd></dd> <dt>

<span id="Discrete"></span><span id="discrete"></span><span id="DISCRETE"></span>

**Дискретная** (2)


</dt> <dd></dd> <dt>

<span id="Bulk"></span><span id="bulk"></span><span id="BULK"></span>

**Массовый** (3)


</dt> <dd></dd> <dt>

<span id="Both"></span><span id="both"></span><span id="BOTH"></span>

**Оба** (4)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**Зарезервировано DMTF** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

**Зависит от поставщика** (32768.65 535)


</dt> <dd></dd> </dl>

</dd> <dt>

**метриксконтролтипес**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16** , массив
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный"), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ метриксервицекапабилитиес**.**Контроллаблеметрикс**")
</dt> </dl>

Массив, указывающий типы элементов управления, которые поддерживаются службой метрик. Этот массив соответствует массиву **контроллаблеметрикс** . Типы элементов управления в этом массиве связаны с метриками через массив **контроллаблеметрикс** .

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Неизвестно** (0)


</dt> <dd></dd> <dt>

<span id="Discrete"></span><span id="discrete"></span><span id="DISCRETE"></span>

**Дискретная** (2)


</dt> <dd></dd> <dt>

<span id="Bulk"></span><span id="bulk"></span><span id="BULK"></span>

**Массовый** (3)


</dt> <dd></dd> <dt>

<span id="Both"></span><span id="both"></span><span id="BOTH"></span>

**Оба** (4)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**Зарезервировано DMTF** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

**Зависит от поставщика** (32768.65 535)


</dt> <dd></dd> </dl>

</dd> <dt>

**SupportedMethods**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16** , массив
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Массив, содержащий имена методов, поддерживаемых службой метрик.

<dt>

<span id="ControlMetrics"></span><span id="controlmetrics"></span><span id="CONTROLMETRICS"></span>

**Контролметрикс** (2)


</dt> <dd></dd> <dt>

<span id="ControlMetricsByClass"></span><span id="controlmetricsbyclass"></span><span id="CONTROLMETRICSBYCLASS"></span>

**Контролметриксбикласс** (3)


</dt> <dd></dd> <dt>

<span id="ShowMetrics"></span><span id="showmetrics"></span><span id="SHOWMETRICS"></span>

**Шовметрикс** (4)


</dt> <dd></dd> <dt>

<span id="ShowMetricsByClass"></span><span id="showmetricsbyclass"></span><span id="SHOWMETRICSBYCLASS"></span>

**Шовметриксбикласс** (5)


</dt> <dd></dd> <dt>

<span id="GetMetricValues"></span><span id="getmetricvalues"></span><span id="GETMETRICVALUES"></span>

**Жетметриквалуес** (6)


</dt> <dd></dd> <dt>

<span id="ControlSampleTimes"></span><span id="controlsampletimes"></span><span id="CONTROLSAMPLETIMES"></span>

**Контролсамплетимес** (7)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**Зарезервировано DMTF** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

**Зависит от поставщика** (0x8000..)


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8<br/>                                                                                    |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                                          |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_ЕНАБЛЕДЛОГИКАЛЕЛЕМЕНТКАПАБИЛИТИЕС CIM**](cim-enabledlogicalelementcapabilities.md)
</dt> </dl>

 

