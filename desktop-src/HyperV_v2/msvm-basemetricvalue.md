---
description: Представляет значение метрики, определенное экземпляром \_ класса мсвм басеметрикдефинитион.
ms.assetid: bd872f21-ab71-4ab7-88d3-b26dd2fbdbe5
title: Класс Msvm_BaseMetricValue
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_BaseMetricValue
- Msvm_BaseMetricValue.InstanceID
- Msvm_BaseMetricValue.Caption
- Msvm_BaseMetricValue.Description
- Msvm_BaseMetricValue.ElementName
- Msvm_BaseMetricValue.MetricDefinitionId
- Msvm_BaseMetricValue.MeasuredElementName
- Msvm_BaseMetricValue.TimeStamp
- Msvm_BaseMetricValue.Duration
- Msvm_BaseMetricValue.MetricValue
- Msvm_BaseMetricValue.BreakdownDimension
- Msvm_BaseMetricValue.BreakdownValue
- Msvm_BaseMetricValue.Volatile
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 24d61f6068cffc83f8556637bba30de57308b6a5bcefe5b015bc185ab7811108
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119790224"
---
# <a name="msvm_basemetricvalue-class"></a>\_Класс мсвм басеметриквалуе

Представляет значение метрики, определенное экземпляром класса [**мсвм \_ басеметрикдефинитион**](msvm-basemetricdefinition.md) .

Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_BaseMetricValue : CIM_BaseMetricValue
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
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ басеметриквалуе** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **мсвм \_ басеметриквалуе** имеет следующие свойства.

<dl> <dt>

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

**Caption**
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

**Переменный**
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
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                                              |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                                    |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

