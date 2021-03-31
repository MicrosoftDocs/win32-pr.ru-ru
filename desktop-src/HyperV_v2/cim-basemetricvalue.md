---
description: Представляет значение экземпляра метрики.
ms.assetid: 6b272ae8-7684-45bb-bff8-6559680cc8b6
title: Класс CIM_BaseMetricValue
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BaseMetricValue
- CIM_BaseMetricValue.InstanceID
- CIM_BaseMetricValue.MetricDefinitionId
- CIM_BaseMetricValue.MeasuredElementName
- CIM_BaseMetricValue.TimeStamp
- CIM_BaseMetricValue.Duration
- CIM_BaseMetricValue.MetricValue
- CIM_BaseMetricValue.BreakdownDimension
- CIM_BaseMetricValue.BreakdownValue
- CIM_BaseMetricValue.Volatile
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ca6c90a4b6b3ef3e690c13612f69480ec5f008be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999117"
---
# <a name="cim_basemetricvalue-class"></a><span data-ttu-id="4db41-103">\_Класс CIM басеметриквалуе</span><span class="sxs-lookup"><span data-stu-id="4db41-103">CIM\_BaseMetricValue class</span></span>

<span data-ttu-id="4db41-104">Представляет значение экземпляра метрики.</span><span class="sxs-lookup"><span data-stu-id="4db41-104">Represents the instance value of a metric.</span></span>

