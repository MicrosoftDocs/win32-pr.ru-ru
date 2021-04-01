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
# <a name="msvm_aggregationmetricvalue-class"></a><span data-ttu-id="152af-103">\_Класс мсвм аггрегатионметриквалуе</span><span class="sxs-lookup"><span data-stu-id="152af-103">Msvm\_AggregationMetricValue class</span></span>

<span data-ttu-id="152af-104">Представляет значение экземпляра метрики, определенной экземпляром класса [**мсвм \_ аггрегатионметрикдефинитион**](msvm-aggregationmetricdefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="152af-104">Represents the instance value of a metric defined by an instance of the [**Msvm\_AggregationMetricDefinition**](msvm-aggregationmetricdefinition.md) class.</span></span> <span data-ttu-id="152af-105">Свойства, наследуемые от [**мсвм \_ басеметриквалуе**](msvm-basemetricvalue.md) , предоставляют фактическое значение метрики.</span><span class="sxs-lookup"><span data-stu-id="152af-105">The properties inherited from [**Msvm\_BaseMetricValue**](msvm-basemetricvalue.md) provide the actual metric value.</span></span> <span data-ttu-id="152af-106">Свойства, определенные этим классом, предоставляют сведения о интервале, через который была применена статистическая функция.</span><span class="sxs-lookup"><span data-stu-id="152af-106">The properties defined by this class provide information about the interval over which the aggregation function was applied.</span></span>

<span data-ttu-id="152af-107">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="152af-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="152af-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="152af-108">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="152af-109">Члены</span><span class="sxs-lookup"><span data-stu-id="152af-109">Members</span></span>

<span data-ttu-id="152af-110">Класс **мсвм \_ аггрегатионметриквалуе** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="152af-110">The **Msvm\_AggregationMetricValue** class has these types of members:</span></span>

-   [<span data-ttu-id="152af-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="152af-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="152af-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="152af-112">Properties</span></span>

<span data-ttu-id="152af-113">Класс **мсвм \_ аггрегатионметриквалуе** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="152af-113">The **Msvm\_AggregationMetricValue** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="152af-114">**аггрегатиондуратион**</span><span class="sxs-lookup"><span data-stu-id="152af-114">**AggregationDuration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="152af-115">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="152af-115">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="152af-116">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="152af-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="152af-117">Представляет период времени, в течение которого Вычисление агрегата было выполнено.</span><span class="sxs-lookup"><span data-stu-id="152af-117">Represents the time duration over which the aggregation was computed.</span></span> <span data-ttu-id="152af-118">Начало интервала мониторинга, по отношению к которому применяется статистическая функция, определяется путем вычитания **аггрегатиондуратион** из **аггрегатионтиместамп**.</span><span class="sxs-lookup"><span data-stu-id="152af-118">The start of a monitoring interval over which the aggregation function is applied is determined by subtracting the **AggregationDuration** from the **AggregationTimeStamp**.</span></span> <span data-ttu-id="152af-119">Это свойство наследуется от **CIM \_ аггрегатионметриквалуе**.</span><span class="sxs-lookup"><span data-stu-id="152af-119">This property is inherited from **CIM\_AggregationMetricValue**.</span></span>

</dd> <dt>

<span data-ttu-id="152af-120">**аггрегатионтиместамп**</span><span class="sxs-lookup"><span data-stu-id="152af-120">**AggregationTimeStamp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="152af-121">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="152af-121">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="152af-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="152af-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="152af-123">Определяет время, когда статистическая функция была применена для определения значения экземпляра метрики.</span><span class="sxs-lookup"><span data-stu-id="152af-123">Identifies the time when the aggregation function was applied to determine the value of the metric instance.</span></span> <span data-ttu-id="152af-124">Это не то же самое, что и время создания экземпляра.</span><span class="sxs-lookup"><span data-stu-id="152af-124">This is not the same as the time when the instance was created.</span></span> <span data-ttu-id="152af-125">Для данного экземпляра **CIM \_ аггрегатионметриквалуе** **аггрегатионтиместамп** изменяется при применении статистической функции к вычислению значения.</span><span class="sxs-lookup"><span data-stu-id="152af-125">For a given **CIM\_AggregationMetricValue** instance, the **AggregationTimeStamp** changes whenever the aggregation function is applied to calculate the value.</span></span> <span data-ttu-id="152af-126">Это свойство наследуется от **CIM \_ аггрегатионметриквалуе**.</span><span class="sxs-lookup"><span data-stu-id="152af-126">This property is inherited from **CIM\_AggregationMetricValue**.</span></span>

</dd> <dt>

<span data-ttu-id="152af-127">**бреакдовндименсион**</span><span class="sxs-lookup"><span data-stu-id="152af-127">**BreakdownDimension**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="152af-128">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="152af-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="152af-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="152af-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="152af-130">Указывает одно измерение декомпозиции из массива **бреакдовндименсионс** , определенного в связанном [**мсвм \_ басеметрикдефинитион**](msvm-basemetricdefinition.md).</span><span class="sxs-lookup"><span data-stu-id="152af-130">Specifies one breakdown dimension from the **BreakdownDimensions** array defined in the associated [**Msvm\_BaseMetricDefinition**](msvm-basemetricdefinition.md).</span></span> <span data-ttu-id="152af-131">Это измерение, в котором этот набор значений метрик разбит на части.</span><span class="sxs-lookup"><span data-stu-id="152af-131">This is the dimension along which this set of metric values is broken down.</span></span> <span data-ttu-id="152af-132">Это свойство наследуется от [**CIM \_ басеметрикдефинитион**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="152af-132">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="152af-133">**бреакдовнвалуе**</span><span class="sxs-lookup"><span data-stu-id="152af-133">**BreakdownValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="152af-134">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="152af-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="152af-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="152af-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="152af-136">Определяет значение свойства **бреакдовндименсион** , определенного для данного экземпляра значения метрики.</span><span class="sxs-lookup"><span data-stu-id="152af-136">Defines a value of the **BreakdownDimension** property defined for this metric value instance.</span></span> <span data-ttu-id="152af-137">Например, если **бреакдовндименсион** имеет значение "трансактионнаме", это свойство может наименовать фактическую транзакцию, к которой применяется это конкретное метрика.</span><span class="sxs-lookup"><span data-stu-id="152af-137">For example, if the **BreakdownDimension** is "TransactionName", this property could name the actual transaction to which this particular metric value applies.</span></span> <span data-ttu-id="152af-138">Это свойство наследуется от [**CIM \_ басеметрикдефинитион**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="152af-138">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="152af-139">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="152af-139">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="152af-140">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="152af-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="152af-141">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="152af-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="152af-142">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="152af-142">A short description of the object.</span></span> <span data-ttu-id="152af-143">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="152af-143">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="152af-144">**Описание**</span><span class="sxs-lookup"><span data-stu-id="152af-144">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="152af-145">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="152af-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="152af-146">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="152af-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="152af-147">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="152af-147">A description of the object.</span></span> <span data-ttu-id="152af-148">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="152af-148">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="152af-149">**Длительность**</span><span class="sxs-lookup"><span data-stu-id="152af-149">**Duration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="152af-150">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="152af-150">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="152af-151">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="152af-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="152af-152">Указывает период времени, в течение которого это значение метрики является допустимым.</span><span class="sxs-lookup"><span data-stu-id="152af-152">Specifies the time duration over which this metric value is valid.</span></span> <span data-ttu-id="152af-153">Это свойство не должно существовать для меток времени, которые применяются только к моменту времени, но должны быть указаны для значений, которые считаются допустимыми в течение определенного периода времени (например, выборка).</span><span class="sxs-lookup"><span data-stu-id="152af-153">This property should not exist for time stamps that apply only to a point in time, but should be specified for values that are considered valid for a certain time period (for example, sampling).</span></span> <span data-ttu-id="152af-154">Если свойство **Duration** существует и не равно **null**, свойство **timestamp** задает конец интервала.</span><span class="sxs-lookup"><span data-stu-id="152af-154">If the **Duration** property exists and is not **Null**, the **TimeStamp** property specifies the end of the interval.</span></span> <span data-ttu-id="152af-155">Это свойство наследуется от [**CIM \_ басеметрикдефинитион**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="152af-155">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="152af-156">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="152af-156">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="152af-157">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="152af-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="152af-158">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="152af-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="152af-159">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="152af-159">A display name for the object.</span></span> <span data-ttu-id="152af-160">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="152af-160">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="152af-161">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="152af-161">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="152af-162">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="152af-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="152af-163">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="152af-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="152af-164">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="152af-164">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="152af-165">Строка, уникально идентифицирующая экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="152af-165">A string that uniquely identifies an instance of this class.</span></span> <span data-ttu-id="152af-166">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="152af-166">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="152af-167">**меасуределементнаме**</span><span class="sxs-lookup"><span data-stu-id="152af-167">**MeasuredElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="152af-168">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="152af-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="152af-169">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="152af-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="152af-170">Описательное имя элемента, которому принадлежит значение метрики (измеряемый элемент).</span><span class="sxs-lookup"><span data-stu-id="152af-170">A descriptive name for the element to which the metric value belongs (the measured element).</span></span> <span data-ttu-id="152af-171">Это свойство наследуется от [**CIM \_ басеметрикдефинитион**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="152af-171">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="152af-172">**метрикдефинитионид**</span><span class="sxs-lookup"><span data-stu-id="152af-172">**MetricDefinitionId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="152af-173">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="152af-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="152af-174">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="152af-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="152af-175">Ключ экземпляра [**\_ басеметрикдефинитион мсвм**](msvm-basemetricdefinition.md) для этого значения.</span><span class="sxs-lookup"><span data-stu-id="152af-175">The key of the [**Msvm\_BaseMetricDefinition**](msvm-basemetricdefinition.md) instance for this value.</span></span> <span data-ttu-id="152af-176">Это свойство наследуется от [**CIM \_ басеметрикдефинитион**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="152af-176">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="152af-177">**метриквалуе**</span><span class="sxs-lookup"><span data-stu-id="152af-177">**MetricValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="152af-178">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="152af-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="152af-179">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="152af-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="152af-180">Значение метрики, представленное в виде строки.</span><span class="sxs-lookup"><span data-stu-id="152af-180">The value of the metric that is represented as a string.</span></span> <span data-ttu-id="152af-181">Это свойство наследуется от [**CIM \_ басеметрикдефинитион**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="152af-181">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="152af-182">**TimeStamp**</span><span class="sxs-lookup"><span data-stu-id="152af-182">**TimeStamp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="152af-183">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="152af-183">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="152af-184">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="152af-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="152af-185">Указывает время, когда значение метрики было перехвачено или вычислено.</span><span class="sxs-lookup"><span data-stu-id="152af-185">Specifies the time when the metric value was captured or computed.</span></span> <span data-ttu-id="152af-186">Имейте в виду, что это отличается от времени создания экземпляра.</span><span class="sxs-lookup"><span data-stu-id="152af-186">Be aware that this is different from the time when the instance was created.</span></span> <span data-ttu-id="152af-187">Это свойство наследуется от [**CIM \_ басеметрикдефинитион**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="152af-187">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="152af-188">**Независимо**</span><span class="sxs-lookup"><span data-stu-id="152af-188">**Volatile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="152af-189">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="152af-189">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="152af-190">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="152af-190">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="152af-191">Значение **true** , если значение для следующего момента времени будет использовать один и тот же экземпляр класса и просто изменить значения свойств (например, **значение** или **метку времени**).</span><span class="sxs-lookup"><span data-stu-id="152af-191">**True** if the value for the next point in time will use the same class instance and just change the property values (such as the **Value** or **TimeStamp**).</span></span> <span data-ttu-id="152af-192">Если **значение — true**, экземпляр используется повторно.</span><span class="sxs-lookup"><span data-stu-id="152af-192">If **True**, the instance is reused.</span></span> <span data-ttu-id="152af-193">Если **значение равно false**, существующие экземпляры остаются неизменными и создается новый экземпляр для нового момента времени.</span><span class="sxs-lookup"><span data-stu-id="152af-193">If **False**, the existing instances remain unchanged and a new instance is created for the new point in time.</span></span> <span data-ttu-id="152af-194">Это свойство наследуется от [**CIM \_ басеметрикдефинитион**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="152af-194">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="152af-195">Требования</span><span class="sxs-lookup"><span data-stu-id="152af-195">Requirements</span></span>



| <span data-ttu-id="152af-196">Требование</span><span class="sxs-lookup"><span data-stu-id="152af-196">Requirement</span></span> | <span data-ttu-id="152af-197">Значение</span><span class="sxs-lookup"><span data-stu-id="152af-197">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="152af-198">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="152af-198">Minimum supported client</span></span><br/> | <span data-ttu-id="152af-199">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="152af-199">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="152af-200">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="152af-200">Minimum supported server</span></span><br/> | <span data-ttu-id="152af-201">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="152af-201">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="152af-202">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="152af-202">Namespace</span></span><br/>                | <span data-ttu-id="152af-203">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="152af-203">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="152af-204">MOF</span><span class="sxs-lookup"><span data-stu-id="152af-204">MOF</span></span><br/>                      | <dl> <span data-ttu-id="152af-205"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="152af-205"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="152af-206">DLL</span><span class="sxs-lookup"><span data-stu-id="152af-206">DLL</span></span><br/>                      | <dl> <span data-ttu-id="152af-207"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="152af-207"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

