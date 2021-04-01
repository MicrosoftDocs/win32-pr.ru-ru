---
description: Описывает возможности связанного \_ экземпляра мсвм метриксервице.
ms.assetid: 4E24D675-8265-4B5E-9551-550510B138FE
title: Класс Msvm_MetricServiceCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricServiceCapabilities
- Msvm_MetricServiceCapabilities.InstanceID
- Msvm_MetricServiceCapabilities.Caption
- Msvm_MetricServiceCapabilities.Description
- Msvm_MetricServiceCapabilities.ElementName
- Msvm_MetricServiceCapabilities.ElementNameEditSupported
- Msvm_MetricServiceCapabilities.MaxElementNameLen
- Msvm_MetricServiceCapabilities.RequestedStatesSupported
- Msvm_MetricServiceCapabilities.ElementNameMask
- Msvm_MetricServiceCapabilities.ControllableMetrics
- Msvm_MetricServiceCapabilities.MetricsControlTypes
- Msvm_MetricServiceCapabilities.ControllableManagedElements
- Msvm_MetricServiceCapabilities.ManagedElementControlTypes
- Msvm_MetricServiceCapabilities.SupportedMethods
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 635e153d3184e74ea581a045e3d6d54a5fea199f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913119"
---
# <a name="msvm_metricservicecapabilities-class"></a><span data-ttu-id="ef533-103">\_Класс мсвм метриксервицекапабилитиес</span><span class="sxs-lookup"><span data-stu-id="ef533-103">Msvm\_MetricServiceCapabilities class</span></span>

<span data-ttu-id="ef533-104">Описывает возможности связанного экземпляра [**мсвм \_ метриксервице**](msvm-metricservice.md) .</span><span class="sxs-lookup"><span data-stu-id="ef533-104">Describes the capabilities of the associated [**Msvm\_MetricService**](msvm-metricservice.md) instance.</span></span>