## <a name="syntax"></a><span data-ttu-id="4db41-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4db41-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.19.0"), UMLPackagePath("CIM::Metrics::BaseMetric"), AMENDMENT]
class CIM_BaseMetricValue : CIM_ManagedElement
{
  string   InstanceID;
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

## <a name="members"></a><span data-ttu-id="4db41-106">Члены</span><span class="sxs-lookup"><span data-stu-id="4db41-106">Members</span></span>

<span data-ttu-id="4db41-107">Класс **CIM \_ басеметриквалуе** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="4db41-107">The **CIM\_BaseMetricValue** class has these types of members:</span></span>

-   [<span data-ttu-id="4db41-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="4db41-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4db41-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="4db41-109">Properties</span></span>

<span data-ttu-id="4db41-110">Класс **CIM \_ басеметриквалуе** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="4db41-110">The **CIM\_BaseMetricValue** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4db41-111">**бреакдовндименсион**</span><span class="sxs-lookup"><span data-stu-id="4db41-111">**BreakdownDimension**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4db41-112">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4db41-112">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4db41-113">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4db41-113">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4db41-114">Измерение, для которого этот набор значений метрик разделяется на основе свойства **бреакдовндименсионс** связанного объекта [**CIM \_ басеметрикдефинитион**](cim-basemetricdefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="4db41-114">The dimension for which this set of metric values is broken down based on **BreakdownDimensions** property of the associated [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="4db41-115">**бреакдовнвалуе**</span><span class="sxs-lookup"><span data-stu-id="4db41-115">**BreakdownValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4db41-116">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4db41-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4db41-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4db41-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4db41-118">Значение свойства **бреакдовндименсион** , определенное для данного значения экземпляра.</span><span class="sxs-lookup"><span data-stu-id="4db41-118">The value of the **BreakdownDimension** property defined for this instance value.</span></span> <span data-ttu-id="4db41-119">Например, если **бреакдовндименсион** содержит "трансактионнаме", это свойство может наименовать фактическую транзакцию, к которой применяется это конкретное значение метрики.</span><span class="sxs-lookup"><span data-stu-id="4db41-119">For example, if **BreakdownDimension** contains "TransactionName", this property could name the actual transaction to which this particular metric value applies.</span></span>

</dd> <dt>

<span data-ttu-id="4db41-120">**Длительность**</span><span class="sxs-lookup"><span data-stu-id="4db41-120">**Duration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4db41-121">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="4db41-121">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="4db41-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4db41-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4db41-123">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ басеметрикдефинитион**](cim-basemetricdefinition.md).**Тимескопе**","**CIM \_ басеметриквалуе**.**TimeStamp**")</span><span class="sxs-lookup"><span data-stu-id="4db41-123">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md).**TimeScope**", "**CIM\_BaseMetricValue**.**TimeStamp**")</span></span>
</dt> </dl>

<span data-ttu-id="4db41-124">Период времени, в течение которого это значение метрики является допустимым.</span><span class="sxs-lookup"><span data-stu-id="4db41-124">The time duration over which this metric value is valid.</span></span> <span data-ttu-id="4db41-125">Это свойство не должно существовать для меток времени, которые применяются только к моменту времени, но должны быть определены для значений, которые считаются допустимыми в течение определенного периода времени (например,</span><span class="sxs-lookup"><span data-stu-id="4db41-125">This property should not exist for time stamps that only apply to a point in time, but should be defined for values that are considered valid for a certain time period (ex.</span></span> <span data-ttu-id="4db41-126">выборка).</span><span class="sxs-lookup"><span data-stu-id="4db41-126">sampling).</span></span> <span data-ttu-id="4db41-127">Если свойство **Duration** существует и не равно null, значение **timestamp** должно быть концом интервала.</span><span class="sxs-lookup"><span data-stu-id="4db41-127">If the **Duration** property exists and is non-Null, the **TimeStamp** value should be the end of the interval.</span></span>

</dd> <dt>

<span data-ttu-id="4db41-128">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="4db41-128">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4db41-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4db41-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4db41-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4db41-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4db41-131">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceId")</span><span class="sxs-lookup"><span data-stu-id="4db41-131">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceID")</span></span>
</dt> </dl>

<span data-ttu-id="4db41-132">Уникально идентифицирует экземпляр этого класса в области содержащего его пространства имен.</span><span class="sxs-lookup"><span data-stu-id="4db41-132">Uniquely identifies an instance of this class within the scope of the containing namespace.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="4db41-133">Чтобы обеспечить уникальность в пространстве имен, значение свойства **InstanceId** должно быть создано в следующем шаблоне: *OrgID*:*LocalId*</span><span class="sxs-lookup"><span data-stu-id="4db41-133">In order to ensure uniqueness within the namespace, the value of the **InstanceID** property should be constructed in the following pattern: *OrgID*:*LocalID*</span></span>
>
> <span data-ttu-id="4db41-134">*OrgID* должен включать в себя запись с правом или иным именем, которая принадлежит бизнес-сущности, определяющей **InstanceId**, или быть зарегистрированным идентификатором, который назначается распознанным глобальным центром сертификации.</span><span class="sxs-lookup"><span data-stu-id="4db41-134">*OrgID* must include a copyrighted, trademarked or otherwise unique name that is owned by the business entity that defines the **InstanceID**, or be a registered ID that is assigned by a recognized global authority.</span></span> <span data-ttu-id="4db41-135">Этот шаблон похож на структуру имен классов схемы.</span><span class="sxs-lookup"><span data-stu-id="4db41-135">This pattern is similar to the structure of schema class names.</span></span> <span data-ttu-id="4db41-136">Кроме того, чтобы обеспечить уникальность, первое двоеточие в **InstanceId** должно находиться между *OrgID* и *LocalId*.</span><span class="sxs-lookup"><span data-stu-id="4db41-136">In addition, to ensure uniqueness, the first colon in **InstanceID** must be between the *OrgID* and *LocalID*.</span></span> <span data-ttu-id="4db41-137">Поэтому *OrgID* не должен содержать двоеточие (":").</span><span class="sxs-lookup"><span data-stu-id="4db41-137">Therefore the *OrgID* must not contain a colon (':').</span></span>
>
> <span data-ttu-id="4db41-138">*LocalId* выбирается бизнес-сущностью и не должна использоваться повторно для обнаружения различных базовых реальных элементов.</span><span class="sxs-lookup"><span data-stu-id="4db41-138">*LocalID* is chosen by the business entity and should not be re-used to identify different underlying real-world elements.</span></span>
>
> <span data-ttu-id="4db41-139">Если приведенный выше шаблон не используется, определяющая сущность должна гарантировать, что результирующее значение **InstanceId** не будет повторно использоваться во всех свойствах **InstanceId** , созданных этим поставщиком или другими поставщиками для этого пространства имен.</span><span class="sxs-lookup"><span data-stu-id="4db41-139">If the above pattern is not used, the defining entity must assure that the resultant **InstanceID** value is not re-used across any **InstanceID** properties that are produced by this provider or other providers for this namespace.</span></span>
>
> <span data-ttu-id="4db41-140">Для экземпляров распределенного управления Task Force (DMTF) необходимо использовать шаблон с *OrgID* , для которого задано значение CIM.</span><span class="sxs-lookup"><span data-stu-id="4db41-140">For Distributed Management Task Force (DMTF) defined instances, the pattern must be used with the *OrgID* set to CIM.</span></span>

 

</dd> <dt>

<span data-ttu-id="4db41-141">**меасуределементнаме**</span><span class="sxs-lookup"><span data-stu-id="4db41-141">**MeasuredElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4db41-142">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4db41-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4db41-143">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4db41-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4db41-144">Описательное имя элемента, которое измеряется метрикой.</span><span class="sxs-lookup"><span data-stu-id="4db41-144">A descriptive name for the element that is measure by the metric.</span></span>

<span data-ttu-id="4db41-145">Это свойство является обязательным, если определение метрики не связано с объектом [**CIM \_ манажеделемент**](cim-managedelement.md) , и его можно использовать в других случаях для предоставления дополнительных сведений.</span><span class="sxs-lookup"><span data-stu-id="4db41-145">This property is required if the metric definition is not associated with a [**CIM\_ManagedElement**](cim-managedelement.md) object, and may be used in other cases to provide supplemental information.</span></span> <span data-ttu-id="4db41-146">Это позволяет записывать метрики независимо от любого объекта **CIM \_ манажеделемент** .</span><span class="sxs-lookup"><span data-stu-id="4db41-146">This allows metrics to be captured independent of any **CIM\_ManagedElement** object.</span></span>

<span data-ttu-id="4db41-147">При наличии нескольких объектов [**CIM \_ манажеделемент**](cim-managedelement.md) , связанных со значением метрики, можно выбрать один из управляемых элементов, чтобы создать дополнительные сведения для метрики.</span><span class="sxs-lookup"><span data-stu-id="4db41-147">If there are multiple [**CIM\_ManagedElement**](cim-managedelement.md) objects associated with the metric value, then you can choose one of the managed elements to create the supplemental information for the metric.</span></span> <span data-ttu-id="4db41-148">Свойство не предназначено для использования в качестве внешнего ключа для запроса измеряемого элемента.</span><span class="sxs-lookup"><span data-stu-id="4db41-148">The property is not meant to be used as a foreign key to query the measured element.</span></span> <span data-ttu-id="4db41-149">Вместо этого следует использовать связь с **\_ манажеделемент CIM** .</span><span class="sxs-lookup"><span data-stu-id="4db41-149">Instead, the association to the **CIM\_ManagedElement** should be used.</span></span>

</dd> <dt>

<span data-ttu-id="4db41-150">**метрикдефинитионид**</span><span class="sxs-lookup"><span data-stu-id="4db41-150">**MetricDefinitionId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4db41-151">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4db41-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4db41-152">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4db41-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4db41-153">Квалификаторы: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ басеметрикдефинитион**](cim-basemetricdefinition.md).**ID**")</span><span class="sxs-lookup"><span data-stu-id="4db41-153">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md).**Id**")</span></span>
</dt> </dl>

