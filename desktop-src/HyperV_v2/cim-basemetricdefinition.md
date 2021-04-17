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
ms.openlocfilehash: cac965ed1eae59f1c269d897a12e9aa116183eb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664689"
---
# <a name="cim_basemetricdefinition-class"></a><span data-ttu-id="41c3a-103">\_Класс CIM басеметрикдефинитион</span><span class="sxs-lookup"><span data-stu-id="41c3a-103">CIM\_BaseMetricDefinition class</span></span>

<span data-ttu-id="41c3a-104">Представляет определение метрики, содержащее метаданные для объекта **\_ метриЦинстанце CIM** .</span><span class="sxs-lookup"><span data-stu-id="41c3a-104">Represents a metric definition that contains the meta data for a **CIM\_MetricInstance** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="41c3a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="41c3a-105">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="41c3a-106">Члены</span><span class="sxs-lookup"><span data-stu-id="41c3a-106">Members</span></span>

<span data-ttu-id="41c3a-107">Класс **CIM \_ басеметрикдефинитион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="41c3a-107">The **CIM\_BaseMetricDefinition** class has these types of members:</span></span>

-   [<span data-ttu-id="41c3a-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="41c3a-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="41c3a-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="41c3a-109">Properties</span></span>

<span data-ttu-id="41c3a-110">Класс **CIM \_ басеметрикдефинитион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="41c3a-110">The **CIM\_BaseMetricDefinition** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="41c3a-111">**бреакдовндименсионс**</span><span class="sxs-lookup"><span data-stu-id="41c3a-111">**BreakdownDimensions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c3a-112">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="41c3a-112">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="41c3a-113">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="41c3a-113">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41c3a-114">Массив, содержащий строки бесплатных форматов, которые можно использовать для разбиения запросов объектов [**CIM \_ басеметриквалуе**](cim-basemetricvalue.md) на определенное измерение.</span><span class="sxs-lookup"><span data-stu-id="41c3a-114">An array that contains free format strings that can be used to break down queries of [**CIM\_BaseMetricValue**](cim-basemetricvalue.md) objects along a certain dimension.</span></span> <span data-ttu-id="41c3a-115">Строки должны быть осмысленными для конечных пользователей данных метрики.</span><span class="sxs-lookup"><span data-stu-id="41c3a-115">The strings should be meaningful to the end users of the metric data.</span></span> <span data-ttu-id="41c3a-116">Кроме того, строки должны указывать, какие измерения разбиения поддерживаются для определения метрики базовым инструментарием.</span><span class="sxs-lookup"><span data-stu-id="41c3a-116">In addition, the strings should indicate which break down dimensions are supported for the metric definition, by the underlying instrumentation.</span></span>

<span data-ttu-id="41c3a-117">В качестве примера можно привести имя транзакции, которое позволяет разбить общее значение всех транзакций на набор значений, по одному для каждого имени транзакции.</span><span class="sxs-lookup"><span data-stu-id="41c3a-117">An example is a transaction name that allows the break down of the total value for all transactions into a set of values, one for each transaction name.</span></span> <span data-ttu-id="41c3a-118">Другими примерами являются система приложений или имя группы пользователей.</span><span class="sxs-lookup"><span data-stu-id="41c3a-118">Other examples are an application system, or a user group name.</span></span>

</dd> <dt>

<span data-ttu-id="41c3a-119">**калкулабле**</span><span class="sxs-lookup"><span data-stu-id="41c3a-119">**Calculable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c3a-120">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="41c3a-120">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="41c3a-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="41c3a-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41c3a-122">Характеристики метрики, используемые для выполнения вычислений.</span><span class="sxs-lookup"><span data-stu-id="41c3a-122">The characteristics of the metric used to perform calculations.</span></span>

<dt>

<span id="Non-calculable"></span><span id="non-calculable"></span><span id="NON-CALCULABLE"></span>

<span data-ttu-id="41c3a-123"><span id="Non-calculable"></span><span id="non-calculable"></span><span id="NON-CALCULABLE"></span>**Не калкулабле** (1)</span><span class="sxs-lookup"><span data-stu-id="41c3a-123"><span id="Non-calculable"></span><span id="non-calculable"></span><span id="NON-CALCULABLE"></span>**Non-calculable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="41c3a-124">Строка.</span><span class="sxs-lookup"><span data-stu-id="41c3a-124">A string.</span></span> <span data-ttu-id="41c3a-125">Арифметические действия не имеют смысла.</span><span class="sxs-lookup"><span data-stu-id="41c3a-125">Arithmetic makes no sense.</span></span>

</dd> <dt>

<span id="Summable"></span><span id="summable"></span><span id="SUMMABLE"></span>

<span data-ttu-id="41c3a-126"><span id="Summable"></span><span id="summable"></span><span id="SUMMABLE"></span>**Подведем** (2)</span><span class="sxs-lookup"><span data-stu-id="41c3a-126"><span id="Summable"></span><span id="summable"></span><span id="SUMMABLE"></span>**Summable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="41c3a-127">Разумно суммировать это значение для нескольких экземпляров, например, Унитофворк, например количество файлов, обработанных в задании резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="41c3a-127">It is reasonable to sum this value over many instances of e.g., UnitOfWork, such as the number of files processed in a backup job.</span></span> <span data-ttu-id="41c3a-128">Например, если каждое задание резервного копирования является Унитофворк, а каждое задание выполняет резервное копирование 27 000 файлов в среднем, то имеет смысл сказать, что задания резервного копирования 100 обрабатывали 2 700 000 файлов.</span><span class="sxs-lookup"><span data-stu-id="41c3a-128">For example, if each backup job is a UnitOfWork, and each job backs up 27,000 files on average, then it makes sense to say that 100 backup jobs processed 2,700,000 files.</span></span>

</dd> <dt>

<span id="Non-summable"></span><span id="non-summable"></span><span id="NON-SUMMABLE"></span>

<span data-ttu-id="41c3a-129"><span id="Non-summable"></span><span id="non-summable"></span><span id="NON-SUMMABLE"></span>**Без суммирования** (3)</span><span class="sxs-lookup"><span data-stu-id="41c3a-129"><span id="Non-summable"></span><span id="non-summable"></span><span id="NON-SUMMABLE"></span>**Non-summable** (3)</span></span>


</dt> <dd>

<span data-ttu-id="41c3a-130">Не имеет смысла суммировать это значение для многих экземпляров Унитофворк.</span><span class="sxs-lookup"><span data-stu-id="41c3a-130">It does not make sense to sum this value over many instances of UnitOfWork.</span></span> <span data-ttu-id="41c3a-131">Примером может быть метрика, которая измеряет длину очереди при поступлении задания на сервер.</span><span class="sxs-lookup"><span data-stu-id="41c3a-131">An example would be a metric that measures the queue length when a job arrives at a server.</span></span> <span data-ttu-id="41c3a-132">Если каждое задание является Унитофворк, а средняя длина очереди при поступлении каждого задания — 33, нет смысла говорить, что длина очереди для заданий 100 составляет 3300.</span><span class="sxs-lookup"><span data-stu-id="41c3a-132">If each job is a UnitOfWork, and the average queue length when each job arrives is 33, it does not make sense to say that the queue length for 100 jobs is 3300.</span></span> <span data-ttu-id="41c3a-133">Имеет смысл сказать, что среднее значение равно 33.</span><span class="sxs-lookup"><span data-stu-id="41c3a-133">It does make sense to say that the mean is 33.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="41c3a-134">**ChangeType**</span><span class="sxs-lookup"><span data-stu-id="41c3a-134">**ChangeType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c3a-135">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="41c3a-135">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="41c3a-136">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="41c3a-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41c3a-137">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ басеметрикдефинитион**.**Continuous**»)</span><span class="sxs-lookup"><span data-stu-id="41c3a-137">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_BaseMetricDefinition**.**IsContinuous**")</span></span>
</dt> </dl>

