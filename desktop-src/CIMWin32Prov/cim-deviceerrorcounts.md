---
description: Класс CIM \_ девицеерроркаунтс является статистическим классом, который содержит счетчики, связанные с ошибками для логического устройства. Типы ошибок определяются с помощью CCITT (REC X. 733) и ISO (IEC 10164-4).
ms.assetid: d65cbc78-40f2-4846-bd47-76e04b2f588b
ms.tgt_platform: multiple
title: Класс CIM_DeviceErrorCounts
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceErrorCounts
- CIM_DeviceErrorCounts.Caption
- CIM_DeviceErrorCounts.Description
- CIM_DeviceErrorCounts.CriticalErrorCount
- CIM_DeviceErrorCounts.DeviceCreationClassName
- CIM_DeviceErrorCounts.DeviceID
- CIM_DeviceErrorCounts.Name
- CIM_DeviceErrorCounts.IndeterminateErrorCount
- CIM_DeviceErrorCounts.MajorErrorCount
- CIM_DeviceErrorCounts.MinorErrorCount
- CIM_DeviceErrorCounts.SystemCreationClassName
- CIM_DeviceErrorCounts.SystemName
- CIM_DeviceErrorCounts.WarningCount
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1602e68b7254811ba8c09726feda8baa7bf23d29
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990666"
---
# <a name="cim_deviceerrorcounts-class"></a><span data-ttu-id="cec15-104">\_Класс CIM девицеерроркаунтс</span><span class="sxs-lookup"><span data-stu-id="cec15-104">CIM\_DeviceErrorCounts class</span></span>