<span data-ttu-id="4db41-154">Ключ экземпляра [**CIM \_ басеметрикдефинитион**](cim-basemetricdefinition.md) , связанный с данным значением экземпляра.</span><span class="sxs-lookup"><span data-stu-id="4db41-154">The key of the [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) instance that is associated with this instance value.</span></span>

</dd> <dt>

<span data-ttu-id="4db41-155">**метриквалуе**</span><span class="sxs-lookup"><span data-stu-id="4db41-155">**MetricValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4db41-156">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4db41-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4db41-157">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4db41-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4db41-158">Квалификаторы: [ **обязательно**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="4db41-158">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="4db41-159">Строковое представление значения метрики.</span><span class="sxs-lookup"><span data-stu-id="4db41-159">A string representation of the metric value.</span></span> <span data-ttu-id="4db41-160">Исходный тип данных значения метрики указывается в связанном объекте [**CIM \_ басеметрикдефинитион**](cim-basemetricdefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="4db41-160">The original data type of the metric value is specified in the associated [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="4db41-161">**TimeStamp**</span><span class="sxs-lookup"><span data-stu-id="4db41-161">**TimeStamp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4db41-162">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="4db41-162">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="4db41-163">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4db41-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4db41-164">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ басеметрикдефинитион**](cim-basemetricdefinition.md).**Тимескопе**","**CIM \_ басеметриквалуе**.**Duration (длительность**))</span><span class="sxs-lookup"><span data-stu-id="4db41-164">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md).**TimeScope**", "**CIM\_BaseMetricValue**.**Duration**")</span></span>
</dt> </dl>