<span data-ttu-id="41c3a-138">Указывает, как изменяется значение метрики с помощью общих атрибутов, таких как изменение направления, минимальное и максимальное значения, а также семантика упаковки.</span><span class="sxs-lookup"><span data-stu-id="41c3a-138">Indicates how the metric value changes using common attributes such as direction change, minimum and maximum values, and wrapping semantics.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="41c3a-139"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="41c3a-139"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="41c3a-140">Конструктору метрик не удалось определить ChangeType.</span><span class="sxs-lookup"><span data-stu-id="41c3a-140">The metric designer did not qualify the ChangeType.</span></span>

</dd> <dt>

<span id="N_A"></span><span id="n_a"></span>

<span data-ttu-id="41c3a-141"><span id="N_A"></span><span id="n_a"></span>**Н/д** (2)</span><span class="sxs-lookup"><span data-stu-id="41c3a-141"><span id="N_A"></span><span id="n_a"></span>**N/A** (2)</span></span>


</dt> <dd>

<span data-ttu-id="41c3a-142">Если свойство "Continuous" имеет значение "false", то ChangeType не имеет смысла и для него должно быть задано значение "н/д".</span><span class="sxs-lookup"><span data-stu-id="41c3a-142">If the "IsContinuous" property is "false", ChangeType does not make sense and MUST be is set to "N/A".</span></span>

