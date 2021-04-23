---
description: '\_Класс WMI взаимосвязей Win32 ассоЦиатедпроцессормемори связывает процессор и его кэш-память.'
ms.assetid: 23da2a9d-772e-4258-9489-07d47801b2d8
ms.tgt_platform: multiple
title: Класс Win32_AssociatedProcessorMemory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_AssociatedProcessorMemory
- Win32_AssociatedProcessorMemory.BusSpeed
- Win32_AssociatedProcessorMemory.Dependent
- Win32_AssociatedProcessorMemory.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3737dca869c539d1414c4399f35fb8f107697b70
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990733"
---
# <a name="win32_associatedprocessormemory-class"></a><span data-ttu-id="7a6ff-103">\_Класс Win32 ассоЦиатедпроцессормемори</span><span class="sxs-lookup"><span data-stu-id="7a6ff-103">Win32\_AssociatedProcessorMemory class</span></span>

<span data-ttu-id="7a6ff-104">[Класс WMI](/windows/desktop/WmiSdk/retrieving-a-class) взаимосвязей **Win32 \_ ассоЦиатедпроцессормемори** связывает процессор и его кэш-память.</span><span class="sxs-lookup"><span data-stu-id="7a6ff-104">The **Win32\_AssociatedProcessorMemory** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a processor and its cache memory.</span></span>

<span data-ttu-id="7a6ff-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="7a6ff-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="7a6ff-106">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="7a6ff-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a6ff-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7a6ff-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{074737F0-ACBC-11d2-ABF6-00805F538618}"), AMENDMENT]
class Win32_AssociatedProcessorMemory : CIM_AssociatedProcessorMemory
{
  uint32                BusSpeed;
  Win32_Processor   REF Dependent;
  Win32_CacheMemory REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="7a6ff-108">Члены</span><span class="sxs-lookup"><span data-stu-id="7a6ff-108">Members</span></span>

<span data-ttu-id="7a6ff-109">Класс **Win32 \_ ассоЦиатедпроцессормемори** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="7a6ff-109">The **Win32\_AssociatedProcessorMemory** class has these types of members:</span></span>

-   [<span data-ttu-id="7a6ff-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="7a6ff-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7a6ff-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="7a6ff-111">Properties</span></span>

<span data-ttu-id="7a6ff-112">Класс **Win32 \_ ассоЦиатедпроцессормемори** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="7a6ff-112">The **Win32\_AssociatedProcessorMemory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7a6ff-113">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="7a6ff-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a6ff-114">Тип данных: **Win32 \_ качемемори**</span><span class="sxs-lookup"><span data-stu-id="7a6ff-114">Data type: **Win32\_CacheMemory**</span></span>
</dt> <dt>

<span data-ttu-id="7a6ff-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7a6ff-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7a6ff-116">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ качемемори")</span><span class="sxs-lookup"><span data-stu-id="7a6ff-116">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_CacheMemory")</span></span>
</dt> </dl>

<span data-ttu-id="7a6ff-117">[**\_ Качемемори Win32**](win32-cachememory.md) , описывающий кэш-память, доступную для процессора.</span><span class="sxs-lookup"><span data-stu-id="7a6ff-117">A [**Win32\_CacheMemory**](win32-cachememory.md) that describes the cache memory available to the processor.</span></span>

</dd> <dt>

<span data-ttu-id="7a6ff-118">**бусспид**</span><span class="sxs-lookup"><span data-stu-id="7a6ff-118">**BusSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a6ff-119">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7a6ff-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7a6ff-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7a6ff-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7a6ff-121">Квалификаторы: [**единицы измерения**](/windows/desktop/WmiSdk/standard-qualifiers) ("мегагерц")</span><span class="sxs-lookup"><span data-stu-id="7a6ff-121">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("megahertz")</span></span>
</dt> </dl>

<span data-ttu-id="7a6ff-122">Скорость шины в мегагерцах (МГц) между процессором и памятью.</span><span class="sxs-lookup"><span data-stu-id="7a6ff-122">Speed of the bus, in megahertz (MHz), between the processor and memory.</span></span>

<span data-ttu-id="7a6ff-123">Это свойство наследуется от [**CIM \_ ассоЦиатедпроцессормемори**](cim-associatedprocessormemory.md).</span><span class="sxs-lookup"><span data-stu-id="7a6ff-123">This property is inherited from [**CIM\_AssociatedProcessorMemory**](cim-associatedprocessormemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="7a6ff-124">**Него**</span><span class="sxs-lookup"><span data-stu-id="7a6ff-124">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a6ff-125">Тип данных: **\_ процессор Win32**</span><span class="sxs-lookup"><span data-stu-id="7a6ff-125">Data type: **Win32\_Processor**</span></span>
</dt> <dt>

<span data-ttu-id="7a6ff-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7a6ff-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7a6ff-127">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| процессор Win32 WMI \_ ")</span><span class="sxs-lookup"><span data-stu-id="7a6ff-127">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_Processor")</span></span>
</dt> </dl>

<span data-ttu-id="7a6ff-128">[**\_ Процессор Win32**](win32-processor.md) , описывающий процессор, использующий кэш-память.</span><span class="sxs-lookup"><span data-stu-id="7a6ff-128">A [**Win32\_Processor**](win32-processor.md) that describes the processor that is using the cache memory.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7a6ff-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7a6ff-129">Remarks</span></span>

<span data-ttu-id="7a6ff-130">Класс **Win32 \_ ассоЦиатедпроцессормемори** является производным от [**CIM \_ ассоЦиатедпроцессормемори**](cim-associatedprocessormemory.md).</span><span class="sxs-lookup"><span data-stu-id="7a6ff-130">The **Win32\_AssociatedProcessorMemory** class is derived from [**CIM\_AssociatedProcessorMemory**](cim-associatedprocessormemory.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7a6ff-131">Требования</span><span class="sxs-lookup"><span data-stu-id="7a6ff-131">Requirements</span></span>



| <span data-ttu-id="7a6ff-132">Требование</span><span class="sxs-lookup"><span data-stu-id="7a6ff-132">Requirement</span></span> | <span data-ttu-id="7a6ff-133">Значение</span><span class="sxs-lookup"><span data-stu-id="7a6ff-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7a6ff-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7a6ff-134">Minimum supported client</span></span><br/> | <span data-ttu-id="7a6ff-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7a6ff-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7a6ff-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7a6ff-136">Minimum supported server</span></span><br/> | <span data-ttu-id="7a6ff-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7a6ff-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7a6ff-138">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="7a6ff-138">Namespace</span></span><br/>                | <span data-ttu-id="7a6ff-139">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="7a6ff-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7a6ff-140">MOF</span><span class="sxs-lookup"><span data-stu-id="7a6ff-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7a6ff-141"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7a6ff-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7a6ff-142">DLL</span><span class="sxs-lookup"><span data-stu-id="7a6ff-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7a6ff-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7a6ff-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a6ff-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7a6ff-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a6ff-145">**\_АССОЦИАТЕДПРОЦЕССОРМЕМОРИ CIM**</span><span class="sxs-lookup"><span data-stu-id="7a6ff-145">**CIM\_AssociatedProcessorMemory**</span></span>](cim-associatedprocessormemory.md)
</dt> <dt>

[<span data-ttu-id="7a6ff-146">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="7a6ff-146">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

