---
description: Представляет аспекты определения метрики.
ms.assetid: 861a69f6-a3bf-4e18-a9c2-931632e3cccc
title: Класс Msvm_BaseMetricDefinition
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_BaseMetricDefinition
- Msvm_BaseMetricDefinition.InstanceID
- Msvm_BaseMetricDefinition.Caption
- Msvm_BaseMetricDefinition.Description
- Msvm_BaseMetricDefinition.ElementName
- Msvm_BaseMetricDefinition.Id
- Msvm_BaseMetricDefinition.Name
- Msvm_BaseMetricDefinition.DataType
- Msvm_BaseMetricDefinition.Calculable
- Msvm_BaseMetricDefinition.Units
- Msvm_BaseMetricDefinition.BreakdownDimensions
- Msvm_BaseMetricDefinition.IsContinuous
- Msvm_BaseMetricDefinition.ChangeType
- Msvm_BaseMetricDefinition.TimeScope
- Msvm_BaseMetricDefinition.GatheringType
- Msvm_BaseMetricDefinition.ProgrammaticUnits
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8d1edbd722e3bf87631371b5650576917a7cfb39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684630"
---
# <a name="msvm_basemetricdefinition-class"></a><span data-ttu-id="e957b-103">\_Класс мсвм басеметрикдефинитион</span><span class="sxs-lookup"><span data-stu-id="e957b-103">Msvm\_BaseMetricDefinition class</span></span>

<span data-ttu-id="e957b-104">Представляет аспекты определения метрики.</span><span class="sxs-lookup"><span data-stu-id="e957b-104">Represents the definition aspects of a metric.</span></span> <span data-ttu-id="e957b-105">Класс **мсвм \_ басеметрикдефинитион** должен быть связан с [**CIM \_ манажеделементс**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) , к которому он применяется.</span><span class="sxs-lookup"><span data-stu-id="e957b-105">The **Msvm\_BaseMetricDefinition** class should be associated with the [**CIM\_ManagedElements**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) to which it applies.</span></span>