</dd> <dt>

<span id="Counter"></span><span id="counter"></span><span id="COUNTER"></span>

<span data-ttu-id="41c3a-143"><span id="Counter"></span><span id="counter"></span><span id="COUNTER"></span>**Счетчик** (3)</span><span class="sxs-lookup"><span data-stu-id="41c3a-143"><span id="Counter"></span><span id="counter"></span><span id="COUNTER"></span>**Counter** (3)</span></span>


</dt> <dd>

<span data-ttu-id="41c3a-144">Метрика является метрикой счетчика.</span><span class="sxs-lookup"><span data-stu-id="41c3a-144">The metric is a counter metric.</span></span> <span data-ttu-id="41c3a-145">Они имеют неотрицательные целочисленные значения, которые увеличиваются монотонно до достижения максимального допустимого числа, а затем заносятся в начало и начинают увеличиваться с 0.</span><span class="sxs-lookup"><span data-stu-id="41c3a-145">These have non-negative integer values which increase monotonically until reaching the maximum representable number and then wrap around and start increasing from 0.</span></span> <span data-ttu-id="41c3a-146">Такие счетчики, также называемые счетчиками смены, могут быть использованы для экземпляра для подсчета числа ошибок сети или количества обработанных транзакций.</span><span class="sxs-lookup"><span data-stu-id="41c3a-146">Such counters, also known as rollover counters, can be used for instance to count the number of network errors or the number of transactions processed.</span></span> <span data-ttu-id="41c3a-147">Единственным способом, с помощью которого клиентское приложение отслеживает заключение, является получение значения счетчика в соответствующие короткие интервалы.</span><span class="sxs-lookup"><span data-stu-id="41c3a-147">The only way for a client application to keep track of wrap arounds is to retrieve the value of the counter in appropriately short intervals.</span></span>

</dd> <dt>

<span id="Gauge"></span><span id="gauge"></span><span id="GAUGE"></span>

<span data-ttu-id="41c3a-148"><span id="Gauge"></span><span id="gauge"></span><span id="GAUGE"></span>**Датчик** (4)</span><span class="sxs-lookup"><span data-stu-id="41c3a-148"><span id="Gauge"></span><span id="gauge"></span><span id="GAUGE"></span>**Gauge** (4)</span></span>


</dt> <dd>