<span data-ttu-id="ef533-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="ef533-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef533-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ef533-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MetricServiceCapabilities : CIM_MetricServiceCapabilities
{
  string  InstanceID;
  string  Caption = "Hyper-V Metric Service Capabilities";
  string  Description = "Defines Hyper-V Metric Service Capabilities";
  string  ElementName = "Hyper-V Metric Service Capabilities";
  boolean ElementNameEditSupported;
  unit16  MaxElementNameLen;
  unit16  RequestedStatesSupported[];
  string  ElementNameMask;
  string  ControllableMetrics[];
  uint16  MetricsControlTypes[];
  string  ControllableManagedElements[];
  uint16  ManagedElementControlTypes[];
  uint16  SupportedMethods[];
};
```

## <a name="members"></a><span data-ttu-id="ef533-107">Члены</span><span class="sxs-lookup"><span data-stu-id="ef533-107">Members</span></span>

<span data-ttu-id="ef533-108">Класс **мсвм \_ метриксервицекапабилитиес** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="ef533-108">The **Msvm\_MetricServiceCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="ef533-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="ef533-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ef533-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="ef533-110">Properties</span></span>

<span data-ttu-id="ef533-111">Класс **мсвм \_ метриксервицекапабилитиес** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="ef533-111">The **Msvm\_MetricServiceCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ef533-112">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="ef533-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef533-113">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ef533-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef533-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ef533-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef533-115">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="ef533-115">A short description of the object.</span></span> <span data-ttu-id="ef533-116">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "возможности службы метрик Hyper-V".</span><span class="sxs-lookup"><span data-stu-id="ef533-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Metric Service Capabilities".</span></span>

</dd> <dt>

<span data-ttu-id="ef533-117">**контроллаблеманажеделементс**</span><span class="sxs-lookup"><span data-stu-id="ef533-117">**ControllableManagedElements**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef533-118">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="ef533-118">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ef533-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ef533-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef533-120">Квалификаторы: **arrayType** ("индексированный")</span><span class="sxs-lookup"><span data-stu-id="ef533-120">Qualifiers: **ArrayType** ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="ef533-121">Определяет экземпляры [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) , которые могут управляться связанным экземпляром **CIM \_ метриксервице** .</span><span class="sxs-lookup"><span data-stu-id="ef533-121">Identifies the instances of [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) that can be controlled by the associated **CIM\_MetricService** instance.</span></span> <span data-ttu-id="ef533-122">Если это свойство имеет **значение NULL**, можно управлять всеми элементами.</span><span class="sxs-lookup"><span data-stu-id="ef533-122">If this property is **Null**, all elements can be controlled.</span></span> <span data-ttu-id="ef533-123">Это свойство наследуется от **CIM \_ метриксервицекапабилитиес**.</span><span class="sxs-lookup"><span data-stu-id="ef533-123">This property is inherited from **CIM\_MetricServiceCapabilities**.</span></span>

</dd> <dt>

<span data-ttu-id="ef533-124">**контроллаблеметрикс**</span><span class="sxs-lookup"><span data-stu-id="ef533-124">**ControllableMetrics**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef533-125">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="ef533-125">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ef533-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ef533-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef533-127">Квалификаторы: **arrayType** ("индексированный")</span><span class="sxs-lookup"><span data-stu-id="ef533-127">Qualifiers: **ArrayType** ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="ef533-128">Определяет экземпляры **CIM \_ басеметрикдефинитион** , которые могут управляться связанным экземпляром **CIM \_ метриксервице** .</span><span class="sxs-lookup"><span data-stu-id="ef533-128">Identifies the instances of **CIM\_BaseMetricDefinition** that can be controlled by the associated **CIM\_MetricService** instance.</span></span> <span data-ttu-id="ef533-129">Если это свойство имеет **значение NULL**, можно управлять всеми метриками.</span><span class="sxs-lookup"><span data-stu-id="ef533-129">If this property is **Null**, all metrics can be controlled.</span></span> <span data-ttu-id="ef533-130">Это свойство наследуется от **CIM \_ метриксервицекапабилитиес**.</span><span class="sxs-lookup"><span data-stu-id="ef533-130">This property is inherited from **CIM\_MetricServiceCapabilities**.</span></span>

</dd> <dt>

<span data-ttu-id="ef533-131">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ef533-131">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef533-132">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ef533-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef533-133">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ef533-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef533-134">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="ef533-134">A description of the object.</span></span> <span data-ttu-id="ef533-135">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "определяет возможности службы метрик Hyper-V".</span><span class="sxs-lookup"><span data-stu-id="ef533-135">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Defines Hyper-V Metric Service Capabilities".</span></span>

</dd> <dt>

<span data-ttu-id="ef533-136">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="ef533-136">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef533-137">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ef533-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef533-138">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ef533-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef533-139">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="ef533-139">A display name for the object.</span></span> <span data-ttu-id="ef533-140">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "возможности службы метрик Hyper-V".</span><span class="sxs-lookup"><span data-stu-id="ef533-140">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Metric Service Capabilities".</span></span>

</dd> <dt>

<span data-ttu-id="ef533-141">**елементнамидитсуппортед**</span><span class="sxs-lookup"><span data-stu-id="ef533-141">**ElementNameEditSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef533-142">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="ef533-142">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ef533-143">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ef533-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef533-144">Указывает, можно ли изменить свойство **ElementName** .</span><span class="sxs-lookup"><span data-stu-id="ef533-144">Indicates whether the **ElementName** property can be modified.</span></span> <span data-ttu-id="ef533-145">Это свойство наследуется от **CIM \_ енабледлогикалелементкапабилитиес**.</span><span class="sxs-lookup"><span data-stu-id="ef533-145">This property is inherited from **CIM\_EnabledLogicalElementCapabilities**.</span></span>

</dd> <dt>

<span data-ttu-id="ef533-146">**елементнамемаск**</span><span class="sxs-lookup"><span data-stu-id="ef533-146">**ElementNameMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef533-147">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ef533-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef533-148">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ef533-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef533-149">Задает ограничения для **ElementName**, выраженные в виде регулярного выражения.</span><span class="sxs-lookup"><span data-stu-id="ef533-149">Specifies the restrictions on **ElementName**, expressed as a regular expression.</span></span> <span data-ttu-id="ef533-150">Это свойство наследуется от **CIM \_ енабледлогикалелементкапабилитиес**.</span><span class="sxs-lookup"><span data-stu-id="ef533-150">This property is inherited from **CIM\_EnabledLogicalElementCapabilities**.</span></span>

</dd> <dt>

<span data-ttu-id="ef533-151">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="ef533-151">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef533-152">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ef533-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef533-153">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ef533-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef533-154">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="ef533-154">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="ef533-155">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="ef533-155">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="ef533-156">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="ef533-156">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="ef533-157">**манажеделементконтролтипес**</span><span class="sxs-lookup"><span data-stu-id="ef533-157">**ManagedElementControlTypes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef533-158">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="ef533-158">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ef533-159">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ef533-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef533-160">Квалификаторы: **arrayType** ("индексированный")</span><span class="sxs-lookup"><span data-stu-id="ef533-160">Qualifiers: **ArrayType** ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="ef533-161">Определяет тип элемента управления, поддерживаемого связанным экземпляром **CIM \_ метриксервице** для объекта [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) , идентифицируемого значением по тому же индексу массива в свойстве **контроллаблеманажеделементс** .</span><span class="sxs-lookup"><span data-stu-id="ef533-161">Identifies the type of control supported by the associated **CIM\_MetricService** instance for the [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) object identified by the value at the same array index in the **ControllableManagedElements** property.</span></span> <span data-ttu-id="ef533-162">Если это свойство имеет **значение NULL**, поддерживаются все типы элементов управления.</span><span class="sxs-lookup"><span data-stu-id="ef533-162">If this property is **Null**, all control types are supported.</span></span> <span data-ttu-id="ef533-163">Это свойство наследуется от **CIM \_ метриксервицекапабилитиес**.</span><span class="sxs-lookup"><span data-stu-id="ef533-163">This property is inherited from **CIM\_MetricServiceCapabilities**.</span></span>



| <span data-ttu-id="ef533-164">Значение</span><span class="sxs-lookup"><span data-stu-id="ef533-164">Value</span></span>                                                                                   | <span data-ttu-id="ef533-165">Значение</span><span class="sxs-lookup"><span data-stu-id="ef533-165">Meaning</span></span>                    |
|-----------------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="ef533-166"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="ef533-166"><dt>0</dt></span></span> </dl>            | <span data-ttu-id="ef533-167">Неизвестно</span><span class="sxs-lookup"><span data-stu-id="ef533-167">Unknown</span></span><br/>         |
| <dl> <span data-ttu-id="ef533-168"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="ef533-168"><dt>2</dt></span></span> </dl>            | <span data-ttu-id="ef533-169">Discrete</span><span class="sxs-lookup"><span data-stu-id="ef533-169">Discrete</span></span><br/>        |
| <dl> <span data-ttu-id="ef533-170"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="ef533-170"><dt>3</dt></span></span> </dl>            | <span data-ttu-id="ef533-171">Массовость</span><span class="sxs-lookup"><span data-stu-id="ef533-171">Bulk</span></span><br/>            |
| <dl> <span data-ttu-id="ef533-172"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="ef533-172"><dt>4</dt></span></span> </dl>            | <span data-ttu-id="ef533-173">Оба</span><span class="sxs-lookup"><span data-stu-id="ef533-173">Both</span></span><br/>            |
| <dl> <span data-ttu-id="ef533-174"><dt>5.. 32767</dt></span><span class="sxs-lookup"><span data-stu-id="ef533-174"><dt>5..32767</dt></span></span> </dl>     | <span data-ttu-id="ef533-175">Зарезервировано DMTF</span><span class="sxs-lookup"><span data-stu-id="ef533-175">DMTF reserved</span></span><br/>   |
| <dl> <span data-ttu-id="ef533-176"><dt>32768.. 65535</dt></span><span class="sxs-lookup"><span data-stu-id="ef533-176"><dt>32768..65535</dt></span></span> </dl> | <span data-ttu-id="ef533-177">Зависит от поставщика</span><span class="sxs-lookup"><span data-stu-id="ef533-177">Vendor specific</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="ef533-178">**макселементнамелен**</span><span class="sxs-lookup"><span data-stu-id="ef533-178">**MaxElementNameLen**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef533-179">Тип данных: **unit16**</span><span class="sxs-lookup"><span data-stu-id="ef533-179">Data type: **unit16**</span></span>
</dt> <dt>

<span data-ttu-id="ef533-180">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ef533-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef533-181">Квалификаторы: **MaxValue** (256)</span><span class="sxs-lookup"><span data-stu-id="ef533-181">Qualifiers: **MaxValue** (256)</span></span>
</dt> </dl>

<span data-ttu-id="ef533-182">Задает максимальную поддерживаемую длину свойства **ElementName** .</span><span class="sxs-lookup"><span data-stu-id="ef533-182">Specifies the maximum supported length of the **ElementName** property.</span></span> <span data-ttu-id="ef533-183">Это свойство наследуется от **CIM \_ енабледлогикалелементкапабилитиес**.</span><span class="sxs-lookup"><span data-stu-id="ef533-183">This property is inherited from **CIM\_EnabledLogicalElementCapabilities**.</span></span>

</dd> <dt>

<span data-ttu-id="ef533-184">**метриксконтролтипес**</span><span class="sxs-lookup"><span data-stu-id="ef533-184">**MetricsControlTypes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef533-185">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="ef533-185">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ef533-186">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ef533-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef533-187">Квалификаторы: **arrayType** ("индексированный")</span><span class="sxs-lookup"><span data-stu-id="ef533-187">Qualifiers: **ArrayType** ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="ef533-188">Определяет тип элемента управления, поддерживаемого связанным экземпляром **CIM \_ метриксервице** для **\_ басеметрикдефинитион CIM** , идентифицируемого значением по тому же индексу массива в свойстве **контроллаблеметрикс** .</span><span class="sxs-lookup"><span data-stu-id="ef533-188">Identifies the type of control supported by the associated **CIM\_MetricService** instance for the **CIM\_BaseMetricDefinition** identified by the value at the same array index in the **ControllableMetrics** property.</span></span> <span data-ttu-id="ef533-189">Если это свойство имеет **значение NULL**, поддерживаются все типы элементов управления.</span><span class="sxs-lookup"><span data-stu-id="ef533-189">If this property is **Null**, all control types are supported.</span></span> <span data-ttu-id="ef533-190">Это свойство наследуется от **CIM \_ метриксервицекапабилитиес**.</span><span class="sxs-lookup"><span data-stu-id="ef533-190">This property is inherited from **CIM\_MetricServiceCapabilities**.</span></span>



| <span data-ttu-id="ef533-191">Значение</span><span class="sxs-lookup"><span data-stu-id="ef533-191">Value</span></span>                                                                                   | <span data-ttu-id="ef533-192">Значение</span><span class="sxs-lookup"><span data-stu-id="ef533-192">Meaning</span></span>                    |
|-----------------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="ef533-193"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="ef533-193"><dt>0</dt></span></span> </dl>            | <span data-ttu-id="ef533-194">Неизвестно</span><span class="sxs-lookup"><span data-stu-id="ef533-194">Unknown</span></span><br/>         |
| <dl> <span data-ttu-id="ef533-195"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="ef533-195"><dt>2</dt></span></span> </dl>            | <span data-ttu-id="ef533-196">Discrete</span><span class="sxs-lookup"><span data-stu-id="ef533-196">Discrete</span></span><br/>        |
| <dl> <span data-ttu-id="ef533-197"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="ef533-197"><dt>3</dt></span></span> </dl>            | <span data-ttu-id="ef533-198">Массовость</span><span class="sxs-lookup"><span data-stu-id="ef533-198">Bulk</span></span><br/>            |
| <dl> <span data-ttu-id="ef533-199"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="ef533-199"><dt>4</dt></span></span> </dl>            | <span data-ttu-id="ef533-200">Оба</span><span class="sxs-lookup"><span data-stu-id="ef533-200">Both</span></span><br/>            |
| <dl> <span data-ttu-id="ef533-201"><dt>5.. 32767</dt></span><span class="sxs-lookup"><span data-stu-id="ef533-201"><dt>5..32767</dt></span></span> </dl>     | <span data-ttu-id="ef533-202">Зарезервировано DMTF</span><span class="sxs-lookup"><span data-stu-id="ef533-202">DMTF reserved</span></span><br/>   |
| <dl> <span data-ttu-id="ef533-203"><dt>32768.. 65535</dt></span><span class="sxs-lookup"><span data-stu-id="ef533-203"><dt>32768..65535</dt></span></span> </dl> | <span data-ttu-id="ef533-204">Зависит от поставщика</span><span class="sxs-lookup"><span data-stu-id="ef533-204">Vendor specific</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="ef533-205">**рекуестедстатессуппортед**</span><span class="sxs-lookup"><span data-stu-id="ef533-205">**RequestedStatesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef533-206">Тип данных: массив **unit16**</span><span class="sxs-lookup"><span data-stu-id="ef533-206">Data type: **unit16** array</span></span>
</dt> <dt>

<span data-ttu-id="ef533-207">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ef533-207">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef533-208">Указывает возможные состояния, которые могут быть запрошены при использовании метода **RequestStateChange** для включенного логического элемента.</span><span class="sxs-lookup"><span data-stu-id="ef533-208">Indicates the possible states that can be requested when using the **RequestStateChange** method on the enabled logical element.</span></span> <span data-ttu-id="ef533-209">Это свойство наследуется от **CIM \_ енабледлогикалелементкапабилитиес**.</span><span class="sxs-lookup"><span data-stu-id="ef533-209">This property is inherited from **CIM\_EnabledLogicalElementCapabilities**.</span></span>



| <span data-ttu-id="ef533-210">Значение</span><span class="sxs-lookup"><span data-stu-id="ef533-210">Value</span></span>                                                                         | <span data-ttu-id="ef533-211">Значение</span><span class="sxs-lookup"><span data-stu-id="ef533-211">Meaning</span></span>              |
|-------------------------------------------------------------------------------|----------------------|
| <dl> <span data-ttu-id="ef533-212"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="ef533-212"><dt>2</dt></span></span> </dl>  | <span data-ttu-id="ef533-213">Активировано</span><span class="sxs-lookup"><span data-stu-id="ef533-213">Enabled</span></span><br/>   |
| <dl> <span data-ttu-id="ef533-214"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="ef533-214"><dt>3</dt></span></span> </dl>  | <span data-ttu-id="ef533-215">Отключит</span><span class="sxs-lookup"><span data-stu-id="ef533-215">Disables</span></span><br/>  |
| <dl> <span data-ttu-id="ef533-216"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="ef533-216"><dt>4</dt></span></span> </dl>  | <span data-ttu-id="ef533-217">Завершение работы</span><span class="sxs-lookup"><span data-stu-id="ef533-217">Shut Down</span></span><br/> |
| <dl> <span data-ttu-id="ef533-218"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="ef533-218"><dt>6</dt></span></span> </dl>  | <span data-ttu-id="ef533-219">Автономная миграция</span><span class="sxs-lookup"><span data-stu-id="ef533-219">Offline</span></span><br/>   |
| <dl> <span data-ttu-id="ef533-220"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="ef533-220"><dt>7</dt></span></span> </dl>  | <span data-ttu-id="ef533-221">Тест</span><span class="sxs-lookup"><span data-stu-id="ef533-221">Test</span></span><br/>      |
| <dl> <span data-ttu-id="ef533-222"><dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="ef533-222"><dt>8</dt></span></span> </dl>  | <span data-ttu-id="ef533-223">Которого</span><span class="sxs-lookup"><span data-stu-id="ef533-223">Defer</span></span><br/>     |
| <dl> <span data-ttu-id="ef533-224"><dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="ef533-224"><dt>9</dt></span></span> </dl>  | <span data-ttu-id="ef533-225">Замораживани</span><span class="sxs-lookup"><span data-stu-id="ef533-225">Quiesce</span></span><br/>   |
| <dl> <span data-ttu-id="ef533-226"><dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="ef533-226"><dt>10</dt></span></span> </dl> | <span data-ttu-id="ef533-227">Перезагрузка</span><span class="sxs-lookup"><span data-stu-id="ef533-227">Reboot</span></span><br/>    |
| <dl> <span data-ttu-id="ef533-228"><dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="ef533-228"><dt>11</dt></span></span> </dl> | <span data-ttu-id="ef533-229">Reset</span><span class="sxs-lookup"><span data-stu-id="ef533-229">Reset</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="ef533-230">**SupportedMethods**</span><span class="sxs-lookup"><span data-stu-id="ef533-230">**SupportedMethods**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef533-231">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="ef533-231">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ef533-232">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ef533-232">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef533-233">Указывает методы, поддерживаемые службой метрики.</span><span class="sxs-lookup"><span data-stu-id="ef533-233">Specifies the methods supported by the metric service.</span></span> <span data-ttu-id="ef533-234">Это свойство наследуется от **CIM \_ метриксервицекапабилитиес**.</span><span class="sxs-lookup"><span data-stu-id="ef533-234">This property is inherited from **CIM\_MetricServiceCapabilities**.</span></span>



| <span data-ttu-id="ef533-235">Значение</span><span class="sxs-lookup"><span data-stu-id="ef533-235">Value</span></span>                                                                                   | <span data-ttu-id="ef533-236">Значение</span><span class="sxs-lookup"><span data-stu-id="ef533-236">Meaning</span></span>                                                                                         |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ef533-237"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="ef533-237"><dt>2</dt></span></span> </dl>            | <span data-ttu-id="ef533-238">Поддерживается метод [**контролметрикс**](controlmetrics-msvm-metricservice.md) .</span><span class="sxs-lookup"><span data-stu-id="ef533-238">The [**ControlMetrics**](controlmetrics-msvm-metricservice.md) method is supported.</span></span><br/> |
| <dl> <span data-ttu-id="ef533-239"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="ef533-239"><dt>3</dt></span></span> </dl>            | <span data-ttu-id="ef533-240">Поддерживается метод **контролметриксбикласс** .</span><span class="sxs-lookup"><span data-stu-id="ef533-240">The **ControlMetricsByClass** method is supported.</span></span><br/>                                   |
| <dl> <span data-ttu-id="ef533-241"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="ef533-241"><dt>4</dt></span></span> </dl>            | <span data-ttu-id="ef533-242">Поддерживается метод **шовметрикс** .</span><span class="sxs-lookup"><span data-stu-id="ef533-242">The **ShowMetrics** method is supported.</span></span><br/>                                             |
| <dl> <span data-ttu-id="ef533-243"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="ef533-243"><dt>5</dt></span></span> </dl>            | <span data-ttu-id="ef533-244">Поддерживается метод **шовметриксбикласс** .</span><span class="sxs-lookup"><span data-stu-id="ef533-244">The **ShowMetricsByClass** method is supported.</span></span><br/>                                      |
| <dl> <span data-ttu-id="ef533-245"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="ef533-245"><dt>6</dt></span></span> </dl>            | <span data-ttu-id="ef533-246">Поддерживается метод **жетметриквалуес** .</span><span class="sxs-lookup"><span data-stu-id="ef533-246">The **GetMetricValues** method is supported.</span></span><br/>                                         |
| <dl> <span data-ttu-id="ef533-247"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="ef533-247"><dt>7</dt></span></span> </dl>            | <span data-ttu-id="ef533-248">Поддерживается метод **контролсамплетимес** .</span><span class="sxs-lookup"><span data-stu-id="ef533-248">The **ControlSampleTimes** method is supported.</span></span><br/>                                      |
| <dl> <span data-ttu-id="ef533-249"><dt>8.. 32767</dt></span><span class="sxs-lookup"><span data-stu-id="ef533-249"><dt>8..32767</dt></span></span> </dl>     | <span data-ttu-id="ef533-250">Зарезервировано DMTF</span><span class="sxs-lookup"><span data-stu-id="ef533-250">DMTF reserved</span></span><br/>                                                                        |
| <dl> <span data-ttu-id="ef533-251"><dt>32768.. 65535</dt></span><span class="sxs-lookup"><span data-stu-id="ef533-251"><dt>32768..65535</dt></span></span> </dl> | <span data-ttu-id="ef533-252">Зависит от поставщика</span><span class="sxs-lookup"><span data-stu-id="ef533-252">Vendor specific</span></span><br/>                                                                      |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ef533-253">Требования</span><span class="sxs-lookup"><span data-stu-id="ef533-253">Requirements</span></span>



| <span data-ttu-id="ef533-254">Требование</span><span class="sxs-lookup"><span data-stu-id="ef533-254">Requirement</span></span> | <span data-ttu-id="ef533-255">Значение</span><span class="sxs-lookup"><span data-stu-id="ef533-255">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef533-256">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ef533-256">Minimum supported client</span></span><br/> | <span data-ttu-id="ef533-257">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="ef533-257">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="ef533-258">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ef533-258">Minimum supported server</span></span><br/> | <span data-ttu-id="ef533-259">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="ef533-259">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ef533-260">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="ef533-260">Namespace</span></span><br/>                | <span data-ttu-id="ef533-261">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="ef533-261">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="ef533-262">MOF</span><span class="sxs-lookup"><span data-stu-id="ef533-262">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ef533-263"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ef533-263"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ef533-264">DLL</span><span class="sxs-lookup"><span data-stu-id="ef533-264">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ef533-265"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ef533-265"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ef533-266">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ef533-266">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef533-267">**\_МЕТРИКСЕРВИЦЕКАПАБИЛИТИЕС CIM**</span><span class="sxs-lookup"><span data-stu-id="ef533-267">**CIM\_MetricServiceCapabilities**</span></span>](cim-metricservicecapabilities.md)
</dt> <dt>

[<span data-ttu-id="ef533-268">**Мсвм \_ метриксервице**</span><span class="sxs-lookup"><span data-stu-id="ef533-268">**Msvm\_MetricService**</span></span>](msvm-metricservice.md)
</dt> </dl>

 

