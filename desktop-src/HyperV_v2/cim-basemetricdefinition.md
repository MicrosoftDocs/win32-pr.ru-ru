---
description: Представляет определение метрики, содержащее метаданные для \_ объекта МЕТРИЦИНСТАНЦЕ CIM.
ms.assetid: 6abfb0dc-e80b-4ca6-89d9-2e43283d0abe
title: Класс CIM_BaseMetricDefinition
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BaseMetricDefinition
- CIM_BaseMetricDefinition.Id
- CIM_BaseMetricDefinition.Name
- CIM_BaseMetricDefinition.DataType
- CIM_BaseMetricDefinition.Calculable
- CIM_BaseMetricDefinition.Units
- CIM_BaseMetricDefinition.BreakdownDimensions
- CIM_BaseMetricDefinition.IsContinuous
- CIM_BaseMetricDefinition.ChangeType
- CIM_BaseMetricDefinition.TimeScope
- CIM_BaseMetricDefinition.GatheringType
- CIM_BaseMetricDefinition.ProgrammaticUnits
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0614b14f3033da5cf97dfb293f0e9cc130025dbb534331f8ec3386513d8796c6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829724"
---
# <a name="cim_basemetricdefinition-class"></a>\_Класс CIM басеметрикдефинитион

Представляет определение метрики, содержащее метаданные для объекта **\_ метриЦинстанце CIM** .