<span data-ttu-id="e957b-106">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="e957b-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e957b-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e957b-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_BaseMetricDefinition : CIM_BaseMetricDefinition
{
  string  InstanceID;
  string  Caption;
  string  Description;
  string  ElementName;
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

## <a name="members"></a><span data-ttu-id="e957b-108">Члены</span><span class="sxs-lookup"><span data-stu-id="e957b-108">Members</span></span>

<span data-ttu-id="e957b-109">Класс **мсвм \_ басеметрикдефинитион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="e957b-109">The **Msvm\_BaseMetricDefinition** class has these types of members:</span></span>

-   [<span data-ttu-id="e957b-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="e957b-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e957b-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="e957b-111">Properties</span></span>

<span data-ttu-id="e957b-112">Класс **мсвм \_ басеметрикдефинитион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="e957b-112">The **Msvm\_BaseMetricDefinition** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e957b-113">**бреакдовндименсионс**</span><span class="sxs-lookup"><span data-stu-id="e957b-113">**BreakdownDimensions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e957b-114">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="e957b-114">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="e957b-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e957b-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e957b-116">Определяет одну или несколько строк, которые могут быть использованы для уточнения (разбиения) запросов к значениям метрики в определенном измерении.</span><span class="sxs-lookup"><span data-stu-id="e957b-116">Defines one or more strings that can be used to refine (break down) queries against the metric values along a certain dimension.</span></span> <span data-ttu-id="e957b-117">Примером является имя транзакции, позволяющее разделить итоговое значение всех транзакций на набор значений, по одному для каждого имени транзакции.</span><span class="sxs-lookup"><span data-stu-id="e957b-117">An example is a transaction name, allowing the break down of the total value for all transactions into a set of values, one for each transaction name.</span></span> <span data-ttu-id="e957b-118">Другими примерами могут быть имя системы приложений или группы пользователей.</span><span class="sxs-lookup"><span data-stu-id="e957b-118">Other examples might be application system or user group name.</span></span> <span data-ttu-id="e957b-119">Строки имеют свободный формат и должны быть осмысленными для конечных пользователей данных метрик.</span><span class="sxs-lookup"><span data-stu-id="e957b-119">The strings are free format and should be meaningful to the end users of the metric data.</span></span> <span data-ttu-id="e957b-120">Строки указывают, какие измерения разбиения поддерживаются для этого определения метрики базовым инструментарием.</span><span class="sxs-lookup"><span data-stu-id="e957b-120">The strings indicate which break down dimensions are supported for this metric definition, by the underlying instrumentation.</span></span> <span data-ttu-id="e957b-121">Это свойство наследуется от **CIM \_ басеметрикдефинитион**.</span><span class="sxs-lookup"><span data-stu-id="e957b-121">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span>

</dd> <dt>

<span data-ttu-id="e957b-122">**калкулабле**</span><span class="sxs-lookup"><span data-stu-id="e957b-122">**Calculable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e957b-123">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e957b-123">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e957b-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e957b-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e957b-125">Описывает характеристики метрики в целях выполнения вычислений.</span><span class="sxs-lookup"><span data-stu-id="e957b-125">Describes the characteristics of the metric for purposes of performing calculations.</span></span> <span data-ttu-id="e957b-126">Это свойство наследуется от **CIM \_ басеметрикдефинитион**.</span><span class="sxs-lookup"><span data-stu-id="e957b-126">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span> <span data-ttu-id="e957b-127">Это может быть **значение NULL** или одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="e957b-127">This may be **Null** or one of the following values.</span></span>



| <span data-ttu-id="e957b-128">Значение</span><span class="sxs-lookup"><span data-stu-id="e957b-128">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="e957b-129">Значение</span><span class="sxs-lookup"><span data-stu-id="e957b-129">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Non-calculable"></span><span id="non-calculable"></span><span id="NON-CALCULABLE"></span><dl> <span data-ttu-id="e957b-130"><dt>**Не калкулабле**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="e957b-130"><dt>**Non-calculable**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="e957b-131">Значение не может быть вычислено.</span><span class="sxs-lookup"><span data-stu-id="e957b-131">The value cannot be calculated.</span></span> <span data-ttu-id="e957b-132">Например, строка.</span><span class="sxs-lookup"><span data-stu-id="e957b-132">For example, a string.</span></span><br/>                                                                                                                                                                                                                                                                                                         |
| <span id="Summable"></span><span id="summable"></span><span id="SUMMABLE"></span><dl> <span data-ttu-id="e957b-133">С <dt>**суммированием**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="e957b-133"><dt>**Summable**</dt> <dt>2</dt></span></span> </dl>                         | <span data-ttu-id="e957b-134">Значение можно суммировать для нескольких экземпляров.</span><span class="sxs-lookup"><span data-stu-id="e957b-134">The value can be summed over many instances.</span></span> <span data-ttu-id="e957b-135">Например, если каждое задание резервного копирования является единицей работы и каждое задание создает резервную копию 27 000 файлов в среднем, то 100 задания резервного копирования обрабатывали 2 700 000 файлов.</span><span class="sxs-lookup"><span data-stu-id="e957b-135">For example, if each backup job is a unit of work, and each job backs up 27,000 files on average, then 100 backup jobs processed 2,700,000 files.</span></span><br/>                                                                                                                                                                 |
| <span id="Non-summable_"></span><span id="non-summable_"></span><span id="NON-SUMMABLE_"></span><dl> <span data-ttu-id="e957b-136"><dt> **Без суммирования**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="e957b-136"><dt>**Non-summable** </dt> <dt>3 </dt></span></span> </dl>    | <span data-ttu-id="e957b-137">Это значение не может быть суммировано для нескольких экземпляров.</span><span class="sxs-lookup"><span data-stu-id="e957b-137">This value cannot be summed over many instances.</span></span> <span data-ttu-id="e957b-138">Примером может быть метрика, которая измеряет длину очереди при поступлении задания на сервер.</span><span class="sxs-lookup"><span data-stu-id="e957b-138">An example would be a metric that measures the queue length when a job arrives at a server.</span></span> <span data-ttu-id="e957b-139">Если каждое задание является единицей работы и средняя длина очереди при поступлении каждого задания — 33, нет смысла говорить, что длина очереди для заданий 100 составляет 3300.</span><span class="sxs-lookup"><span data-stu-id="e957b-139">If each job is a unit of work, and the average queue length when each job arrives is 33, it does not make sense to say that the queue length for 100 jobs is 3300.</span></span> <span data-ttu-id="e957b-140">Имеет смысл сказать, что среднее значение равно 33.</span><span class="sxs-lookup"><span data-stu-id="e957b-140">It does make sense to say that the mean is 33.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="e957b-141">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="e957b-141">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e957b-142">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e957b-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e957b-143">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e957b-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e957b-144">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="e957b-144">A short description of the object.</span></span> <span data-ttu-id="e957b-145">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="e957b-145">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e957b-146">**ChangeType**</span><span class="sxs-lookup"><span data-stu-id="e957b-146">**ChangeType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e957b-147">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e957b-147">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e957b-148">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e957b-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e957b-149">Указывает, как изменяется значение метрики в виде типичных сочетаний атрибутов более мелких граней, таких как изменение направления, минимальное и максимальное значения, а также семантика упаковки.</span><span class="sxs-lookup"><span data-stu-id="e957b-149">Indicates how the metric value changes, in the form of typical combinations of finer grain attributes such as direction change, minimum and maximum values, and wrapping semantics.</span></span> <span data-ttu-id="e957b-150">Это свойство наследуется от **CIM \_ басеметрикдефинитион**.</span><span class="sxs-lookup"><span data-stu-id="e957b-150">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span>



| <span data-ttu-id="e957b-151">Значение</span><span class="sxs-lookup"><span data-stu-id="e957b-151">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="e957b-152">Значение</span><span class="sxs-lookup"><span data-stu-id="e957b-152">Meaning</span></span>                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="e957b-153"><dt>**Неизвестно**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e957b-153"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="e957b-154">Конструктору метрик не удалось определить **ChangeType.**</span><span class="sxs-lookup"><span data-stu-id="e957b-154">The metric designer did not qualify the **ChangeType.**.</span></span><br/>                                                                                                                              |
| <span id="N_A"></span><span id="n_a"></span><dl> <span data-ttu-id="e957b-155"><dt>**Н/д**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="e957b-155"><dt>**N/A**</dt> <dt>2</dt></span></span> </dl>                                                                                       | <span data-ttu-id="e957b-156">Если свойство **Continuous** имеет значение false, то **ChangeType** не имеет смысла и для него должно быть задано значение "н/д".</span><span class="sxs-lookup"><span data-stu-id="e957b-156">If the **IsContinuous** property is "false", **ChangeType** does not make sense and must be set to "N/A".</span></span><br/>                                                                             |
| <span id="Counter"></span><span id="counter"></span><span id="COUNTER"></span><dl> <span data-ttu-id="e957b-157"><dt>**Счетчик**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="e957b-157"><dt>**Counter**</dt> <dt>3</dt></span></span> </dl>                                                 | <span data-ttu-id="e957b-158">Метрика является метрикой счетчика.</span><span class="sxs-lookup"><span data-stu-id="e957b-158">The metric is a counter metric.</span></span> <span data-ttu-id="e957b-159">Они имеют неотрицательные целочисленные значения, которые увеличиваются до достижения максимального представимого числа, а затем заносятся в начало и увеличиваются с 0.</span><span class="sxs-lookup"><span data-stu-id="e957b-159">These have nonnegative integer values that increase until reaching the maximum representable number and then wrap around and start increasing from 0.</span></span><br/> |
| <span id="Gauge"></span><span id="gauge"></span><span id="GAUGE"></span><dl> <span data-ttu-id="e957b-160"><dt>**Датчик**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="e957b-160"><dt>**Gauge**</dt> <dt>4</dt></span></span> </dl>                                                         | <span data-ttu-id="e957b-161">Метрика — это метрика датчика.</span><span class="sxs-lookup"><span data-stu-id="e957b-161">The metric is a gauge metric.</span></span> <span data-ttu-id="e957b-162">Они имеют целые значения или числа с плавающей запятой, которые могут увеличиваться и уменьшаться произвольным образом.</span><span class="sxs-lookup"><span data-stu-id="e957b-162">These have integer or float values that can increase and decrease arbitrarily.</span></span><br/>                                                                          |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="e957b-163"><dt>**Зарезервировано 5 DMTF**</dt> <dt>.. 32767</dt></span><span class="sxs-lookup"><span data-stu-id="e957b-163"><dt>**DMTF Reserved**</dt> <dt>5..32767</dt></span></span> </dl>                  |                                                                                                                                                                                                  |
| <span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span><dl> <span data-ttu-id="e957b-164"><dt> **Поставщик зарезервирован**</dt> <dt>32768.. 65535</dt></span><span class="sxs-lookup"><span data-stu-id="e957b-164"><dt>**Vendor Reserved** </dt> <dt>32768..65535 </dt></span></span> </dl> | <span data-ttu-id="e957b-165">Поставщики могут расширить свойство **ChangeType** в диапазоне, зарезервированном поставщиком.</span><span class="sxs-lookup"><span data-stu-id="e957b-165">Vendors may extend the **ChangeType** property in the vendor reserved range.</span></span><br/>                                                                                                          |



 

</dd> <dt>

<span data-ttu-id="e957b-166">**DataType**</span><span class="sxs-lookup"><span data-stu-id="e957b-166">**DataType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e957b-167">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e957b-167">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e957b-168">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e957b-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e957b-169">Тип данных метрики.</span><span class="sxs-lookup"><span data-stu-id="e957b-169">The data type of the metric.</span></span> <span data-ttu-id="e957b-170">Это свойство наследуется от **CIM \_ басеметрикдефинитион**.</span><span class="sxs-lookup"><span data-stu-id="e957b-170">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span>

<dl> <dt>

<span data-ttu-id="e957b-171"><span id="boolean"></span><span id="BOOLEAN"></span>**логическое значение** (1)</span><span class="sxs-lookup"><span data-stu-id="e957b-171"><span id="boolean"></span><span id="BOOLEAN"></span>**boolean** (1)</span></span>
</dt> <dt>

<span data-ttu-id="e957b-172"><span id="char16"></span><span id="CHAR16"></span>**Char16** (2)</span><span class="sxs-lookup"><span data-stu-id="e957b-172"><span id="char16"></span><span id="CHAR16"></span>**char16** (2)</span></span>
</dt> <dt>

<span data-ttu-id="e957b-173"><span id="datetime"></span><span id="DATETIME"></span>**DateTime** (3)</span><span class="sxs-lookup"><span data-stu-id="e957b-173"><span id="datetime"></span><span id="DATETIME"></span>**datetime** (3)</span></span>
</dt> <dt>

<span data-ttu-id="e957b-174"><span id="real32"></span><span id="REAL32"></span>**real32** (4)</span><span class="sxs-lookup"><span data-stu-id="e957b-174"><span id="real32"></span><span id="REAL32"></span>**real32** (4)</span></span>
</dt> <dt>

<span data-ttu-id="e957b-175"><span id="real64"></span><span id="REAL64"></span>**real64** (5)</span><span class="sxs-lookup"><span data-stu-id="e957b-175"><span id="real64"></span><span id="REAL64"></span>**real64** (5)</span></span>
</dt> <dt>

<span data-ttu-id="e957b-176"><span id="sint16"></span><span id="SINT16"></span>**sint16** (6)</span><span class="sxs-lookup"><span data-stu-id="e957b-176"><span id="sint16"></span><span id="SINT16"></span>**sint16** (6)</span></span>
</dt> <dt>

<span data-ttu-id="e957b-177"><span id="sint32"></span><span id="SINT32"></span>**Sint32** (7)</span><span class="sxs-lookup"><span data-stu-id="e957b-177"><span id="sint32"></span><span id="SINT32"></span>**sint32** (7)</span></span>
</dt> <dt>

<span data-ttu-id="e957b-178"><span id="sint64"></span><span id="SINT64"></span>**sint64** (8)</span><span class="sxs-lookup"><span data-stu-id="e957b-178"><span id="sint64"></span><span id="SINT64"></span>**sint64** (8)</span></span>
</dt> <dt>

<span data-ttu-id="e957b-179"><span id="sint8"></span><span id="SINT8"></span>**sint8** (9)</span><span class="sxs-lookup"><span data-stu-id="e957b-179"><span id="sint8"></span><span id="SINT8"></span>**sint8** (9)</span></span>
</dt> <dt>

<span data-ttu-id="e957b-180"><span id="string"></span><span id="STRING"></span>**строка** (10)</span><span class="sxs-lookup"><span data-stu-id="e957b-180"><span id="string"></span><span id="STRING"></span>**string** (10)</span></span>
</dt> <dt>

<span data-ttu-id="e957b-181"><span id="uint16"></span><span id="UINT16"></span>**UInt16** (11)</span><span class="sxs-lookup"><span data-stu-id="e957b-181"><span id="uint16"></span><span id="UINT16"></span>**uint16** (11)</span></span>
</dt> <dt>

<span data-ttu-id="e957b-182"><span id="uint32"></span><span id="UINT32"></span>**UInt32** (12)</span><span class="sxs-lookup"><span data-stu-id="e957b-182"><span id="uint32"></span><span id="UINT32"></span>**uint32** (12)</span></span>
</dt> <dt>

<span data-ttu-id="e957b-183"><span id="uint64"></span><span id="UINT64"></span>**UInt64** (13)</span><span class="sxs-lookup"><span data-stu-id="e957b-183"><span id="uint64"></span><span id="UINT64"></span>**uint64** (13)</span></span>
</dt> <dt>

<span data-ttu-id="e957b-184"><span id="uint8_"></span><span id="UINT8_"></span>**Uint8** (14)</span><span class="sxs-lookup"><span data-stu-id="e957b-184"><span id="uint8_"></span><span id="UINT8_"></span>**uint8** (14 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e957b-185">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e957b-185">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e957b-186">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e957b-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e957b-187">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e957b-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e957b-188">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="e957b-188">A description of the object.</span></span> <span data-ttu-id="e957b-189">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="e957b-189">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e957b-190">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="e957b-190">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e957b-191">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e957b-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e957b-192">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e957b-192">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e957b-193">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="e957b-193">A display name for the object.</span></span> <span data-ttu-id="e957b-194">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="e957b-194">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e957b-195">**гасерингтипе**</span><span class="sxs-lookup"><span data-stu-id="e957b-195">**GatheringType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e957b-196">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e957b-196">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e957b-197">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e957b-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e957b-198">Указывает, как значения метрик собираются базовым инструментарием.</span><span class="sxs-lookup"><span data-stu-id="e957b-198">Indicates how the metric values are gathered by the underlying instrumentation.</span></span> <span data-ttu-id="e957b-199">Это позволяет клиентскому приложению выбрать правильную метрику для цели.</span><span class="sxs-lookup"><span data-stu-id="e957b-199">This allows the client application to choose the right metric for the purpose.</span></span> <span data-ttu-id="e957b-200">Это свойство наследуется от **CIM \_ басеметрикдефинитион**.</span><span class="sxs-lookup"><span data-stu-id="e957b-200">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span> <span data-ttu-id="e957b-201">Это может быть **значение NULL** или одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="e957b-201">This may be **Null** or one of the following values.</span></span>



| <span data-ttu-id="e957b-202">Значение</span><span class="sxs-lookup"><span data-stu-id="e957b-202">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="e957b-203">Значение</span><span class="sxs-lookup"><span data-stu-id="e957b-203">Meaning</span></span>                                                                                                                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="e957b-204"><dt>**Неизвестно**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e957b-204"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="e957b-205">Тип сбора данных неизвестен.</span><span class="sxs-lookup"><span data-stu-id="e957b-205">The gathering type is not known.</span></span><br/>                                                                                                                                                                                                                               |
| <span id="OnChange"></span><span id="onchange"></span><span id="ONCHANGE"></span><dl> <span data-ttu-id="e957b-206"><dt>**Изменение**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="e957b-206"><dt>**OnChange**</dt> <dt>2</dt></span></span> </dl>                                             | <span data-ttu-id="e957b-207">Значения метрик обновляются немедленно при изменении значений в измеренном ресурсе.</span><span class="sxs-lookup"><span data-stu-id="e957b-207">The metric values get updated immediately when the values inside of the measured resource change.</span></span><br/>                                                                                                                                                              |
| <span id="Periodic"></span><span id="periodic"></span><span id="PERIODIC"></span><dl> <span data-ttu-id="e957b-208"><dt>**Периодическое**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="e957b-208"><dt>**Periodic**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="e957b-209">Значения метрик обновляются периодически.</span><span class="sxs-lookup"><span data-stu-id="e957b-209">The metric values get updated periodically.</span></span> <span data-ttu-id="e957b-210">Например, для клиентского приложения значение метрики, которое применяется к текущему времени, будет отображаться как константа во время каждого интервала сбора, а затем будет переходить к новому значению в конце каждого интервала сбора.</span><span class="sxs-lookup"><span data-stu-id="e957b-210">For instance, to a client application, a metric value that applies to the current time will appear constant during each gathering interval, and then jumps to the new value at the end of each gathering interval.</span></span><br/> |
| <span id="OnRequest"></span><span id="onrequest"></span><span id="ONREQUEST"></span><dl> <span data-ttu-id="e957b-211"><dt>**Onrequest**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="e957b-211"><dt>**OnRequest**</dt> <dt>4</dt></span></span> </dl>                                         | <span data-ttu-id="e957b-212">Значение метрики определяется каждый раз, когда клиентское приложение считывает его.</span><span class="sxs-lookup"><span data-stu-id="e957b-212">The metric value is determined each time a client application reads it.</span></span><br/>                                                                                                                                                                                        |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="e957b-213"><dt>**Зарезервировано 5 DMTF**</dt> <dt>.. 32767</dt></span><span class="sxs-lookup"><span data-stu-id="e957b-213"><dt>**DMTF Reserved**</dt> <dt>5..32767</dt></span></span> </dl>                  |                                                                                                                                                                                                                                                                           |
| <span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span><dl> <span data-ttu-id="e957b-214"><dt> **Поставщик зарезервирован**</dt> <dt>32768.. 65535</dt></span><span class="sxs-lookup"><span data-stu-id="e957b-214"><dt>**Vendor Reserved** </dt> <dt>32768..65535 </dt></span></span> </dl> |                                                                                                                                                                                                                                                                           |



 

</dd> <dt>

<span data-ttu-id="e957b-215">**Id**</span><span class="sxs-lookup"><span data-stu-id="e957b-215">**Id**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e957b-216">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e957b-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e957b-217">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e957b-217">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e957b-218">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="e957b-218">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="e957b-219">Строка, однозначно идентифицирующая определение метрики.</span><span class="sxs-lookup"><span data-stu-id="e957b-219">A string that uniquely identifies the metric definition.</span></span> <span data-ttu-id="e957b-220">Это свойство наследуется от **CIM \_ басеметрикдефинитион**.</span><span class="sxs-lookup"><span data-stu-id="e957b-220">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span>

</dd> <dt>

<span data-ttu-id="e957b-221">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="e957b-221">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e957b-222">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e957b-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e957b-223">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e957b-223">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e957b-224">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="e957b-224">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="e957b-225">Строка, уникально идентифицирующая экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="e957b-225">A string that uniquely identifies an instance of this class.</span></span> <span data-ttu-id="e957b-226">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="e957b-226">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e957b-227">**IsContinuous**</span><span class="sxs-lookup"><span data-stu-id="e957b-227">**IsContinuous**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e957b-228">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="e957b-228">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e957b-229">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e957b-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e957b-230">Указывает, является ли значение метрики непрерывным или скалярным.</span><span class="sxs-lookup"><span data-stu-id="e957b-230">Indicates whether the metric value is continuous or scalar.</span></span> <span data-ttu-id="e957b-231">Метрики производительности являются примером непрерывной метрики.</span><span class="sxs-lookup"><span data-stu-id="e957b-231">Performance metrics are an example of a continuous metric.</span></span> <span data-ttu-id="e957b-232">Примеры скалярных метрик включают коды ошибок или операционные состояния.</span><span class="sxs-lookup"><span data-stu-id="e957b-232">Examples of scalar metrics include error codes or operational states.</span></span> <span data-ttu-id="e957b-233">Непрерывные метрики можно сравнивать с помощью отношения "больше чем".</span><span class="sxs-lookup"><span data-stu-id="e957b-233">Continuous metrics can be compared by using the "greater than" relation.</span></span> <span data-ttu-id="e957b-234">Это свойство наследуется от **CIM \_ басеметрикдефинитион**.</span><span class="sxs-lookup"><span data-stu-id="e957b-234">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span>

</dd> <dt>

<span data-ttu-id="e957b-235">**Name**</span><span class="sxs-lookup"><span data-stu-id="e957b-235">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e957b-236">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e957b-236">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e957b-237">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e957b-237">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e957b-238">Имя метрики.</span><span class="sxs-lookup"><span data-stu-id="e957b-238">The name of the metric.</span></span> <span data-ttu-id="e957b-239">Это свойство наследуется от **CIM \_ басеметрикдефинитион**.</span><span class="sxs-lookup"><span data-stu-id="e957b-239">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span>

</dd> <dt>

<span data-ttu-id="e957b-240">**программатикунитс**</span><span class="sxs-lookup"><span data-stu-id="e957b-240">**ProgrammaticUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e957b-241">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e957b-241">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e957b-242">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e957b-242">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e957b-243">Определяет конкретные единицы значения.</span><span class="sxs-lookup"><span data-stu-id="e957b-243">Identifies the specific units of a value.</span></span> <span data-ttu-id="e957b-244">Значением этого свойства будет допустимое значение квалификатора программных единиц, как определено в приложении C. 1 [DSP0004 v 2.4](https://www.dmtf.org/sites/default/files/standards/documents/DSP0004_2.5.0.pdf) или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="e957b-244">The value of this property will be a legal value of the Programmatic Units qualifier as defined in Appendix C.1 of [DSP0004 V2.4](https://www.dmtf.org/sites/default/files/standards/documents/DSP0004_2.5.0.pdf) or later.</span></span> <span data-ttu-id="e957b-245">Это свойство наследуется от **CIM \_ басеметрикдефинитион**.</span><span class="sxs-lookup"><span data-stu-id="e957b-245">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span>

</dd> <dt>

<span data-ttu-id="e957b-246">**тимескопе**</span><span class="sxs-lookup"><span data-stu-id="e957b-246">**TimeScope**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e957b-247">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e957b-247">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e957b-248">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e957b-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e957b-249">Указывает область времени, к которой применяется значение метрики.</span><span class="sxs-lookup"><span data-stu-id="e957b-249">Indicates the time scope to which the metric value applies.</span></span> <span data-ttu-id="e957b-250">Это свойство наследуется от **CIM \_ басеметрикдефинитион**.</span><span class="sxs-lookup"><span data-stu-id="e957b-250">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span>



| <span data-ttu-id="e957b-251">Значение</span><span class="sxs-lookup"><span data-stu-id="e957b-251">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="e957b-252">Значение</span><span class="sxs-lookup"><span data-stu-id="e957b-252">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="e957b-253"><dt>**Неизвестно**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e957b-253"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="e957b-254">Область времени не определена конструктором метрик или неизвестна поставщику.</span><span class="sxs-lookup"><span data-stu-id="e957b-254">The time scope was not qualified by the metric designer or is unknown to the provider.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="Point"></span><span id="point"></span><span id="POINT"></span><dl> <span data-ttu-id="e957b-255"><dt>**Точка**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="e957b-255"><dt>**Point**</dt> <dt>2</dt></span></span> </dl>                                                         | <span data-ttu-id="e957b-256">Метрика применяется к моменту времени.</span><span class="sxs-lookup"><span data-stu-id="e957b-256">The metric applies to a point in time.</span></span> <span data-ttu-id="e957b-257">В соответствующих экземплярах [**мсвм \_ Басеметриквалуе**](msvm-basemetricvalue.md) свойство **timestamp** указывает момент времени, а свойство **Duration** всегда равно 0.</span><span class="sxs-lookup"><span data-stu-id="e957b-257">On the corresponding [**Msvm\_BaseMetricValue**](msvm-basemetricvalue.md) instances, the **TimeStamp** property specifies the point in time, and the **Duration** property is always 0.</span></span><br/>                                                                                                                                                                                                                                                                                              |
| <span id="Interval"></span><span id="interval"></span><span id="INTERVAL"></span><dl> <span data-ttu-id="e957b-258"><dt>**Интервал**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="e957b-258"><dt>**Interval**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="e957b-259">Метрика применяется к интервалу времени.</span><span class="sxs-lookup"><span data-stu-id="e957b-259">The metric applies to a time interval.</span></span> <span data-ttu-id="e957b-260">В соответствующих экземплярах [**мсвм \_ Басеметриквалуе**](msvm-basemetricvalue.md) свойство **timestamp** указывает конец интервала времени, а свойство **Duration** указывает его длительность.</span><span class="sxs-lookup"><span data-stu-id="e957b-260">On the corresponding [**Msvm\_BaseMetricValue**](msvm-basemetricvalue.md) instances, the **TimeStamp** property specifies the end of the time interval, and the **Duration** property specifies its duration.</span></span><br/>                                                                                                                                                                                                                                                                        |
| <span id="StartupInterval"></span><span id="startupinterval"></span><span id="STARTUPINTERVAL"></span><dl> <span data-ttu-id="e957b-261"><dt>**Стартупинтервал**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="e957b-261"><dt>**StartupInterval**</dt> <dt>4</dt></span></span> </dl>                 | <span data-ttu-id="e957b-262">Метрика применяется к интервалу времени, который начался при запуске измеряемого ресурса (то есть Манажеделемент, связанном с Метрикдефформе).</span><span class="sxs-lookup"><span data-stu-id="e957b-262">The metric applies to a time interval that began at the startup of the measured resource (that is, the ManagedElement associated by MetricDefForMe).</span></span> <span data-ttu-id="e957b-263">В соответствующих экземплярах [**мсвм \_ Басеметриквалуе**](msvm-basemetricvalue.md) свойство **timestamp** указывает конец интервала времени.</span><span class="sxs-lookup"><span data-stu-id="e957b-263">On the corresponding [**Msvm\_BaseMetricValue**](msvm-basemetricvalue.md) instances, the **TimeStamp** property specifies the end of the time interval.</span></span> <span data-ttu-id="e957b-264">Если свойство **Duration** равно 0, это означает, что время запуска измеряемого ресурса неизвестно.</span><span class="sxs-lookup"><span data-stu-id="e957b-264">If the **Duration** property is 0, this indicates that the startup time of the measured resource is unknown.</span></span> <span data-ttu-id="e957b-265">В противном случае **Длительность** указывает длительность между запуском ресурса и **меткой времени**.</span><span class="sxs-lookup"><span data-stu-id="e957b-265">Otherwise, **Duration** specifies the duration between startup of the resource and **TimeStamp**.</span></span><br/> |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="e957b-266"><dt>**Зарезервировано 5 DMTF**</dt> <dt>.. 32767</dt></span><span class="sxs-lookup"><span data-stu-id="e957b-266"><dt>**DMTF Reserved**</dt> <dt>5..32767</dt></span></span> </dl>                  |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span><dl> <span data-ttu-id="e957b-267"><dt> **Поставщик зарезервирован**</dt> <dt>32768.. 65535</dt></span><span class="sxs-lookup"><span data-stu-id="e957b-267"><dt>**Vendor Reserved** </dt> <dt>32768..65535 </dt></span></span> </dl> |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

</dd> <dt>

<span data-ttu-id="e957b-268">**единиц(ы)**</span><span class="sxs-lookup"><span data-stu-id="e957b-268">**Units**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e957b-269">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e957b-269">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e957b-270">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e957b-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e957b-271">Определяет конкретные единицы значения, например "мегабайты".</span><span class="sxs-lookup"><span data-stu-id="e957b-271">Identifies the specific units of a value, for example, "megabytes".</span></span> <span data-ttu-id="e957b-272">Это свойство наследуется от **CIM \_ басеметрикдефинитион**.</span><span class="sxs-lookup"><span data-stu-id="e957b-272">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e957b-273">Требования</span><span class="sxs-lookup"><span data-stu-id="e957b-273">Requirements</span></span>



| <span data-ttu-id="e957b-274">Требование</span><span class="sxs-lookup"><span data-stu-id="e957b-274">Requirement</span></span> | <span data-ttu-id="e957b-275">Значение</span><span class="sxs-lookup"><span data-stu-id="e957b-275">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e957b-276">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e957b-276">Minimum supported client</span></span><br/> | <span data-ttu-id="e957b-277">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="e957b-277">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="e957b-278">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e957b-278">Minimum supported server</span></span><br/> | <span data-ttu-id="e957b-279">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="e957b-279">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e957b-280">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e957b-280">Namespace</span></span><br/>                | <span data-ttu-id="e957b-281">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="e957b-281">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="e957b-282">MOF</span><span class="sxs-lookup"><span data-stu-id="e957b-282">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e957b-283"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e957b-283"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e957b-284">DLL</span><span class="sxs-lookup"><span data-stu-id="e957b-284">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e957b-285"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e957b-285"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

