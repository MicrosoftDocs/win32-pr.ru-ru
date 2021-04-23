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
# <a name="cim_metricservicecapabilities-class"></a><span data-ttu-id="54d0e-103">\_Класс CIM метриксервицекапабилитиес</span><span class="sxs-lookup"><span data-stu-id="54d0e-103">CIM\_MetricServiceCapabilities class</span></span>

<span data-ttu-id="54d0e-104">Описывает возможности объекта [**\_ метриксервице CIM**](cim-metricservice.md) .</span><span class="sxs-lookup"><span data-stu-id="54d0e-104">Describes the capabilities of a [**CIM\_MetricService**](cim-metricservice.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="54d0e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="54d0e-105">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="54d0e-106">Члены</span><span class="sxs-lookup"><span data-stu-id="54d0e-106">Members</span></span>

<span data-ttu-id="54d0e-107">Класс **CIM \_ метриксервицекапабилитиес** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="54d0e-107">The **CIM\_MetricServiceCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="54d0e-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="54d0e-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="54d0e-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="54d0e-109">Properties</span></span>

<span data-ttu-id="54d0e-110">Класс **CIM \_ метриксервицекапабилитиес** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="54d0e-110">The **CIM\_MetricServiceCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="54d0e-111">**контроллаблеманажеделементс**</span><span class="sxs-lookup"><span data-stu-id="54d0e-111">**ControllableManagedElements**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54d0e-112">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="54d0e-112">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="54d0e-113">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="54d0e-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="54d0e-114">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный"), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ метриксервицекапабилитиес**.**Манажеделементконтролтипес**")</span><span class="sxs-lookup"><span data-stu-id="54d0e-114">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_MetricServiceCapabilities**.**ManagedElementControlTypes**")</span></span>
</dt> </dl>

<span data-ttu-id="54d0e-115">Массив, содержащий идентификаторы экземпляров [**\_ манажеделемент CIM**](cim-managedelement.md) , управляемых службой метрик.</span><span class="sxs-lookup"><span data-stu-id="54d0e-115">An array that contains identifiers of the [**CIM\_ManagedElement**](cim-managedelement.md) instances that are controlled by the metric service.</span></span> <span data-ttu-id="54d0e-116">Идентификаторы должны быть отформатированы как URI Web-Based Enterprise Management (WBEM).</span><span class="sxs-lookup"><span data-stu-id="54d0e-116">The identifiers must be formatted as Web-Based Enterprise Management (WBEM) URIs.</span></span> <span data-ttu-id="54d0e-117">Чтобы использовать это свойство, служба метрик должна поддерживать включение или отключение по крайней мере одной метрики, определенной для экземпляра **CIM \_ манажеделемент** .</span><span class="sxs-lookup"><span data-stu-id="54d0e-117">In order to use this property, the metric service must support enabling or disabling at least one metric that is defined for the **CIM\_ManagedElement** instance.</span></span>

</dd> <dt>

<span data-ttu-id="54d0e-118">**контроллаблеметрикс**</span><span class="sxs-lookup"><span data-stu-id="54d0e-118">**ControllableMetrics**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54d0e-119">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="54d0e-119">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="54d0e-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="54d0e-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="54d0e-121">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный"), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ метриксервицекапабилитиес**.**Метрикконтролтипес**")</span><span class="sxs-lookup"><span data-stu-id="54d0e-121">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_MetricServiceCapabilities**.**MetricControlTypes**")</span></span>
</dt> </dl>

<span data-ttu-id="54d0e-122">Массив, содержащий идентификаторы [**CIM \_ басеметрикдефинитион**](cim-basemetricdefinition.md) , определяющие метрики, управляемые службой метрик.</span><span class="sxs-lookup"><span data-stu-id="54d0e-122">An array that contains identifiers of the [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) that defines the metrics that are managed by the metric service.</span></span> <span data-ttu-id="54d0e-123">Идентификаторы должны быть отформатированы как URI Web-Based Enterprise Management (WBEM).</span><span class="sxs-lookup"><span data-stu-id="54d0e-123">The identifiers must be formatted as Web-Based Enterprise Management (WBEM) URIs.</span></span>

<span data-ttu-id="54d0e-124">Чтобы использовать это свойство, экземпляр [**CIM \_ басеметрикдефинитион**](cim-basemetricdefinition.md) должен быть связан с экземпляром [**CIM \_ метриксервице**](cim-metricservice.md) через класс [**CIM \_ сервицеаффектселемент**](cim-serviceaffectselement.md) .</span><span class="sxs-lookup"><span data-stu-id="54d0e-124">In order to use this property, a [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) instance must be associated with a [**CIM\_MetricService**](cim-metricservice.md) instance through the [**CIM\_ServiceAffectsElement**](cim-serviceaffectselement.md) class.</span></span> <span data-ttu-id="54d0e-125">Кроме того, служба метрик должна поддерживать включение или отключение по крайней мере одной метрики, определенной экземпляром **CIM \_ басеметрикдефинитион** .</span><span class="sxs-lookup"><span data-stu-id="54d0e-125">In addition the metric service must support enabling or disabling at least one metric that is defined by the **CIM\_BaseMetricDefinition** instance.</span></span>

