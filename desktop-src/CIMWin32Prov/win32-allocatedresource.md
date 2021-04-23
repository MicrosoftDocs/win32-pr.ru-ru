---
description: '\_Класс WMI взаимосвязей Win32 аллокатедресаурце связывает логическое устройство с системным ресурсом. Этот класс используется для обнаружения того, какие ресурсы, такие как IRQ или каналы DMA, используются конкретным устройством.'
ms.assetid: cfac1209-1405-4fee-847c-8a61504bfac1
ms.tgt_platform: multiple
title: Класс Win32_AllocatedResource
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_AllocatedResource
- Win32_AllocatedResource.Dependent
- Win32_AllocatedResource.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 87a57e53a85e4433ae325fc2ed441211db75b79f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990734"
---
# <a name="win32_allocatedresource-class"></a><span data-ttu-id="5cf91-104">\_Класс Win32 аллокатедресаурце</span><span class="sxs-lookup"><span data-stu-id="5cf91-104">Win32\_AllocatedResource class</span></span>

<span data-ttu-id="5cf91-105">[Класс WMI](/windows/desktop/WmiSdk/retrieving-a-class) взаимосвязей **Win32 \_ аллокатедресаурце** связывает логическое устройство с системным ресурсом.</span><span class="sxs-lookup"><span data-stu-id="5cf91-105">The **Win32\_AllocatedResource** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a logical device to a system resource.</span></span> <span data-ttu-id="5cf91-106">Этот класс используется для обнаружения того, какие ресурсы, такие как IRQ или каналы DMA, используются конкретным устройством.</span><span class="sxs-lookup"><span data-stu-id="5cf91-106">This class is used to discover which resources, such as IRQs or DMA channels, are in use by a specific device.</span></span>

<span data-ttu-id="5cf91-107">Этот класс устарел.</span><span class="sxs-lookup"><span data-stu-id="5cf91-107">This class is obsolete.</span></span> <span data-ttu-id="5cf91-108">Вместо этого класса следует использовать свойства в классе [**Win32 \_ пнпаллокатедресаурце**](win32-pnpallocatedresource.md) .</span><span class="sxs-lookup"><span data-stu-id="5cf91-108">In place of this class, you should use the properties in the [**Win32\_PNPAllocatedResource**](win32-pnpallocatedresource.md) class.</span></span>

<span data-ttu-id="5cf91-109">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="5cf91-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="5cf91-110">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="5cf91-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="5cf91-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5cf91-111">Syntax</span></span>

``` syntax
[DEPRECATED, Dynamic, Provider("CIMWin32"), UUID("{8502C50D-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_AllocatedResource : CIM_Dependency
{
  CIM_LogicalDevice  REF Dependent;
  CIM_SystemResource REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="5cf91-112">Члены</span><span class="sxs-lookup"><span data-stu-id="5cf91-112">Members</span></span>

<span data-ttu-id="5cf91-113">Класс **Win32 \_ аллокатедресаурце** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="5cf91-113">The **Win32\_AllocatedResource** class has these types of members:</span></span>

-   [<span data-ttu-id="5cf91-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="5cf91-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5cf91-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="5cf91-115">Properties</span></span>

<span data-ttu-id="5cf91-116">Класс **Win32 \_ аллокатедресаурце** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="5cf91-116">The **Win32\_AllocatedResource** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5cf91-117">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="5cf91-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cf91-118">Тип данных: **CIM \_ системресаурце**</span><span class="sxs-lookup"><span data-stu-id="5cf91-118">Data type: **CIM\_SystemResource**</span></span>
</dt> <dt>

<span data-ttu-id="5cf91-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5cf91-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5cf91-120">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \| CIM \_ системресаурце")</span><span class="sxs-lookup"><span data-stu-id="5cf91-120">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\|CIM\_SystemResource")</span></span>
</dt> </dl>

<span data-ttu-id="5cf91-121">[**\_ Системресаурце CIM**](cim-systemresource.md) , описывающий свойства системного ресурса, доступного для логического устройства.</span><span class="sxs-lookup"><span data-stu-id="5cf91-121">A [**CIM\_SystemResource**](cim-systemresource.md) that describes the properties of a system resource available to the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="5cf91-122">**Него**</span><span class="sxs-lookup"><span data-stu-id="5cf91-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cf91-123">Тип данных: **CIM \_** с типом "модель"</span><span class="sxs-lookup"><span data-stu-id="5cf91-123">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="5cf91-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5cf91-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5cf91-125">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \| CIM \_ ")</span><span class="sxs-lookup"><span data-stu-id="5cf91-125">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\|CIM\_LogicalDevice")</span></span>
</dt> </dl>

<span data-ttu-id="5cf91-126">Логическое устройство типа [**CIM \_**](cim-logicaldevice.md) , представляющее свойства логического устройства, которое использует назначенные ему системные ресурсы.</span><span class="sxs-lookup"><span data-stu-id="5cf91-126">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that represents the properties of the logical device that is using the system resources assigned to it.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5cf91-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5cf91-127">Remarks</span></span>

<span data-ttu-id="5cf91-128">Класс **Win32 \_ аллокатедресаурце** является производным от [**\_ зависимости CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="5cf91-128">The **Win32\_AllocatedResource** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5cf91-129">Требования</span><span class="sxs-lookup"><span data-stu-id="5cf91-129">Requirements</span></span>



| <span data-ttu-id="5cf91-130">Требование</span><span class="sxs-lookup"><span data-stu-id="5cf91-130">Requirement</span></span> | <span data-ttu-id="5cf91-131">Значение</span><span class="sxs-lookup"><span data-stu-id="5cf91-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5cf91-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5cf91-132">Minimum supported client</span></span><br/> | <span data-ttu-id="5cf91-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5cf91-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5cf91-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5cf91-134">Minimum supported server</span></span><br/> | <span data-ttu-id="5cf91-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5cf91-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5cf91-136">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="5cf91-136">Namespace</span></span><br/>                | <span data-ttu-id="5cf91-137">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="5cf91-137">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5cf91-138">MOF</span><span class="sxs-lookup"><span data-stu-id="5cf91-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5cf91-139"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5cf91-139"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5cf91-140">DLL</span><span class="sxs-lookup"><span data-stu-id="5cf91-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5cf91-141"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5cf91-141"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5cf91-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5cf91-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5cf91-143">**\_Зависимость CIM**</span><span class="sxs-lookup"><span data-stu-id="5cf91-143">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> <dt>

[<span data-ttu-id="5cf91-144">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="5cf91-144">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