<span data-ttu-id="41c3a-149">Метрика — это метрика датчика.</span><span class="sxs-lookup"><span data-stu-id="41c3a-149">The metric is a gauge metric.</span></span> <span data-ttu-id="41c3a-150">Они имеют целые значения или числа с плавающей запятой, которые могут увеличиваться и уменьшаться произвольным образом.</span><span class="sxs-lookup"><span data-stu-id="41c3a-150">These have integer or float values that can increase and decrease arbitrarily.</span></span> <span data-ttu-id="41c3a-151">Индикатор не должен переноситься при достижении минимального или максимального допустимого числа, вместо этого значение "фиксируется" в этом номере.</span><span class="sxs-lookup"><span data-stu-id="41c3a-151">A gauge MUST NOT wrap when reaching the minimum or maximum representable number, instead, the value "sticks" at that number.</span></span> <span data-ttu-id="41c3a-152">Минимальное или максимальное значение в диапазоне представимых значений, в котором Метрика может быть определена как "число".</span><span class="sxs-lookup"><span data-stu-id="41c3a-152">Minimum or maximum values inside of the representable value range at which the metric value "sticks", may or may not be defined.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="41c3a-153"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (5.. 32767)</span><span class="sxs-lookup"><span data-stu-id="41c3a-153"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (5..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="41c3a-154"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Поставщик зарезервирован** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="41c3a-154"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="41c3a-155">**DataType**</span><span class="sxs-lookup"><span data-stu-id="41c3a-155">**DataType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c3a-156">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="41c3a-156">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="41c3a-157">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="41c3a-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41c3a-158">Тип данных метрики.</span><span class="sxs-lookup"><span data-stu-id="41c3a-158">The data type of the metric.</span></span>

<dt>

<span id="boolean"></span><span id="BOOLEAN"></span>

<span data-ttu-id="41c3a-159">**логическое значение** (1)</span><span class="sxs-lookup"><span data-stu-id="41c3a-159">**boolean** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="char16"></span><span id="CHAR16"></span>

<span data-ttu-id="41c3a-160">**Char16** (2)</span><span class="sxs-lookup"><span data-stu-id="41c3a-160">**char16** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="datetime"></span><span id="DATETIME"></span>

<span data-ttu-id="41c3a-161">**DateTime** (3)</span><span class="sxs-lookup"><span data-stu-id="41c3a-161">**datetime** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="real32"></span><span id="REAL32"></span>

<span data-ttu-id="41c3a-162">**real32** (4)</span><span class="sxs-lookup"><span data-stu-id="41c3a-162">**real32** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="real64"></span><span id="REAL64"></span>

<span data-ttu-id="41c3a-163">**real64** (5)</span><span class="sxs-lookup"><span data-stu-id="41c3a-163">**real64** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="sint16"></span><span id="SINT16"></span>

<span data-ttu-id="41c3a-164">**sint16** (6)</span><span class="sxs-lookup"><span data-stu-id="41c3a-164">**sint16** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="sint32"></span><span id="SINT32"></span>

<span data-ttu-id="41c3a-165">**Sint32** (7)</span><span class="sxs-lookup"><span data-stu-id="41c3a-165">**sint32** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="sint64"></span><span id="SINT64"></span>

<span data-ttu-id="41c3a-166">**sint64** (8)</span><span class="sxs-lookup"><span data-stu-id="41c3a-166">**sint64** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="sint8"></span><span id="SINT8"></span>

<span data-ttu-id="41c3a-167">**sint8** (9)</span><span class="sxs-lookup"><span data-stu-id="41c3a-167">**sint8** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="string"></span><span id="STRING"></span>

<span data-ttu-id="41c3a-168">**строка** (10)</span><span class="sxs-lookup"><span data-stu-id="41c3a-168">**string** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="uint16"></span><span id="UINT16"></span>

<span data-ttu-id="41c3a-169">**UInt16** (11)</span><span class="sxs-lookup"><span data-stu-id="41c3a-169">**uint16** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="uint32"></span><span id="UINT32"></span>

<span data-ttu-id="41c3a-170">**UInt32** (12)</span><span class="sxs-lookup"><span data-stu-id="41c3a-170">**uint32** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="uint64"></span><span id="UINT64"></span>

<span data-ttu-id="41c3a-171">**UInt64** (13)</span><span class="sxs-lookup"><span data-stu-id="41c3a-171">**uint64** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="uint8"></span><span id="UINT8"></span>

<span data-ttu-id="41c3a-172">**Uint8** (14)</span><span class="sxs-lookup"><span data-stu-id="41c3a-172">**uint8** (14)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="41c3a-173">**гасерингтипе**</span><span class="sxs-lookup"><span data-stu-id="41c3a-173">**GatheringType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c3a-174">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="41c3a-174">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="41c3a-175">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="41c3a-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41c3a-176">Указывает, как значения метрик собираются базовым инструментарием.</span><span class="sxs-lookup"><span data-stu-id="41c3a-176">Indicates how the metric values are gathered by the underlying instrumentation.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="41c3a-177"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="41c3a-177"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="41c3a-178">Указывает, что Гасерингтипе неизвестен.</span><span class="sxs-lookup"><span data-stu-id="41c3a-178">Indicates that the GatheringType is not known.</span></span>

</dd> <dt>

<span id="OnChange"></span><span id="onchange"></span><span id="ONCHANGE"></span>

<span data-ttu-id="41c3a-179"><span id="OnChange"></span><span id="onchange"></span><span id="ONCHANGE"></span>**OnChange** (2)</span><span class="sxs-lookup"><span data-stu-id="41c3a-179"><span id="OnChange"></span><span id="onchange"></span><span id="ONCHANGE"></span>**OnChange** (2)</span></span>


</dt> <dd>

<span data-ttu-id="41c3a-180">Указывает, что значения метрик CIM обновляются немедленно при изменении значений в измеренном ресурсе.</span><span class="sxs-lookup"><span data-stu-id="41c3a-180">Indicates that the CIM metric values get updated immediately when the values inside of the measured resource change.</span></span> <span data-ttu-id="41c3a-181">Значения метрик OnChange действительно отражать текущую ситуацию в ресурсе в любое время.</span><span class="sxs-lookup"><span data-stu-id="41c3a-181">The values of OnChange metrics truly reflect the current situation within the resource at any time.</span></span> <span data-ttu-id="41c3a-182">Например, число вошедших в систему пользователей, которые немедленно обновляются по мере входа и отключения пользователей.</span><span class="sxs-lookup"><span data-stu-id="41c3a-182">An example is the number of logged on users that gets updated immediately as users log on and off.</span></span>

</dd> <dt>

<span id="Periodic"></span><span id="periodic"></span><span id="PERIODIC"></span>

<span data-ttu-id="41c3a-183"><span id="Periodic"></span><span id="periodic"></span><span id="PERIODIC"></span>**Периодические** (3)</span><span class="sxs-lookup"><span data-stu-id="41c3a-183"><span id="Periodic"></span><span id="periodic"></span><span id="PERIODIC"></span>**Periodic** (3)</span></span>


</dt> <dd>

<span data-ttu-id="41c3a-184">": Указывает, что значения метрик CIM обновляются периодически.</span><span class="sxs-lookup"><span data-stu-id="41c3a-184">": Indicates that the CIM metric values get updated periodically.</span></span> <span data-ttu-id="41c3a-185">Например, для клиентского приложения значение метрики, применяемое к текущему времени, будет отображаться как константа во время каждого интервала сбора, а затем будет переходить к новому значению в конце каждого интервала сбора.</span><span class="sxs-lookup"><span data-stu-id="41c3a-185">For instance, to a client application, a metric value applying to the current time will appear constant during each gathering interval, and then jumps to the new value at the end of each gathering interval.</span></span>

</dd> <dt>

<span id="OnRequest"></span><span id="onrequest"></span><span id="ONREQUEST"></span>

<span data-ttu-id="41c3a-186"><span id="OnRequest"></span><span id="onrequest"></span><span id="ONREQUEST"></span>**Onrequest** (4)</span><span class="sxs-lookup"><span data-stu-id="41c3a-186"><span id="OnRequest"></span><span id="onrequest"></span><span id="ONREQUEST"></span>**OnRequest** (4)</span></span>


</dt> <dd>

<span data-ttu-id="41c3a-187">Указывает, что значение метрики CIM определяется каждый раз, когда клиентское приложение считывает его.</span><span class="sxs-lookup"><span data-stu-id="41c3a-187">Indicates that the CIM metric value is determined each time a client application reads it.</span></span> <span data-ttu-id="41c3a-188">Значения метрик onrequest действительно возвращают текущую ситуацию в ресурсе, если кто – то запрашивает его.</span><span class="sxs-lookup"><span data-stu-id="41c3a-188">The values of OnRequest metrics truly return the current situation within the resource if somebody asks for it.</span></span> <span data-ttu-id="41c3a-189">Однако они не изменяют "ненаблюдаемые", поэтому не рекомендуется подписываться на изменения значений метрик onrequest.</span><span class="sxs-lookup"><span data-stu-id="41c3a-189">However, they do not change "unobserved", and therefore subscribing for value changes of OnRequest metrics is NOT RECOMMENDED.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="41c3a-190"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (5.. 32767)</span><span class="sxs-lookup"><span data-stu-id="41c3a-190"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (5..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="41c3a-191"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Поставщик зарезервирован** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="41c3a-191"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="41c3a-192">**Id**</span><span class="sxs-lookup"><span data-stu-id="41c3a-192">**Id**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c3a-193">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="41c3a-193">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41c3a-194">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="41c3a-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41c3a-195">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="41c3a-195">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="41c3a-196">Уникальный идентификатор определения метрики.</span><span class="sxs-lookup"><span data-stu-id="41c3a-196">The unique ID of the metric definition.</span></span> <span data-ttu-id="41c3a-197">Рекомендуется использовать идентификаторы UUID и GUID Open Software Foundation (использование).</span><span class="sxs-lookup"><span data-stu-id="41c3a-197">Open Software Foundation (OSF) UUID/GUIDs are recommended.</span></span>

</dd> <dt>

<span data-ttu-id="41c3a-198">**IsContinuous**</span><span class="sxs-lookup"><span data-stu-id="41c3a-198">**IsContinuous**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c3a-199">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="41c3a-199">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="41c3a-200">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="41c3a-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41c3a-201">Значение true, если метрика непрерывная; в противном случае — значение false.</span><span class="sxs-lookup"><span data-stu-id="41c3a-201">True if the metric value is continuous; otherwise, false.</span></span>

</dd> <dt>

<span data-ttu-id="41c3a-202">**Name**</span><span class="sxs-lookup"><span data-stu-id="41c3a-202">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c3a-203">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="41c3a-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41c3a-204">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="41c3a-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41c3a-205">Имя метрики.</span><span class="sxs-lookup"><span data-stu-id="41c3a-205">The name of the metric.</span></span> <span data-ttu-id="41c3a-206">Это имя может быть уникальным, но оно должно быть описательным и содержать пробелы.</span><span class="sxs-lookup"><span data-stu-id="41c3a-206">This name does not have to be unique, but should be descriptive and may contain blank spaces.</span></span>

</dd> <dt>

<span data-ttu-id="41c3a-207">**программатикунитс**</span><span class="sxs-lookup"><span data-stu-id="41c3a-207">**ProgrammaticUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c3a-208">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="41c3a-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41c3a-209">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="41c3a-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41c3a-210">Конкретные единицы значения.</span><span class="sxs-lookup"><span data-stu-id="41c3a-210">The specific units of a value.</span></span> <span data-ttu-id="41c3a-211">Значение этого свойства должно быть допустимым значением квалификатора программных единиц, как определено в приложении C. 1 DSP0004 V 2.4 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="41c3a-211">The value of this property should be a legal value of the Programmatic Units qualifier as defined in Appendix C.1 of DSP0004 V2.4 or later.</span></span>

</dd> <dt>

<span data-ttu-id="41c3a-212">**тимескопе**</span><span class="sxs-lookup"><span data-stu-id="41c3a-212">**TimeScope**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c3a-213">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="41c3a-213">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="41c3a-214">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="41c3a-214">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41c3a-215">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ басеметриквалуе**](cim-basemetricvalue.md).**TimeStamp**","**CIM \_ басеметриквалуе**.**Duration (длительность**))</span><span class="sxs-lookup"><span data-stu-id="41c3a-215">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_BaseMetricValue**](cim-basemetricvalue.md).**TimeStamp**", "**CIM\_BaseMetricValue**.**Duration**")</span></span>
</dt> </dl>