</dd> <dt>

<span data-ttu-id="54d0e-126">**манажеделементконтролтипес**</span><span class="sxs-lookup"><span data-stu-id="54d0e-126">**ManagedElementControlTypes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54d0e-127">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="54d0e-127">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="54d0e-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="54d0e-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="54d0e-129">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный"), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ метриксервицекапабилитиес**.**Контроллаблеманажеделементс**")</span><span class="sxs-lookup"><span data-stu-id="54d0e-129">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_MetricServiceCapabilities**.**ControllableManagedElements**")</span></span>
</dt> </dl>

<span data-ttu-id="54d0e-130">Массив, указывающий типы элементов управления, поддерживаемые службой метрик для управляемых элементов в массиве **контроллаблеманажеделементс** .</span><span class="sxs-lookup"><span data-stu-id="54d0e-130">An array that indicates the control types that are supported by the metric service for the managed elements in the **ControllableManagedElements** array.</span></span> <span data-ttu-id="54d0e-131">Этот массив соответствует массиву **контроллаблеманажеделементс** .</span><span class="sxs-lookup"><span data-stu-id="54d0e-131">This array corresponds to the **ControllableManagedElements** array.</span></span> <span data-ttu-id="54d0e-132">Типы элементов управления в этом массиве связаны с метриками через массив **контроллаблеманажеделементс** .</span><span class="sxs-lookup"><span data-stu-id="54d0e-132">The control types in this array are associated with metrics through the **ControllableManagedElements** array.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="54d0e-133">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="54d0e-133">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Discrete"></span><span id="discrete"></span><span id="DISCRETE"></span>

<span data-ttu-id="54d0e-134">**Дискретная** (2)</span><span class="sxs-lookup"><span data-stu-id="54d0e-134">**Discrete** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Bulk"></span><span id="bulk"></span><span id="BULK"></span>

<span data-ttu-id="54d0e-135">**Массовый** (3)</span><span class="sxs-lookup"><span data-stu-id="54d0e-135">**Bulk** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Both"></span><span id="both"></span><span id="BOTH"></span>

<span data-ttu-id="54d0e-136">**Оба** (4)</span><span class="sxs-lookup"><span data-stu-id="54d0e-136">**Both** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="54d0e-137">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="54d0e-137">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

<span data-ttu-id="54d0e-138">**Зависит от поставщика** (32768.65 535)</span><span class="sxs-lookup"><span data-stu-id="54d0e-138">**Vendor Specific** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="54d0e-139">**метриксконтролтипес**</span><span class="sxs-lookup"><span data-stu-id="54d0e-139">**MetricsControlTypes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54d0e-140">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="54d0e-140">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="54d0e-141">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="54d0e-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="54d0e-142">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный"), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ метриксервицекапабилитиес**.**Контроллаблеметрикс**")</span><span class="sxs-lookup"><span data-stu-id="54d0e-142">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_MetricServiceCapabilities**.**ControllableMetrics**")</span></span>
</dt> </dl>

<span data-ttu-id="54d0e-143">Массив, указывающий типы элементов управления, которые поддерживаются службой метрик.</span><span class="sxs-lookup"><span data-stu-id="54d0e-143">An array that indicates the control types that are supported by the metric service.</span></span> <span data-ttu-id="54d0e-144">Этот массив соответствует массиву **контроллаблеметрикс** .</span><span class="sxs-lookup"><span data-stu-id="54d0e-144">This array corresponds to the **ControllableMetrics** array.</span></span> <span data-ttu-id="54d0e-145">Типы элементов управления в этом массиве связаны с метриками через массив **контроллаблеметрикс** .</span><span class="sxs-lookup"><span data-stu-id="54d0e-145">The control types in this array are associated with metrics through the **ControllableMetrics** array.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="54d0e-146">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="54d0e-146">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Discrete"></span><span id="discrete"></span><span id="DISCRETE"></span>

<span data-ttu-id="54d0e-147">**Дискретная** (2)</span><span class="sxs-lookup"><span data-stu-id="54d0e-147">**Discrete** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Bulk"></span><span id="bulk"></span><span id="BULK"></span>

<span data-ttu-id="54d0e-148">**Массовый** (3)</span><span class="sxs-lookup"><span data-stu-id="54d0e-148">**Bulk** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Both"></span><span id="both"></span><span id="BOTH"></span>