<span data-ttu-id="cec15-105">Класс **CIM \_ девицеерроркаунтс** является статистическим классом, который содержит счетчики, связанные с ошибками для логического устройства.</span><span class="sxs-lookup"><span data-stu-id="cec15-105">The **CIM\_DeviceErrorCounts** class is a statistical class that contains error-related counters for a logical device.</span></span> <span data-ttu-id="cec15-106">Типы ошибок определяются с помощью CCITT (REC X. 733) и ISO (IEC 10164-4).</span><span class="sxs-lookup"><span data-stu-id="cec15-106">The types of errors are defined by CCITT (Rec X.733) and ISO (IEC 10164-4).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cec15-107">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="cec15-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="cec15-108">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="cec15-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="cec15-109">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="cec15-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="cec15-110">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="cec15-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="cec15-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cec15-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{117FDB8C-D025-11d2-85F5-0000F8102E5F}"), AMENDMENT]
class CIM_DeviceErrorCounts : CIM_StatisticalInformation
{
  string Caption;
  string Description;
  uint64 CriticalErrorCount;
  string DeviceCreationClassName;
  string DeviceID;
  string Name;
  uint64 IndeterminateErrorCount;
  uint64 MajorErrorCount;
  uint64 MinorErrorCount;
  string SystemCreationClassName;
  string SystemName;
  uint64 WarningCount;
};
```

## <a name="members"></a><span data-ttu-id="cec15-112">Члены</span><span class="sxs-lookup"><span data-stu-id="cec15-112">Members</span></span>

<span data-ttu-id="cec15-113">Класс **CIM \_ девицеерроркаунтс** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="cec15-113">The **CIM\_DeviceErrorCounts** class has these types of members:</span></span>

-   [<span data-ttu-id="cec15-114">Методы</span><span class="sxs-lookup"><span data-stu-id="cec15-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="cec15-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="cec15-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="cec15-116">Методы</span><span class="sxs-lookup"><span data-stu-id="cec15-116">Methods</span></span>

<span data-ttu-id="cec15-117">Класс **CIM \_ девицеерроркаунтс** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="cec15-117">The **CIM\_DeviceErrorCounts** class has these methods.</span></span>



| <span data-ttu-id="cec15-118">Метод</span><span class="sxs-lookup"><span data-stu-id="cec15-118">Method</span></span>                                                                     | <span data-ttu-id="cec15-119">Описание</span><span class="sxs-lookup"><span data-stu-id="cec15-119">Description</span></span>                                                               |
|:---------------------------------------------------------------------------|:--------------------------------------------------------------------------|
| [<span data-ttu-id="cec15-120">**ресеткаунтер**</span><span class="sxs-lookup"><span data-stu-id="cec15-120">**ResetCounter**</span></span>](resetcounter-method-in-class-cim-deviceerrorcounts.md) | <span data-ttu-id="cec15-121">Сбрасывает счетчики ошибок и предупреждений.</span><span class="sxs-lookup"><span data-stu-id="cec15-121">Resets the error and warning counters.</span></span> <span data-ttu-id="cec15-122">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="cec15-122">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="cec15-123">Свойства</span><span class="sxs-lookup"><span data-stu-id="cec15-123">Properties</span></span>

<span data-ttu-id="cec15-124">Класс **CIM \_ девицеерроркаунтс** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="cec15-124">The **CIM\_DeviceErrorCounts** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cec15-125">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="cec15-125">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cec15-126">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="cec15-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cec15-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cec15-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cec15-128">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="cec15-128">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="cec15-129">Краткое текстовое описание для статистики или метрики.</span><span class="sxs-lookup"><span data-stu-id="cec15-129">Short textual description for the statistic or metric.</span></span>

<span data-ttu-id="cec15-130">Это свойство наследуется от [**CIM \_ статистикалинформатион**](cim-statisticalinformation.md).</span><span class="sxs-lookup"><span data-stu-id="cec15-130">This property is inherited from [**CIM\_StatisticalInformation**](cim-statisticalinformation.md).</span></span>

</dd> <dt>

<span data-ttu-id="cec15-131">**Criticalerrorcount единицей**</span><span class="sxs-lookup"><span data-stu-id="cec15-131">**CriticalErrorCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cec15-132">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="cec15-132">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="cec15-133">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cec15-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cec15-134">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Рабочее состояние DMTF \| 003,7 ")</span><span class="sxs-lookup"><span data-stu-id="cec15-134">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.7")</span></span>
</dt> </dl>

<span data-ttu-id="cec15-135">Количество критических ошибок.</span><span class="sxs-lookup"><span data-stu-id="cec15-135">Count of the critical errors.</span></span>

<span data-ttu-id="cec15-136">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="cec15-136">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="cec15-137">**Описание**</span><span class="sxs-lookup"><span data-stu-id="cec15-137">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cec15-138">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="cec15-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cec15-139">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cec15-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cec15-140">Текстовое описание статистики или метрики.</span><span class="sxs-lookup"><span data-stu-id="cec15-140">Textual description of the statistic or metric.</span></span>

<span data-ttu-id="cec15-141">Это свойство наследуется от [**CIM \_ статистикалинформатион**](cim-statisticalinformation.md).</span><span class="sxs-lookup"><span data-stu-id="cec15-141">This property is inherited from [**CIM\_StatisticalInformation**](cim-statisticalinformation.md).</span></span>

</dd> <dt>

<span data-ttu-id="cec15-142">**девицекреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="cec15-142">**DeviceCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cec15-143">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="cec15-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cec15-144">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cec15-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cec15-145">Квалификаторы: распространяются ("[**CIM- \_**](cim-logicaldevice.md) [**унаследованный**](/windows/desktop/WmiSdk/standard-qualifiers) ".**CreationClassName**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="cec15-145">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_LogicalDevice**](cim-logicaldevice.md).**CreationClassName**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="cec15-146">Свойство **CreationClassName** устройства в области.</span><span class="sxs-lookup"><span data-stu-id="cec15-146">The scoping device's **CreationClassName** property.</span></span>

</dd> <dt>

<span data-ttu-id="cec15-147">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="cec15-147">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cec15-148">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="cec15-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cec15-149">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cec15-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cec15-150">Квалификаторы: распространяются ("[**CIM- \_**](cim-logicaldevice.md) [**унаследованный**](/windows/desktop/WmiSdk/standard-qualifiers) ".**DeviceID**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="cec15-150">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_LogicalDevice**](cim-logicaldevice.md).**DeviceID**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="cec15-151">Идентификатор устройства в области.</span><span class="sxs-lookup"><span data-stu-id="cec15-151">The scoping device's identifier.</span></span>

</dd> <dt>

<span data-ttu-id="cec15-152">**индетерминатирроркаунт**</span><span class="sxs-lookup"><span data-stu-id="cec15-152">**IndeterminateErrorCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cec15-153">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="cec15-153">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="cec15-154">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cec15-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cec15-155">Количество неопределенных ошибок.</span><span class="sxs-lookup"><span data-stu-id="cec15-155">Count of the indeterminate errors.</span></span>

<span data-ttu-id="cec15-156">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="cec15-156">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="cec15-157">**мажорерроркаунт**</span><span class="sxs-lookup"><span data-stu-id="cec15-157">**MajorErrorCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cec15-158">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="cec15-158">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="cec15-159">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cec15-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cec15-160">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Рабочее состояние DMTF \| 003,8 ")</span><span class="sxs-lookup"><span data-stu-id="cec15-160">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.8")</span></span>
</dt> </dl>

<span data-ttu-id="cec15-161">Количество основных ошибок.</span><span class="sxs-lookup"><span data-stu-id="cec15-161">Count of the major errors.</span></span>

<span data-ttu-id="cec15-162">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="cec15-162">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="cec15-163">**минорерроркаунт**</span><span class="sxs-lookup"><span data-stu-id="cec15-163">**MinorErrorCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cec15-164">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="cec15-164">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="cec15-165">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cec15-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cec15-166">Количество незначительных ошибок.</span><span class="sxs-lookup"><span data-stu-id="cec15-166">Count of the minor errors.</span></span>

<span data-ttu-id="cec15-167">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="cec15-167">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="cec15-168">**Name**</span><span class="sxs-lookup"><span data-stu-id="cec15-168">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cec15-169">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="cec15-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cec15-170">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cec15-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cec15-171">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="cec15-171">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="cec15-172">Унаследованное свойство Name служит частью ключа для экземпляра **CIM \_ девицеерроркаунтс** .</span><span class="sxs-lookup"><span data-stu-id="cec15-172">The inherited Name property serves as part of the key for the **CIM\_DeviceErrorCounts** instance.</span></span> <span data-ttu-id="cec15-173">Объект ограничивается логическим устройством, к которому применяется статистика.</span><span class="sxs-lookup"><span data-stu-id="cec15-173">The object is scoped by the logical device to which the statistics apply.</span></span>

</dd> <dt>

<span data-ttu-id="cec15-174">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="cec15-174">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cec15-175">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="cec15-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cec15-176">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cec15-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cec15-177">Квалификаторы: распространяются ("[**CIM- \_**](cim-logicaldevice.md) [**унаследованный**](/windows/desktop/WmiSdk/standard-qualifiers) ".**Системкреатионкласснаме**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="cec15-177">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_LogicalDevice**](cim-logicaldevice.md).**SystemCreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="cec15-178">Область **CreationClassName** системы.</span><span class="sxs-lookup"><span data-stu-id="cec15-178">Scoping system's **CreationClassName**.</span></span>

</dd> <dt>

<span data-ttu-id="cec15-179">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="cec15-179">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cec15-180">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="cec15-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cec15-181">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cec15-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cec15-182">Квалификаторы: распространяются ("[**CIM- \_**](cim-logicaldevice.md) [**унаследованный**](/windows/desktop/WmiSdk/standard-qualifiers) ".**SystemName**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="cec15-182">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_LogicalDevice**](cim-logicaldevice.md).**SystemName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="cec15-183">Свойство **имени** системы области.</span><span class="sxs-lookup"><span data-stu-id="cec15-183">Scoping system's **Name** property.</span></span>

</dd> <dt>

<span data-ttu-id="cec15-184">**варнингкаунт**</span><span class="sxs-lookup"><span data-stu-id="cec15-184">**WarningCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cec15-185">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="cec15-185">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="cec15-186">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cec15-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cec15-187">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Рабочее состояние DMTF \| 003,9 ")</span><span class="sxs-lookup"><span data-stu-id="cec15-187">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.9")</span></span>
</dt> </dl>

<span data-ttu-id="cec15-188">Количество предупреждений.</span><span class="sxs-lookup"><span data-stu-id="cec15-188">Count of the warnings.</span></span>

<span data-ttu-id="cec15-189">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="cec15-189">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cec15-190">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cec15-190">Remarks</span></span>

<span data-ttu-id="cec15-191">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="cec15-191">WMI does not implement this class.</span></span>

<span data-ttu-id="cec15-192">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="cec15-192">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="cec15-193">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="cec15-193">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="cec15-194">Требования</span><span class="sxs-lookup"><span data-stu-id="cec15-194">Requirements</span></span>



| <span data-ttu-id="cec15-195">Требование</span><span class="sxs-lookup"><span data-stu-id="cec15-195">Requirement</span></span> | <span data-ttu-id="cec15-196">Значение</span><span class="sxs-lookup"><span data-stu-id="cec15-196">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cec15-197">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cec15-197">Minimum supported client</span></span><br/> | <span data-ttu-id="cec15-198">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cec15-198">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="cec15-199">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cec15-199">Minimum supported server</span></span><br/> | <span data-ttu-id="cec15-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cec15-200">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="cec15-201">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="cec15-201">Namespace</span></span><br/>                | <span data-ttu-id="cec15-202">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="cec15-202">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="cec15-203">MOF</span><span class="sxs-lookup"><span data-stu-id="cec15-203">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cec15-204"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cec15-204"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="cec15-205">DLL</span><span class="sxs-lookup"><span data-stu-id="cec15-205">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cec15-206"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cec15-206"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cec15-207">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cec15-207">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cec15-208">**\_СТАТИСТИКАЛИНФОРМАТИОН CIM**</span><span class="sxs-lookup"><span data-stu-id="cec15-208">**CIM\_StatisticalInformation**</span></span>](cim-statisticalinformation.md)
</dt> </dl>

 