<span data-ttu-id="41c3a-216">Область времени, которая применяется к конструктору метрик.</span><span class="sxs-lookup"><span data-stu-id="41c3a-216">The time scope that applies to the metric designer.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="41c3a-217"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="41c3a-217"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="41c3a-218">Указывает, что область времени не определена конструктором метрик или неизвестна поставщику.</span><span class="sxs-lookup"><span data-stu-id="41c3a-218">Indicates the time scope was not qualified by the metric designer, or is unknown to the provider.</span></span>

</dd> <dt>

<span id="Point"></span><span id="point"></span><span id="POINT"></span>

<span data-ttu-id="41c3a-219"><span id="Point"></span><span id="point"></span><span id="POINT"></span>**Точка** (2)</span><span class="sxs-lookup"><span data-stu-id="41c3a-219"><span id="Point"></span><span id="point"></span><span id="POINT"></span>**Point** (2)</span></span>


</dt> <dd>

<span data-ttu-id="41c3a-220">Указывает, что метрика относится к моменту времени.</span><span class="sxs-lookup"><span data-stu-id="41c3a-220">Indicates that the metric applies to a point in time.</span></span> <span data-ttu-id="41c3a-221">В соответствующих экземплярах Басеметриквалуе метка времени указывает на момент времени, а длительность всегда равна 0.</span><span class="sxs-lookup"><span data-stu-id="41c3a-221">On the corresponding BaseMetricValue instances, TimeStamp specifies the point in time and Duration is always 0.</span></span>

