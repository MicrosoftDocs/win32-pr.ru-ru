---
description: '\_Класс WMI взаимосвязей Win32 меморяррайлокатион связывает массив логических памяти и массив физической памяти, в котором он существует.'
ms.assetid: 455daeee-ad67-4599-84d6-fa3f4ac593aa
ms.tgt_platform: multiple
title: Класс Win32_MemoryArrayLocation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_MemoryArrayLocation
- Win32_MemoryArrayLocation.Dependent
- Win32_MemoryArrayLocation.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 62aae3bf672b12bdb947ff8ce6b76f919eaa11b7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539230"
---
# <a name="win32_memoryarraylocation-class"></a><span data-ttu-id="fff61-103">\_Класс Win32 меморяррайлокатион</span><span class="sxs-lookup"><span data-stu-id="fff61-103">Win32\_MemoryArrayLocation class</span></span>

<span data-ttu-id="fff61-104">[Класс WMI](/windows/desktop/WmiSdk/retrieving-a-class) взаимосвязей **Win32 \_ меморяррайлокатион** связывает массив логических памяти и массив физической памяти, в котором он существует.</span><span class="sxs-lookup"><span data-stu-id="fff61-104">The **Win32\_MemoryArrayLocation** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a logical memory array and the physical memory array on which it exists.</span></span>

<span data-ttu-id="fff61-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="fff61-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="fff61-106">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="fff61-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="fff61-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fff61-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{B24EF561-BBBE-11d2-ABFB-00805F538618}"), AMENDMENT]
class Win32_MemoryArrayLocation : CIM_Realizes
{
  Win32_MemoryArray         REF Dependent;
  Win32_PhysicalMemoryArray REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="fff61-108">Члены</span><span class="sxs-lookup"><span data-stu-id="fff61-108">Members</span></span>

<span data-ttu-id="fff61-109">Класс **Win32 \_ меморяррайлокатион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="fff61-109">The **Win32\_MemoryArrayLocation** class has these types of members:</span></span>

-   [<span data-ttu-id="fff61-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="fff61-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fff61-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="fff61-111">Properties</span></span>

<span data-ttu-id="fff61-112">Класс **Win32 \_ меморяррайлокатион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="fff61-112">The **Win32\_MemoryArrayLocation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fff61-113">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="fff61-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fff61-114">Тип данных: **Win32 \_ фисикалмеморяррай**</span><span class="sxs-lookup"><span data-stu-id="fff61-114">Data type: **Win32\_PhysicalMemoryArray**</span></span>
</dt> <dt>

<span data-ttu-id="fff61-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="fff61-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fff61-116">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ фисикалмеморяррай")</span><span class="sxs-lookup"><span data-stu-id="fff61-116">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_PhysicalMemoryArray")</span></span>
</dt> </dl>

<span data-ttu-id="fff61-117">[**\_ Фисикалмеморяррай Win32**](win32-physicalmemoryarray.md) , описывающий массив физической памяти, который реализует массив логической памяти.</span><span class="sxs-lookup"><span data-stu-id="fff61-117">A [**Win32\_PhysicalMemoryArray**](win32-physicalmemoryarray.md) that describes the physical memory array that implements the logical memory array.</span></span>

</dd> <dt>

<span data-ttu-id="fff61-118">**Него**</span><span class="sxs-lookup"><span data-stu-id="fff61-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fff61-119">Тип данных: **Win32 \_ меморяррай**</span><span class="sxs-lookup"><span data-stu-id="fff61-119">Data type: **Win32\_MemoryArray**</span></span>
</dt> <dt>

<span data-ttu-id="fff61-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="fff61-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fff61-121">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ меморяррай")</span><span class="sxs-lookup"><span data-stu-id="fff61-121">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_MemoryArray")</span></span>
</dt> </dl>

<span data-ttu-id="fff61-122">[**\_ Меморяррай Win32**](win32-memoryarray.md) , описывающий массив логических памяти, реализованный массивом физической памяти.</span><span class="sxs-lookup"><span data-stu-id="fff61-122">A [**Win32\_MemoryArray**](win32-memoryarray.md) that describes the logical memory array implemented by the physical memory array.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fff61-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fff61-123">Remarks</span></span>

<span data-ttu-id="fff61-124">Класс **Win32 \_ меморяррайлокатион** является производным от [**CIM \_**](cim-realizes.md).</span><span class="sxs-lookup"><span data-stu-id="fff61-124">The **Win32\_MemoryArrayLocation** class is derived from [**CIM\_Realizes**](cim-realizes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fff61-125">Требования</span><span class="sxs-lookup"><span data-stu-id="fff61-125">Requirements</span></span>



| <span data-ttu-id="fff61-126">Требование</span><span class="sxs-lookup"><span data-stu-id="fff61-126">Requirement</span></span> | <span data-ttu-id="fff61-127">Значение</span><span class="sxs-lookup"><span data-stu-id="fff61-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fff61-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fff61-128">Minimum supported client</span></span><br/> | <span data-ttu-id="fff61-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fff61-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fff61-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fff61-130">Minimum supported server</span></span><br/> | <span data-ttu-id="fff61-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fff61-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fff61-132">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="fff61-132">Namespace</span></span><br/>                | <span data-ttu-id="fff61-133">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="fff61-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="fff61-134">MOF</span><span class="sxs-lookup"><span data-stu-id="fff61-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fff61-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fff61-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="fff61-136">DLL</span><span class="sxs-lookup"><span data-stu-id="fff61-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fff61-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fff61-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fff61-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fff61-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fff61-139">**\_Реализации CIM**</span><span class="sxs-lookup"><span data-stu-id="fff61-139">**CIM\_Realizes**</span></span>](cim-realizes.md)
</dt> <dt>

[<span data-ttu-id="fff61-140">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="fff61-140">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

