---
description: Класс CIM \_ ерроркаунтерсфордевице связывает \_ класс CIM девицеерроркаунтс с логическим устройством, к которому оно применяется.
ms.assetid: 200971ab-df85-4a45-beb3-4ffe11ce92dc
ms.tgt_platform: multiple
title: Класс CIM_ErrorCountersForDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ErrorCountersForDevice
- CIM_ErrorCountersForDevice.Element
- CIM_ErrorCountersForDevice.Stats
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7c4e11b1f58cae7b544b251044657bb737525b37
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896033"
---
# <a name="cim_errorcountersfordevice-class"></a><span data-ttu-id="05984-103">\_Класс CIM ерроркаунтерсфордевице</span><span class="sxs-lookup"><span data-stu-id="05984-103">CIM\_ErrorCountersForDevice class</span></span>

<span data-ttu-id="05984-104">Класс **CIM \_ ерроркаунтерсфордевице** связывает класс [**CIM \_ девицеерроркаунтс**](cim-deviceerrorcounts.md) с логическим устройством, к которому оно применяется.</span><span class="sxs-lookup"><span data-stu-id="05984-104">The **CIM\_ErrorCountersForDevice** class associates the [**CIM\_DeviceErrorCounts**](cim-deviceerrorcounts.md) class to the logical device to which it applies.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="05984-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="05984-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="05984-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="05984-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="05984-107">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="05984-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="05984-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="05984-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="05984-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="05984-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{2D79F3A0-D025-11d2-85F5-0000F8102E5F}"), AMENDMENT]
class CIM_ErrorCountersForDevice : CIM_Statistics
{
  CIM_LogicalDevice     REF Element;
  CIM_DeviceErrorCounts REF Stats;
};
```

## <a name="members"></a><span data-ttu-id="05984-110">Члены</span><span class="sxs-lookup"><span data-stu-id="05984-110">Members</span></span>

<span data-ttu-id="05984-111">Класс **CIM \_ ерроркаунтерсфордевице** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="05984-111">The **CIM\_ErrorCountersForDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="05984-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="05984-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="05984-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="05984-113">Properties</span></span>

<span data-ttu-id="05984-114">Класс **CIM \_ ерроркаунтерсфордевице** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="05984-114">The **CIM\_ErrorCountersForDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="05984-115">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="05984-115">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05984-116">Тип данных: **CIM \_** с типом "модель"</span><span class="sxs-lookup"><span data-stu-id="05984-116">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="05984-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="05984-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05984-118">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("элемент"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="05984-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Element"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="05984-119">Логическое значение типа [**CIM \_**](cim-logicaldevice.md) , описывающее устройство, к которому применяются счетчики ошибок.</span><span class="sxs-lookup"><span data-stu-id="05984-119">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that describes the device to which the error counters apply.</span></span>

</dd> <dt>

<span data-ttu-id="05984-120">**Статистика**</span><span class="sxs-lookup"><span data-stu-id="05984-120">**Stats**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05984-121">Тип данных: **CIM \_ девицеерроркаунтс**</span><span class="sxs-lookup"><span data-stu-id="05984-121">Data type: **CIM\_DeviceErrorCounts**</span></span>
</dt> <dt>

<span data-ttu-id="05984-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="05984-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05984-123">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (статистика), [**слабый**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="05984-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Stats"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="05984-124">[**CIM \_ девицеерроркаунтс**](cim-deviceerrorcounts.md) , описывающий статистический объект, в данном случае класс счетчика ошибок.</span><span class="sxs-lookup"><span data-stu-id="05984-124">A [**CIM\_DeviceErrorCounts**](cim-deviceerrorcounts.md) describing the statistical object - in this case, the error counter class.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="05984-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="05984-125">Remarks</span></span>

<span data-ttu-id="05984-126">Класс **CIM \_ ерроркаунтерсфордевице** наследуется от [**\_ статистики CIM**](cim-statistics.md).</span><span class="sxs-lookup"><span data-stu-id="05984-126">The **CIM\_ErrorCountersForDevice** class is inherited from [**CIM\_Statistics**](cim-statistics.md).</span></span>

<span data-ttu-id="05984-127">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="05984-127">WMI does not implement this class.</span></span>

<span data-ttu-id="05984-128">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="05984-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="05984-129">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="05984-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="05984-130">Требования</span><span class="sxs-lookup"><span data-stu-id="05984-130">Requirements</span></span>



| <span data-ttu-id="05984-131">Требование</span><span class="sxs-lookup"><span data-stu-id="05984-131">Requirement</span></span> | <span data-ttu-id="05984-132">Значение</span><span class="sxs-lookup"><span data-stu-id="05984-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="05984-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="05984-133">Minimum supported client</span></span><br/> | <span data-ttu-id="05984-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="05984-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="05984-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="05984-135">Minimum supported server</span></span><br/> | <span data-ttu-id="05984-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="05984-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="05984-137">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="05984-137">Namespace</span></span><br/>                | <span data-ttu-id="05984-138">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="05984-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="05984-139">MOF</span><span class="sxs-lookup"><span data-stu-id="05984-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="05984-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="05984-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="05984-141">DLL</span><span class="sxs-lookup"><span data-stu-id="05984-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="05984-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="05984-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05984-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="05984-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05984-144">**\_Статистика CIM**</span><span class="sxs-lookup"><span data-stu-id="05984-144">**CIM\_Statistics**</span></span>](cim-statistics.md)
</dt> </dl>

 

