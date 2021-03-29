---
description: Представляет определение метрики, которая является производной от другого значения метрики. Объект CIM \_ аггрегатионметрикдефинитион должен быть связан с \_ объектами CIM манажеделемент, к которым он применяется.
ms.assetid: 0059bfd6-ecf3-41f0-be6b-0ce46dfbbb18
title: Класс CIM_AggregationMetricDefinition
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AggregationMetricDefinition
- CIM_AggregationMetricDefinition.ChangeType
- CIM_AggregationMetricDefinition.SimpleFunction
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9a84eed5a725ebff3b39ca92bab530ef90cfca58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812736"
---
# <a name="cim_aggregationmetricdefinition-class"></a>\_Класс CIM аггрегатионметрикдефинитион

Представляет определение метрики, которая является производной от другого значения метрики. Объект **CIM \_ аггрегатионметрикдефинитион** должен быть связан с объектами **CIM \_ манажеделемент** , к которым он применяется.

## <a name="syntax"></a>Синтаксис

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Metrics::BaseMetric"), AMENDMENT]
class CIM_AggregationMetricDefinition : CIM_BaseMetricDefinition
{
  uint16 ChangeType = 5;
  uint16 SimpleFunction;
};
```

## <a name="members"></a>Члены

Класс **CIM \_ аггрегатионметрикдефинитион** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **CIM \_ аггрегатионметрикдефинитион** имеет следующие свойства.

<dl> <dt>

**ChangeType**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ChangeType"), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ аггрегатионметрикдефинитион**.**Continuous**»)
</dt> </dl>

Указывает, как изменяется значение метрики с помощью общих атрибутов, таких как изменение направления, минимальное и максимальное значения, а также семантика упаковки.

<dt>

<span id="Simple_Function"></span><span id="simple_function"></span><span id="SIMPLE_FUNCTION"></span>

**Простая функция** (5)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**Зарезервировано DMTF** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Поставщик зарезервирован** (32768.. 65535)


</dt> <dd></dd> </dl>

</dd> <dt>

**симплефунктион**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Базовые вычисления, выполняемые с базовой метрикой, которые поступают на значение этой производной метрики. Это свойство имеет значение **null** , если свойство **ChangeType** имеет значение, отличное от "5" (простая функция).

<dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)


</dt> <dd></dd> <dt>

<span id="Minimum"></span><span id="minimum"></span><span id="MINIMUM"></span>

<span id="Minimum"></span><span id="minimum"></span><span id="MINIMUM"></span>**Минимум** (2)


</dt> <dd>

Метрика сообщает наименьшее значение, обнаруженное для связанной отслеживаемой сущности. Это также называется нижнего предела.

</dd> <dt>

<span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>

<span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>**Максимум** (3)


</dt> <dd>

Метрика сообщает максимальное значение, обнаруженное для связанной отслеживаемой сущности. Это также называется верхний предел.

</dd> <dt>

<span id="Average"></span><span id="average"></span><span id="AVERAGE"></span>

<span id="Average"></span><span id="average"></span><span id="AVERAGE"></span>**Среднее значение** (4)


</dt> <dd>

Метрика Возвращает среднее значение базовых значений метрики.

</dd> <dt>

<span id="Median"></span><span id="median"></span><span id="MEDIAN"></span>

<span id="Median"></span><span id="median"></span><span id="MEDIAN"></span>**Медиана** (5)


</dt> <dd>

Метрика сообщает медиану значений базовых метрик.

</dd> <dt>

<span id="Mode"></span><span id="mode"></span><span id="MODE"></span>

<span id="Mode"></span><span id="mode"></span><span id="MODE"></span>**Режим** (6)


</dt> <dd>

Метрика сообщает об модальном значении базовых значений метрики.

</dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Поставщик зарезервирован** (32768.. 65535)


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

[**\_БАСЕМЕТРИКДЕФИНИТИОН CIM**](cim-basemetricdefinition.md)
</dt> </dl>

 