</dd> <dt>

<span id="Interval"></span><span id="interval"></span><span id="INTERVAL"></span>

<span data-ttu-id="41c3a-222"><span id="Interval"></span><span id="interval"></span><span id="INTERVAL"></span>**Интервал** (3)</span><span class="sxs-lookup"><span data-stu-id="41c3a-222"><span id="Interval"></span><span id="interval"></span><span id="INTERVAL"></span>**Interval** (3)</span></span>


</dt> <dd>

<span data-ttu-id="41c3a-223">Указывает, что метрика применяется к интервалу времени.</span><span class="sxs-lookup"><span data-stu-id="41c3a-223">Indicates that the metric applies to a time interval.</span></span> <span data-ttu-id="41c3a-224">В соответствующих экземплярах Басеметриквалуе метка времени указывает конец интервала времени, а длительность задает его длительность.</span><span class="sxs-lookup"><span data-stu-id="41c3a-224">On the corresponding BaseMetricValue instances, TimeStamp specifies the end of the time interval and Duration specifies its duration</span></span>

</dd> <dt>

<span id="StartupInterval"></span><span id="startupinterval"></span><span id="STARTUPINTERVAL"></span>

<span data-ttu-id="41c3a-225"><span id="StartupInterval"></span><span id="startupinterval"></span><span id="STARTUPINTERVAL"></span>**Стартупинтервал** (4)</span><span class="sxs-lookup"><span data-stu-id="41c3a-225"><span id="StartupInterval"></span><span id="startupinterval"></span><span id="STARTUPINTERVAL"></span>**StartupInterval** (4)</span></span>