<span data-ttu-id="54d0e-149">**Оба** (4)</span><span class="sxs-lookup"><span data-stu-id="54d0e-149">**Both** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="54d0e-150">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="54d0e-150">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

<span data-ttu-id="54d0e-151">**Зависит от поставщика** (32768.65 535)</span><span class="sxs-lookup"><span data-stu-id="54d0e-151">**Vendor Specific** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="54d0e-152">**SupportedMethods**</span><span class="sxs-lookup"><span data-stu-id="54d0e-152">**SupportedMethods**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54d0e-153">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="54d0e-153">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="54d0e-154">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="54d0e-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="54d0e-155">Массив, содержащий имена методов, поддерживаемых службой метрик.</span><span class="sxs-lookup"><span data-stu-id="54d0e-155">An array that contains names of methods that are supported by the metric service.</span></span>

<dt>

<span id="ControlMetrics"></span><span id="controlmetrics"></span><span id="CONTROLMETRICS"></span>

<span data-ttu-id="54d0e-156">**Контролметрикс** (2)</span><span class="sxs-lookup"><span data-stu-id="54d0e-156">**ControlMetrics** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="ControlMetricsByClass"></span><span id="controlmetricsbyclass"></span><span id="CONTROLMETRICSBYCLASS"></span>

<span data-ttu-id="54d0e-157">**Контролметриксбикласс** (3)</span><span class="sxs-lookup"><span data-stu-id="54d0e-157">**ControlMetricsByClass** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ShowMetrics"></span><span id="showmetrics"></span><span id="SHOWMETRICS"></span>

<span data-ttu-id="54d0e-158">**Шовметрикс** (4)</span><span class="sxs-lookup"><span data-stu-id="54d0e-158">**ShowMetrics** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="ShowMetricsByClass"></span><span id="showmetricsbyclass"></span><span id="SHOWMETRICSBYCLASS"></span>

<span data-ttu-id="54d0e-159">**Шовметриксбикласс** (5)</span><span class="sxs-lookup"><span data-stu-id="54d0e-159">**ShowMetricsByClass** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="GetMetricValues"></span><span id="getmetricvalues"></span><span id="GETMETRICVALUES"></span>

<span data-ttu-id="54d0e-160">**Жетметриквалуес** (6)</span><span class="sxs-lookup"><span data-stu-id="54d0e-160">**GetMetricValues** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="ControlSampleTimes"></span><span id="controlsampletimes"></span><span id="CONTROLSAMPLETIMES"></span>

<span data-ttu-id="54d0e-161">**Контролсамплетимес** (7)</span><span class="sxs-lookup"><span data-stu-id="54d0e-161">**ControlSampleTimes** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="54d0e-162">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="54d0e-162">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

<span data-ttu-id="54d0e-163">**Зависит от поставщика** (0x8000..)</span><span class="sxs-lookup"><span data-stu-id="54d0e-163">**Vendor Specific** (0x8000..)</span></span>


<span data-ttu-id="54d0e-164"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="54d0e-164"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="54d0e-165">Требования</span><span class="sxs-lookup"><span data-stu-id="54d0e-165">Requirements</span></span>



| <span data-ttu-id="54d0e-166">Требование</span><span class="sxs-lookup"><span data-stu-id="54d0e-166">Requirement</span></span> | <span data-ttu-id="54d0e-167">Значение</span><span class="sxs-lookup"><span data-stu-id="54d0e-167">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54d0e-168">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="54d0e-168">Minimum supported client</span></span><br/> | <span data-ttu-id="54d0e-169">Windows 8</span><span class="sxs-lookup"><span data-stu-id="54d0e-169">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="54d0e-170">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="54d0e-170">Minimum supported server</span></span><br/> | <span data-ttu-id="54d0e-171">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="54d0e-171">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="54d0e-172">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="54d0e-172">Namespace</span></span><br/>                | <span data-ttu-id="54d0e-173">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="54d0e-173">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="54d0e-174">MOF</span><span class="sxs-lookup"><span data-stu-id="54d0e-174">MOF</span></span><br/>                      | <dl> <span data-ttu-id="54d0e-175"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="54d0e-175"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="54d0e-176">DLL</span><span class="sxs-lookup"><span data-stu-id="54d0e-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="54d0e-177"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="54d0e-177"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="54d0e-178">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="54d0e-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54d0e-179">**\_ЕНАБЛЕДЛОГИКАЛЕЛЕМЕНТКАПАБИЛИТИЕС CIM**</span><span class="sxs-lookup"><span data-stu-id="54d0e-179">**CIM\_EnabledLogicalElementCapabilities**</span></span>](cim-enabledlogicalelementcapabilities.md)
</dt> </dl>

 

