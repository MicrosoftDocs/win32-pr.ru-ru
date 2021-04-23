---
description: Указывает, что страница памяти была удалена из системы из-за избыточной проверки ошибок оборудования и ошибок коррекции (ECC). Этот класс доступен только в 64-разрядных системах Windows.
ms.assetid: 364a2520-8d7c-44f2-95f6-eea9a5531975
title: Класс MSMCAEvent_MemoryPageRemoved
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_MemoryPageRemoved
- MSMCAEvent_MemoryPageRemoved.Active
- MSMCAEvent_MemoryPageRemoved.InstanceName
- MSMCAEvent_MemoryPageRemoved.PhysicalAddress
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: dc29c5b51531e204ab50f062dd08ef8d5abf1bbf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693450"
---
# <a name="msmcaevent_memorypageremoved-class"></a><span data-ttu-id="483c7-104">\_Класс мсмкаевент меморипажеремовед</span><span class="sxs-lookup"><span data-stu-id="483c7-104">MSMCAEvent\_MemoryPageRemoved class</span></span>

<span data-ttu-id="483c7-105">Класс **мсмкаевент \_ меморипажеремовед** указывает на то, что страница памяти была удалена из системы в связи с избыточной проверкой ошибок оборудования и исправлением ошибок (ECC).</span><span class="sxs-lookup"><span data-stu-id="483c7-105">The **MSMCAEvent\_MemoryPageRemoved** class indicates that a memory page has been removed from system use due to excessive hardware Error Checking and Correcting (ECC) errors.</span></span> <span data-ttu-id="483c7-106">Этот класс доступен только в 64-разрядных системах Windows.</span><span class="sxs-lookup"><span data-stu-id="483c7-106">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="483c7-107">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="483c7-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="483c7-108">Свойства и методы имеют алфавитный порядок, а не порядок MOF.</span><span class="sxs-lookup"><span data-stu-id="483c7-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="483c7-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="483c7-109">Syntax</span></span>

``` syntax
class MSMCAEvent_MemoryPageRemoved : WmiEvent
{
  boolean Active;
  string  InstanceName;
  uint64  PhysicalAddress;
};
```

## <a name="members"></a><span data-ttu-id="483c7-110">Члены</span><span class="sxs-lookup"><span data-stu-id="483c7-110">Members</span></span>

<span data-ttu-id="483c7-111">Класс **мсмкаевент \_ меморипажеремовед** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="483c7-111">The **MSMCAEvent\_MemoryPageRemoved** class has these types of members:</span></span>

-   [<span data-ttu-id="483c7-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="483c7-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="483c7-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="483c7-113">Properties</span></span>

<span data-ttu-id="483c7-114">Класс **мсмкаевент \_ меморипажеремовед** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="483c7-114">The **MSMCAEvent\_MemoryPageRemoved** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="483c7-115">**Активен**</span><span class="sxs-lookup"><span data-stu-id="483c7-115">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="483c7-116">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="483c7-116">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="483c7-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="483c7-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="483c7-118">**Значение true**, если данный экземпляр класса активен; в противном случае — **false**.</span><span class="sxs-lookup"><span data-stu-id="483c7-118">**TRUE**, if this instance of the class is active; otherwise **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="483c7-119">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="483c7-119">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="483c7-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="483c7-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="483c7-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="483c7-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="483c7-122">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="483c7-122">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="483c7-123">Уникальный идентификатор для этого экземпляра класса.</span><span class="sxs-lookup"><span data-stu-id="483c7-123">Unique identifier for this instance of the class.</span></span>

</dd> <dt>

<span data-ttu-id="483c7-124">**PhysicalAddress**</span><span class="sxs-lookup"><span data-stu-id="483c7-124">**PhysicalAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="483c7-125">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="483c7-125">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="483c7-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="483c7-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="483c7-127">Адрес страницы памяти, которая была удалена.</span><span class="sxs-lookup"><span data-stu-id="483c7-127">Address of the page of memory that has been removed.</span></span>

<span data-ttu-id="483c7-128">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="483c7-128">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="483c7-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="483c7-129">Remarks</span></span>

<span data-ttu-id="483c7-130">Класс **мсмкаевент \_ меморипажеремовед** является производным от [**WMIEvent**](wmievent.md).</span><span class="sxs-lookup"><span data-stu-id="483c7-130">The **MSMCAEvent\_MemoryPageRemoved** class is derived from [**WMIEvent**](wmievent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="483c7-131">Требования</span><span class="sxs-lookup"><span data-stu-id="483c7-131">Requirements</span></span>



| <span data-ttu-id="483c7-132">Требование</span><span class="sxs-lookup"><span data-stu-id="483c7-132">Requirement</span></span> | <span data-ttu-id="483c7-133">Значение</span><span class="sxs-lookup"><span data-stu-id="483c7-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="483c7-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="483c7-134">Minimum supported client</span></span><br/> | <span data-ttu-id="483c7-135">Windows XP</span><span class="sxs-lookup"><span data-stu-id="483c7-135">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="483c7-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="483c7-136">Minimum supported server</span></span><br/> | <span data-ttu-id="483c7-137">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="483c7-137">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="483c7-138">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="483c7-138">Namespace</span></span><br/>                | <span data-ttu-id="483c7-139">Корневой \\ инструментарий WMI</span><span class="sxs-lookup"><span data-stu-id="483c7-139">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="483c7-140">MOF</span><span class="sxs-lookup"><span data-stu-id="483c7-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="483c7-141"><dt>Вмикоре. mof</dt></span><span class="sxs-lookup"><span data-stu-id="483c7-141"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="483c7-142">DLL</span><span class="sxs-lookup"><span data-stu-id="483c7-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="483c7-143"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="483c7-143"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="483c7-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="483c7-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="483c7-145">Классы МСМКА</span><span class="sxs-lookup"><span data-stu-id="483c7-145">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="483c7-146">**WMIEvent**</span><span class="sxs-lookup"><span data-stu-id="483c7-146">**WMIEvent**</span></span>](wmievent.md)
</dt> </dl>

 

