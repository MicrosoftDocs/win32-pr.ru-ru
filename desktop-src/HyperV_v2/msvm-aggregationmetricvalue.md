---
description: Представляет значение экземпляра метрики, определенной экземпляром \_ класса мсвм аггрегатионметрикдефинитион.
ms.assetid: 6dfcb711-6137-492a-aff4-82facbd11949
title: Класс Msvm_AggregationMetricValue
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_AggregationMetricValue
- Msvm_AggregationMetricValue.InstanceID
- Msvm_AggregationMetricValue.Caption
- Msvm_AggregationMetricValue.Description
- Msvm_AggregationMetricValue.ElementName
- Msvm_AggregationMetricValue.MetricDefinitionId
- Msvm_AggregationMetricValue.MeasuredElementName
- Msvm_AggregationMetricValue.TimeStamp
- Msvm_AggregationMetricValue.Duration
- Msvm_AggregationMetricValue.MetricValue
- Msvm_AggregationMetricValue.BreakdownDimension
- Msvm_AggregationMetricValue.BreakdownValue
- Msvm_AggregationMetricValue.Volatile
- Msvm_AggregationMetricValue.AggregationTimeStamp
- Msvm_AggregationMetricValue.AggregationDuration
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f6842e5a23fbbf7cf1d639862cf5b9737bc1ff96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081237"
---
# <a name="msvm_aggregationmetricvalue-class"></a>\_Класс мсвм аггрегатионметриквалуе

Представляет значение экземпляра метрики, определенной экземпляром класса [**мсвм \_ аггрегатионметрикдефинитион**](msvm-aggregationmetricdefinition.md) . Свойства, наследуемые от [**мсвм \_ басеметриквалуе**](msvm-basemetricvalue.md) , предоставляют фактическое значение метрики. Свойства, определенные этим классом, предоставляют сведения о интервале, через который была применена статистическая функция.

Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_AggregationMetricValue : CIM_AggregationMetricValue
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  string   MetricDefinitionId;
  string   MeasuredElementName;
  datetime TimeStamp;
  datetime Duration;
  string   MetricValue;
  string   BreakdownDimension;
  string   BreakdownValue;
  boolean  Volatile;
  datetime AggregationTimeStamp;
  datetime AggregationDuration;
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ аггрегатионметриквалуе** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **мсвм \_ аггрегатионметриквалуе** имеет следующие свойства.

<dl> <dt>

**аггрегатиондуратион**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Представляет период времени, в течение которого Вычисление агрегата было выполнено. Начало интервала мониторинга, по отношению к которому применяется статистическая функция, определяется путем вычитания **аггрегатиондуратион** из **аггрегатионтиместамп**. Это свойство наследуется от **CIM \_ аггрегатионметриквалуе**.

</dd> <dt>

**аггрегатионтиместамп**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Определяет время, когда статистическая функция была применена для определения значения экземпляра метрики. Это не то же самое, что и время создания экземпляра. Для данного экземпляра **CIM \_ аггрегатионметриквалуе** **аггрегатионтиместамп** изменяется при применении статистической функции к вычислению значения. Это свойство наследуется от **CIM \_ аггрегатионметриквалуе**.

</dd> <dt>

**бреакдовндименсион**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает одно измерение декомпозиции из массива **бреакдовндименсионс** , определенного в связанном [**мсвм \_ басеметрикдефинитион**](msvm-basemetricdefinition.md). Это измерение, в котором этот набор значений метрик разбит на части. Это свойство наследуется от [**CIM \_ басеметрикдефинитион**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**бреакдовнвалуе**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Определяет значение свойства **бреакдовндименсион** , определенного для данного экземпляра значения метрики. Например, если **бреакдовндименсион** имеет значение "трансактионнаме", это свойство может наименовать фактическую транзакцию, к которой применяется это конкретное метрика. Это свойство наследуется от [**CIM \_ басеметрикдефинитион**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**Заголовок**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Краткое описание объекта. Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**Описание**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Описание объекта. Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**Длительность**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает период времени, в течение которого это значение метрики является допустимым. Это свойство не должно существовать для меток времени, которые применяются только к моменту времени, но должны быть указаны для значений, которые считаются допустимыми в течение определенного периода времени (например, выборка). Если свойство **Duration** существует и не равно **null**, свойство **timestamp** задает конец интервала. Это свойство наследуется от [**CIM \_ басеметрикдефинитион**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Отображаемое имя объекта. Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **ключ**
</dt> </dl>

Строка, уникально идентифицирующая экземпляр этого класса. Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**меасуределементнаме**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Описательное имя элемента, которому принадлежит значение метрики (измеряемый элемент). Это свойство наследуется от [**CIM \_ басеметрикдефинитион**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**метрикдефинитионид**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Ключ экземпляра [**\_ басеметрикдефинитион мсвм**](msvm-basemetricdefinition.md) для этого значения. Это свойство наследуется от [**CIM \_ басеметрикдефинитион**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**метриквалуе**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Значение метрики, представленное в виде строки. Это свойство наследуется от [**CIM \_ басеметрикдефинитион**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**TimeStamp**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает время, когда значение метрики было перехвачено или вычислено. Имейте в виду, что это отличается от времени создания экземпляра. Это свойство наследуется от [**CIM \_ басеметрикдефинитион**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**Независимо**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Значение **true** , если значение для следующего момента времени будет использовать один и тот же экземпляр класса и просто изменить значения свойств (например, **значение** или **метку времени**). Если **значение — true**, экземпляр используется повторно. Если **значение равно false**, существующие экземпляры остаются неизменными и создается новый экземпляр для нового момента времени. Это свойство наследуется от [**CIM \_ басеметрикдефинитион**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                                              |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                                    |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