</dt> <dd>

<span data-ttu-id="41c3a-226">Указывает, что метрика применяется к интервалу времени, который начался при запуске измеряемого ресурса (т. е. Манажеделемент, связанном с Метрикдефформе).</span><span class="sxs-lookup"><span data-stu-id="41c3a-226">Indicates that the metric applies to a time interval that began at the startup of the measured resource (i.e. the ManagedElement associated by MetricDefForMe).</span></span> <span data-ttu-id="41c3a-227">В соответствующих экземплярах Басеметриквалуе метка времени указывает конец интервала времени.</span><span class="sxs-lookup"><span data-stu-id="41c3a-227">On the corresponding BaseMetricValue instances, TimeStamp specifies the end of the time interval.</span></span> <span data-ttu-id="41c3a-228">Если значение Duration равно 0, это означает, что время запуска измеряемого ресурса неизвестно.</span><span class="sxs-lookup"><span data-stu-id="41c3a-228">If Duration is 0, this indicates that the startup time of the measured resource is unknown.</span></span> <span data-ttu-id="41c3a-229">В противном случае длительность указывает длительность между запуском ресурса и меткой времени.</span><span class="sxs-lookup"><span data-stu-id="41c3a-229">Else, Duration specifies the duration between startup of the resource and TimeStamp.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="41c3a-230"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (5.. 32767)</span><span class="sxs-lookup"><span data-stu-id="41c3a-230"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (5..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="41c3a-231"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Поставщик зарезервирован** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="41c3a-231"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="41c3a-232">**единиц(ы)**</span><span class="sxs-lookup"><span data-stu-id="41c3a-232">**Units**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c3a-233">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="41c3a-233">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41c3a-234">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="41c3a-234">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41c3a-235">Единицы измерения метрики.</span><span class="sxs-lookup"><span data-stu-id="41c3a-235">The units of the metric.</span></span> <span data-ttu-id="41c3a-236">Примерами могут быть байты, пакеты, задания, файлы, миллисекунды и ампер.</span><span class="sxs-lookup"><span data-stu-id="41c3a-236">Examples are bytes, packets, jobs, files, milliseconds, and amps.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="41c3a-237">Требования</span><span class="sxs-lookup"><span data-stu-id="41c3a-237">Requirements</span></span>



| <span data-ttu-id="41c3a-238">Требование</span><span class="sxs-lookup"><span data-stu-id="41c3a-238">Requirement</span></span> | <span data-ttu-id="41c3a-239">Значение</span><span class="sxs-lookup"><span data-stu-id="41c3a-239">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41c3a-240">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="41c3a-240">Minimum supported client</span></span><br/> | <span data-ttu-id="41c3a-241">Windows 8</span><span class="sxs-lookup"><span data-stu-id="41c3a-241">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="41c3a-242">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="41c3a-242">Minimum supported server</span></span><br/> | <span data-ttu-id="41c3a-243">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="41c3a-243">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="41c3a-244">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="41c3a-244">Namespace</span></span><br/>                | <span data-ttu-id="41c3a-245">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="41c3a-245">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="41c3a-246">MOF</span><span class="sxs-lookup"><span data-stu-id="41c3a-246">MOF</span></span><br/>                      | <dl> <span data-ttu-id="41c3a-247"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="41c3a-247"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="41c3a-248">DLL</span><span class="sxs-lookup"><span data-stu-id="41c3a-248">DLL</span></span><br/>                      | <dl> <span data-ttu-id="41c3a-249"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="41c3a-249"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="41c3a-250">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="41c3a-250">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41c3a-251">**\_МАНАЖЕДЕЛЕМЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="41c3a-251">**CIM\_ManagedElement**</span></span>](cim-managedelement.md)
</dt> </dl>

 

