---
description: '\_Класс WMI взаимосвязей Win32 меморидевицелокатион связывает устройство памяти с физической памятью, на которой он существует.'
ms.assetid: 6fef916e-44e2-4b9f-94b7-c7204259004a
ms.tgt_platform: multiple
title: Класс Win32_MemoryDeviceLocation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_MemoryDeviceLocation
- Win32_MemoryDeviceLocation.Dependent
- Win32_MemoryDeviceLocation.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5cf1ba93a2574810892443aefa43e1c7c501636c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990417"
---
# <a name="win32_memorydevicelocation-class"></a><span data-ttu-id="09b50-103">\_Класс Win32 меморидевицелокатион</span><span class="sxs-lookup"><span data-stu-id="09b50-103">Win32\_MemoryDeviceLocation class</span></span>

<span data-ttu-id="09b50-104">[Класс WMI](/windows/desktop/WmiSdk/retrieving-a-class) взаимосвязей **Win32 \_ меморидевицелокатион** связывает устройство памяти с физической памятью, на которой он существует.</span><span class="sxs-lookup"><span data-stu-id="09b50-104">The **Win32\_MemoryDeviceLocation** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a memory device and the physical memory on which it exists.</span></span>

<span data-ttu-id="09b50-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="09b50-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="09b50-106">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="09b50-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="09b50-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="09b50-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{FAF76B9C-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class Win32_MemoryDeviceLocation : CIM_Realizes
{
  Win32_MemoryDevice   REF Dependent;
  Win32_PhysicalMemory REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="09b50-108">Члены</span><span class="sxs-lookup"><span data-stu-id="09b50-108">Members</span></span>

<span data-ttu-id="09b50-109">Класс **Win32 \_ меморидевицелокатион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="09b50-109">The **Win32\_MemoryDeviceLocation** class has these types of members:</span></span>

-   [<span data-ttu-id="09b50-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="09b50-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="09b50-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="09b50-111">Properties</span></span>

<span data-ttu-id="09b50-112">Класс **Win32 \_ меморидевицелокатион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="09b50-112">The **Win32\_MemoryDeviceLocation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="09b50-113">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="09b50-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09b50-114">Тип данных: **Win32 \_ фисикалмемори**</span><span class="sxs-lookup"><span data-stu-id="09b50-114">Data type: **Win32\_PhysicalMemory**</span></span>
</dt> <dt>

<span data-ttu-id="09b50-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="09b50-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="09b50-116">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ фисикалмемори")</span><span class="sxs-lookup"><span data-stu-id="09b50-116">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_PhysicalMemory")</span></span>
</dt> </dl>

<span data-ttu-id="09b50-117">[**\_ Фисикалмемори Win32**](win32-physicalmemory.md) , представляющий физическую память, содержащую устройство памяти.</span><span class="sxs-lookup"><span data-stu-id="09b50-117">A [**Win32\_PhysicalMemory**](win32-physicalmemory.md) that represents the physical memory containing the memory device.</span></span>

</dd> <dt>

<span data-ttu-id="09b50-118">**Него**</span><span class="sxs-lookup"><span data-stu-id="09b50-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09b50-119">Тип данных: **Win32 \_ меморидевице**</span><span class="sxs-lookup"><span data-stu-id="09b50-119">Data type: **Win32\_MemoryDevice**</span></span>
</dt> <dt>

<span data-ttu-id="09b50-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="09b50-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="09b50-121">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ меморидевице")</span><span class="sxs-lookup"><span data-stu-id="09b50-121">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_MemoryDevice")</span></span>
</dt> </dl>

<span data-ttu-id="09b50-122">**\_ Меморидевицелокатион Win32** , представляющий устройство памяти, существующее в физической памяти.</span><span class="sxs-lookup"><span data-stu-id="09b50-122">A **Win32\_MemoryDeviceLocation** that represents the memory device existing in the physical memory.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="09b50-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="09b50-123">Remarks</span></span>

<span data-ttu-id="09b50-124">Класс **Win32 \_ меморидевицелокатион** является производным от [**CIM \_**](cim-realizes.md).</span><span class="sxs-lookup"><span data-stu-id="09b50-124">The **Win32\_MemoryDeviceLocation** class is derived from [**CIM\_Realizes**](cim-realizes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="09b50-125">Требования</span><span class="sxs-lookup"><span data-stu-id="09b50-125">Requirements</span></span>



| <span data-ttu-id="09b50-126">Требование</span><span class="sxs-lookup"><span data-stu-id="09b50-126">Requirement</span></span> | <span data-ttu-id="09b50-127">Значение</span><span class="sxs-lookup"><span data-stu-id="09b50-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="09b50-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="09b50-128">Minimum supported client</span></span><br/> | <span data-ttu-id="09b50-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="09b50-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="09b50-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="09b50-130">Minimum supported server</span></span><br/> | <span data-ttu-id="09b50-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="09b50-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="09b50-132">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="09b50-132">Namespace</span></span><br/>                | <span data-ttu-id="09b50-133">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="09b50-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="09b50-134">MOF</span><span class="sxs-lookup"><span data-stu-id="09b50-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="09b50-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="09b50-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="09b50-136">DLL</span><span class="sxs-lookup"><span data-stu-id="09b50-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="09b50-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="09b50-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09b50-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="09b50-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09b50-139">**\_Реализации CIM**</span><span class="sxs-lookup"><span data-stu-id="09b50-139">**CIM\_Realizes**</span></span>](cim-realizes.md)
</dt> <dt>

[<span data-ttu-id="09b50-140">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="09b50-140">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