## <a name="syntax"></a>Синтаксис

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Metrics::BaseMetric"), AMENDMENT]
class CIM_BaseMetricDefinition : CIM_ManagedElement
{
  string  Id;
  string  Name;
  uint16  DataType;
  uint16  Calculable;
  string  Units;
  string  BreakdownDimensions[];
  boolean IsContinuous;
  uint16  ChangeType;
  uint16  TimeScope;
  uint16  GatheringType;
  string  ProgrammaticUnits;
};
```

## <a name="members"></a>Члены

Класс **CIM \_ басеметрикдефинитион** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **CIM \_ басеметрикдефинитион** имеет следующие свойства.

<dl> <dt>

**бреакдовндименсионс**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Массив, содержащий строки бесплатных форматов, которые можно использовать для разбиения запросов объектов [**CIM \_ басеметриквалуе**](cim-basemetricvalue.md) на определенное измерение. Строки должны быть осмысленными для конечных пользователей данных метрики. Кроме того, строки должны указывать, какие измерения разбиения поддерживаются для определения метрики базовым инструментарием.

В качестве примера можно привести имя транзакции, которое позволяет разбить общее значение всех транзакций на набор значений, по одному для каждого имени транзакции. Другими примерами являются система приложений или имя группы пользователей.

</dd> <dt>

**калкулабле**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Характеристики метрики, используемые для выполнения вычислений.

<dt>

<span id="Non-calculable"></span><span id="non-calculable"></span><span id="NON-CALCULABLE"></span>

<span id="Non-calculable"></span><span id="non-calculable"></span><span id="NON-CALCULABLE"></span>**Не калкулабле** (1)


</dt> <dd>

Строка. Арифметические действия не имеют смысла.

</dd> <dt>

<span id="Summable"></span><span id="summable"></span><span id="SUMMABLE"></span>

<span id="Summable"></span><span id="summable"></span><span id="SUMMABLE"></span>**Подведем** (2)


</dt> <dd>

Разумно суммировать это значение для нескольких экземпляров, например, Унитофворк, например количество файлов, обработанных в задании резервного копирования. Например, если каждое задание резервного копирования является Унитофворк, а каждое задание выполняет резервное копирование 27 000 файлов в среднем, то имеет смысл сказать, что задания резервного копирования 100 обрабатывали 2 700 000 файлов.

</dd> <dt>

<span id="Non-summable"></span><span id="non-summable"></span><span id="NON-SUMMABLE"></span>

<span id="Non-summable"></span><span id="non-summable"></span><span id="NON-SUMMABLE"></span>**Без суммирования** (3)


</dt> <dd>

Не имеет смысла суммировать это значение для многих экземпляров Унитофворк. Примером может быть метрика, которая измеряет длину очереди при поступлении задания на сервер. Если каждое задание является Унитофворк, а средняя длина очереди при поступлении каждого задания — 33, нет смысла говорить, что длина очереди для заданий 100 составляет 3300. Имеет смысл сказать, что среднее значение равно 33.

</dd> </dl>

</dd> <dt>

**ChangeType**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ басеметрикдефинитион**.**Continuous**»)
</dt> </dl>

Указывает, как изменяется значение метрики с помощью общих атрибутов, таких как изменение направления, минимальное и максимальное значения, а также семантика упаковки.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)


</dt> <dd>

Конструктору метрик не удалось определить ChangeType.

</dd> <dt>

<span id="N_A"></span><span id="n_a"></span>

<span id="N_A"></span><span id="n_a"></span>**Н/д** (2)


</dt> <dd>

Если свойство "Continuous" имеет значение "false", то ChangeType не имеет смысла и для него должно быть задано значение "н/д".

</dd> <dt>

<span id="Counter"></span><span id="counter"></span><span id="COUNTER"></span>

<span id="Counter"></span><span id="counter"></span><span id="COUNTER"></span>**Счетчик** (3)


</dt> <dd>

Метрика является метрикой счетчика. Они имеют неотрицательные целочисленные значения, которые увеличиваются монотонно до достижения максимального допустимого числа, а затем заносятся в начало и начинают увеличиваться с 0. Такие счетчики, также называемые счетчиками смены, могут быть использованы для экземпляра для подсчета числа ошибок сети или количества обработанных транзакций. Единственным способом, с помощью которого клиентское приложение отслеживает заключение, является получение значения счетчика в соответствующие короткие интервалы.

</dd> <dt>

<span id="Gauge"></span><span id="gauge"></span><span id="GAUGE"></span>

<span id="Gauge"></span><span id="gauge"></span><span id="GAUGE"></span>**Датчик** (4)


</dt> <dd>

Метрика — это метрика датчика. Они имеют целые значения или числа с плавающей запятой, которые могут увеличиваться и уменьшаться произвольным образом. Индикатор не должен переноситься при достижении минимального или максимального допустимого числа, вместо этого значение "фиксируется" в этом номере. Минимальное или максимальное значение в диапазоне представимых значений, в котором Метрика может быть определена как "число".

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (5.. 32767)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Поставщик зарезервирован** (32768.. 65535)


</dt> <dd></dd> </dl>

</dd> <dt>

**DataType**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Тип данных метрики.

<dt>

<span id="boolean"></span><span id="BOOLEAN"></span>

**логическое значение** (1)


</dt> <dd></dd> <dt>

<span id="char16"></span><span id="CHAR16"></span>

**Char16** (2)


</dt> <dd></dd> <dt>

<span id="datetime"></span><span id="DATETIME"></span>

**DateTime** (3)


</dt> <dd></dd> <dt>

<span id="real32"></span><span id="REAL32"></span>

**real32** (4)


</dt> <dd></dd> <dt>

<span id="real64"></span><span id="REAL64"></span>

**real64** (5)


</dt> <dd></dd> <dt>

<span id="sint16"></span><span id="SINT16"></span>

**sint16** (6)


</dt> <dd></dd> <dt>

<span id="sint32"></span><span id="SINT32"></span>

**Sint32** (7)


</dt> <dd></dd> <dt>

<span id="sint64"></span><span id="SINT64"></span>

**sint64** (8)


</dt> <dd></dd> <dt>

<span id="sint8"></span><span id="SINT8"></span>

**sint8** (9)


</dt> <dd></dd> <dt>

<span id="string"></span><span id="STRING"></span>

**строка** (10)


</dt> <dd></dd> <dt>

<span id="uint16"></span><span id="UINT16"></span>

**UInt16** (11)


</dt> <dd></dd> <dt>

<span id="uint32"></span><span id="UINT32"></span>

**UInt32** (12)


</dt> <dd></dd> <dt>

<span id="uint64"></span><span id="UINT64"></span>

**UInt64** (13)


</dt> <dd></dd> <dt>

<span id="uint8"></span><span id="UINT8"></span>

**Uint8** (14)


</dt> <dd></dd> </dl>

</dd> <dt>

**гасерингтипе**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, как значения метрик собираются базовым инструментарием.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)


</dt> <dd>

Указывает, что Гасерингтипе неизвестен.

</dd> <dt>

<span id="OnChange"></span><span id="onchange"></span><span id="ONCHANGE"></span>

<span id="OnChange"></span><span id="onchange"></span><span id="ONCHANGE"></span>**OnChange** (2)


</dt> <dd>

Указывает, что значения метрик CIM обновляются немедленно при изменении значений в измеренном ресурсе. Значения метрик OnChange действительно отражать текущую ситуацию в ресурсе в любое время. Например, число вошедших в систему пользователей, которые немедленно обновляются по мере входа и отключения пользователей.

</dd> <dt>

<span id="Periodic"></span><span id="periodic"></span><span id="PERIODIC"></span>

<span id="Periodic"></span><span id="periodic"></span><span id="PERIODIC"></span>**Периодические** (3)


</dt> <dd>

": Указывает, что значения метрик CIM обновляются периодически. Например, для клиентского приложения значение метрики, применяемое к текущему времени, будет отображаться как константа во время каждого интервала сбора, а затем будет переходить к новому значению в конце каждого интервала сбора.

</dd> <dt>

<span id="OnRequest"></span><span id="onrequest"></span><span id="ONREQUEST"></span>

<span id="OnRequest"></span><span id="onrequest"></span><span id="ONREQUEST"></span>**Onrequest** (4)


</dt> <dd>

Указывает, что значение метрики CIM определяется каждый раз, когда клиентское приложение считывает его. Значения метрик onrequest действительно возвращают текущую ситуацию в ресурсе, если кто – то запрашивает его. Однако они не изменяют "ненаблюдаемые", поэтому не рекомендуется подписываться на изменения значений метрик onrequest.

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (5.. 32767)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Поставщик зарезервирован** (32768.. 65535)


</dt> <dd></dd> </dl>

</dd> <dt>

**Id**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Уникальный идентификатор определения метрики. Рекомендуется использовать идентификаторы UUID и GUID Open Software Foundation (использование).

</dd> <dt>

**IsContinuous**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Значение true, если метрика непрерывная; в противном случае — значение false.

</dd> <dt>

**Имя**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Имя метрики. Это имя может быть уникальным, но оно должно быть описательным и содержать пробелы.

</dd> <dt>

**программатикунитс**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Конкретные единицы значения. Значение этого свойства должно быть допустимым значением квалификатора программных единиц, как определено в приложении C. 1 DSP0004 V 2.4 или более поздней версии.

</dd> <dt>

**тимескопе**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ басеметриквалуе**](cim-basemetricvalue.md).**TimeStamp**","**CIM \_ басеметриквалуе**.**Duration (длительность**))
</dt> </dl>

Область времени, которая применяется к конструктору метрик.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)


</dt> <dd>

Указывает, что область времени не определена конструктором метрик или неизвестна поставщику.

</dd> <dt>

<span id="Point"></span><span id="point"></span><span id="POINT"></span>

<span id="Point"></span><span id="point"></span><span id="POINT"></span>**Точка** (2)


</dt> <dd>

Указывает, что метрика относится к моменту времени. В соответствующих экземплярах Басеметриквалуе метка времени указывает на момент времени, а длительность всегда равна 0.

</dd> <dt>

<span id="Interval"></span><span id="interval"></span><span id="INTERVAL"></span>

<span id="Interval"></span><span id="interval"></span><span id="INTERVAL"></span>**Интервал** (3)


</dt> <dd>

Указывает, что метрика применяется к интервалу времени. В соответствующих экземплярах Басеметриквалуе метка времени указывает конец интервала времени, а длительность задает его длительность.

</dd> <dt>

<span id="StartupInterval"></span><span id="startupinterval"></span><span id="STARTUPINTERVAL"></span>

<span id="StartupInterval"></span><span id="startupinterval"></span><span id="STARTUPINTERVAL"></span>**Стартупинтервал** (4)


</dt> <dd>

Указывает, что метрика применяется к интервалу времени, который начался при запуске измеряемого ресурса (т. е. Манажеделемент, связанном с Метрикдефформе). В соответствующих экземплярах Басеметриквалуе метка времени указывает конец интервала времени. Если значение Duration равно 0, это означает, что время запуска измеряемого ресурса неизвестно. В противном случае длительность указывает длительность между запуском ресурса и меткой времени.

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (5.. 32767)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Поставщик зарезервирован** (32768.. 65535)


</dt> <dd></dd> </dl>

</dd> <dt>

**единиц(ы)**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Единицы измерения метрики. Примерами могут быть байты, пакеты, задания, файлы, миллисекунды и ампер.

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

[**\_МАНАЖЕДЕЛЕМЕНТ CIM**](cim-managedelement.md)
</dt> </dl>

 