<span data-ttu-id="4db41-165">Время, когда будет вычислено значение экземпляра метрики.</span><span class="sxs-lookup"><span data-stu-id="4db41-165">The time when the value of a metric instance is computed.</span></span> <span data-ttu-id="4db41-166">Это отличается от времени создания экземпляра.</span><span class="sxs-lookup"><span data-stu-id="4db41-166">This is different from the time when the instance is created.</span></span> <span data-ttu-id="4db41-167">Если свойство **volatile** имеет значение true, это значение изменяется при каждом создании нового моментального снимка измерения.</span><span class="sxs-lookup"><span data-stu-id="4db41-167">If the **Volatile** property is true, this value changes whenever a new measurement snapshot is taken.</span></span>

<span data-ttu-id="4db41-168">Приложение управления может установить временные ряды данных метрик, извлекая экземпляры **CIM \_ басеметриквалуе** и сортируя их в соответствии со значением **метки времени** .</span><span class="sxs-lookup"><span data-stu-id="4db41-168">A management application may establish a time series of metric data by retrieving the instances of **CIM\_BaseMetricValue** and sorting them according to their **TimeStamp** value.</span></span>

</dd> <dt>

<span data-ttu-id="4db41-169">**Независимо**</span><span class="sxs-lookup"><span data-stu-id="4db41-169">**Volatile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4db41-170">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="4db41-170">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4db41-171">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4db41-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4db41-172">Значение true, если значение **метки времени** изменяется при каждом изменении значения экземпляра метрики.</span><span class="sxs-lookup"><span data-stu-id="4db41-172">True if the **TimeStamp** value changes whenever the value of the metric instance changes.</span></span> <span data-ttu-id="4db41-173">Значение false, если этот объект должен оставаться неизменным, и новый объект, созданный для нового значения **timestamp** .</span><span class="sxs-lookup"><span data-stu-id="4db41-173">False if this object must remain unchanged and a new object created for the new **TimeStamp** value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4db41-174">Требования</span><span class="sxs-lookup"><span data-stu-id="4db41-174">Requirements</span></span>



| <span data-ttu-id="4db41-175">Требование</span><span class="sxs-lookup"><span data-stu-id="4db41-175">Requirement</span></span> | <span data-ttu-id="4db41-176">Значение</span><span class="sxs-lookup"><span data-stu-id="4db41-176">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4db41-177">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4db41-177">Minimum supported client</span></span><br/> | <span data-ttu-id="4db41-178">Windows 8</span><span class="sxs-lookup"><span data-stu-id="4db41-178">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="4db41-179">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4db41-179">Minimum supported server</span></span><br/> | <span data-ttu-id="4db41-180">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4db41-180">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="4db41-181">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="4db41-181">Namespace</span></span><br/>                | <span data-ttu-id="4db41-182">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="4db41-182">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="4db41-183">MOF</span><span class="sxs-lookup"><span data-stu-id="4db41-183">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4db41-184"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4db41-184"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4db41-185">DLL</span><span class="sxs-lookup"><span data-stu-id="4db41-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4db41-186"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4db41-186"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="4db41-187">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4db41-187">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4db41-188">**\_МАНАЖЕДЕЛЕМЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="4db41-188">**CIM\_ManagedElement**</span></span>](cim-managedelement.md)
</dt> </dl>

 

