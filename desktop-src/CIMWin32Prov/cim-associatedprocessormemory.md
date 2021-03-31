---
description: Класс CIM \_ ассоЦиатедпроцессормемори связывает процессор и системную память или кэш процессора.
ms.assetid: a4c28a0a-e4cc-4db2-bd77-b7b5023eace6
ms.tgt_platform: multiple
title: Класс CIM_AssociatedProcessorMemory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AssociatedProcessorMemory
- CIM_AssociatedProcessorMemory.Antecedent
- CIM_AssociatedProcessorMemory.Dependent
- CIM_AssociatedProcessorMemory.BusSpeed
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: f35cdca92cb15e1c6fff215ff1363844e0d47012
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990670"
---
# <a name="cim_associatedprocessormemory-class"></a><span data-ttu-id="49934-103">\_Класс CIM ассоЦиатедпроцессормемори</span><span class="sxs-lookup"><span data-stu-id="49934-103">CIM\_AssociatedProcessorMemory class</span></span>

<span data-ttu-id="49934-104">Класс **CIM \_ ассоЦиатедпроцессормемори** связывает процессор и системную память или кэш процессора.</span><span class="sxs-lookup"><span data-stu-id="49934-104">The **CIM\_AssociatedProcessorMemory** class associates the processor and system memory, or a processor's cache.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="49934-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="49934-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="49934-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="49934-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="49934-107">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="49934-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="49934-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="49934-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="49934-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="49934-109">Syntax</span></span>

``` syntax
[abstract, UUID("{464FFAB1-946F-11d2-AAE2-006008C78BC7}"), AMENDMENT]
class CIM_AssociatedProcessorMemory : CIM_AssociatedMemory
{
  CIM_Memory    REF Antecedent;
  CIM_Processor REF Dependent;
  uint32            BusSpeed;
};
```

## <a name="members"></a><span data-ttu-id="49934-110">Члены</span><span class="sxs-lookup"><span data-stu-id="49934-110">Members</span></span>

<span data-ttu-id="49934-111">Класс **CIM \_ ассоЦиатедпроцессормемори** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="49934-111">The **CIM\_AssociatedProcessorMemory** class has these types of members:</span></span>

-   [<span data-ttu-id="49934-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="49934-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="49934-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="49934-113">Properties</span></span>

<span data-ttu-id="49934-114">Класс **CIM \_ ассоЦиатедпроцессормемори** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="49934-114">The **CIM\_AssociatedProcessorMemory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="49934-115">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="49934-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49934-116">Тип данных: **\_ память CIM**</span><span class="sxs-lookup"><span data-stu-id="49934-116">Data type: **CIM\_Memory**</span></span>
</dt> <dt>

<span data-ttu-id="49934-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="49934-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="49934-118">[**\_ Память CIM**](cim-memory.md) , описывающая память, установленную на устройстве или связанной с ней.</span><span class="sxs-lookup"><span data-stu-id="49934-118">A [**CIM\_Memory**](cim-memory.md) that describes the memory installed on or associated with a device.</span></span>

<span data-ttu-id="49934-119">Это свойство наследуется от [**CIM \_ ассоЦиатедмемори**](cim-associatedmemory.md).</span><span class="sxs-lookup"><span data-stu-id="49934-119">This property is inherited from [**CIM\_AssociatedMemory**](cim-associatedmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="49934-120">**бусспид**</span><span class="sxs-lookup"><span data-stu-id="49934-120">**BusSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49934-121">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="49934-121">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="49934-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="49934-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49934-123">Квалификаторы: [**единицы измерения**](/windows/desktop/WmiSdk/standard-qualifiers) ("мегагерц")</span><span class="sxs-lookup"><span data-stu-id="49934-123">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("megahertz")</span></span>
</dt> </dl>

<span data-ttu-id="49934-124">Скорость шины в мегагерцах (МГц) между процессором и памятью.</span><span class="sxs-lookup"><span data-stu-id="49934-124">Speed of the bus, in megahertz (MHz), between the processor and memory.</span></span>

</dd> <dt>

<span data-ttu-id="49934-125">**Него**</span><span class="sxs-lookup"><span data-stu-id="49934-125">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49934-126">Тип данных: **\_ процессор CIM**</span><span class="sxs-lookup"><span data-stu-id="49934-126">Data type: **CIM\_Processor**</span></span>
</dt> <dt>

<span data-ttu-id="49934-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="49934-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49934-128">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")</span><span class="sxs-lookup"><span data-stu-id="49934-128">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="49934-129">[**\_ Процессор CIM**](cim-processor.md) , описывающий процессор, обращающийся к памяти или использующий кэш.</span><span class="sxs-lookup"><span data-stu-id="49934-129">A [**CIM\_Processor**](cim-processor.md) describing the processor that accesses the memory or uses the cache.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="49934-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="49934-130">Remarks</span></span>

<span data-ttu-id="49934-131">Класс **CIM \_ ассоЦиатедпроцессормемори** является производным от [**CIM \_ ассоЦиатедмемори**](cim-associatedmemory.md).</span><span class="sxs-lookup"><span data-stu-id="49934-131">The **CIM\_AssociatedProcessorMemory** class is derived from [**CIM\_AssociatedMemory**](cim-associatedmemory.md).</span></span>

<span data-ttu-id="49934-132">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="49934-132">WMI does not implement this class.</span></span> <span data-ttu-id="49934-133">Дополнительные сведения о классах, производных от **CIM \_ ассоЦиатедпроцессормемори**, см. в разделе [Классы Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="49934-133">For more information about classes derived from **CIM\_AssociatedProcessorMemory**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="49934-134">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="49934-134">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="49934-135">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="49934-135">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="49934-136">Требования</span><span class="sxs-lookup"><span data-stu-id="49934-136">Requirements</span></span>



| <span data-ttu-id="49934-137">Требование</span><span class="sxs-lookup"><span data-stu-id="49934-137">Requirement</span></span> | <span data-ttu-id="49934-138">Значение</span><span class="sxs-lookup"><span data-stu-id="49934-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="49934-139">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="49934-139">Minimum supported client</span></span><br/> | <span data-ttu-id="49934-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="49934-140">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="49934-141">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="49934-141">Minimum supported server</span></span><br/> | <span data-ttu-id="49934-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="49934-142">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="49934-143">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="49934-143">Namespace</span></span><br/>                | <span data-ttu-id="49934-144">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="49934-144">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="49934-145">MOF</span><span class="sxs-lookup"><span data-stu-id="49934-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="49934-146"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="49934-146"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="49934-147">DLL</span><span class="sxs-lookup"><span data-stu-id="49934-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="49934-148"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="49934-148"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49934-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="49934-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49934-150">**\_АССОЦИАТЕДМЕМОРИ CIM**</span><span class="sxs-lookup"><span data-stu-id="49934-150">**CIM\_AssociatedMemory**</span></span>](cim-associatedmemory.md)
</dt> </dl>

 

