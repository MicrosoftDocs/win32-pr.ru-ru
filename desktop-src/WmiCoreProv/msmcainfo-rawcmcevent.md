---
description: Содержит исправленное событие проверки компьютера (CMC). Этот класс доступен только в 64-разрядных системах Windows.
ms.assetid: e12efbf7-7d53-415a-bc48-90d33e4ce16d
title: Класс MSMCAInfo_RawCMCEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAInfo_RawCMCEvent
- MSMCAInfo_RawCMCEvent.Active
- MSMCAInfo_RawCMCEvent.Count
- MSMCAInfo_RawCMCEvent.InstanceName
- MSMCAInfo_RawCMCEvent.Records
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 1bb60d5fbcf004b924a91e640d8cd8a8c5ad3c25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712612"
---
# <a name="msmcainfo_rawcmcevent-class"></a><span data-ttu-id="4f167-104">\_Класс мсмкаинфо равкмцевент</span><span class="sxs-lookup"><span data-stu-id="4f167-104">MSMCAInfo\_RawCMCEvent class</span></span>

<span data-ttu-id="4f167-105">Класс **мсмкаинфо \_ Равкмцевент** содержит исправленное событие проверки компьютера (CMC).</span><span class="sxs-lookup"><span data-stu-id="4f167-105">The **MSMCAInfo\_RawCMCEvent** class contains a Corrected Machine Check (CMC) event.</span></span> <span data-ttu-id="4f167-106">Этот класс доступен только в 64-разрядных системах Windows.</span><span class="sxs-lookup"><span data-stu-id="4f167-106">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="4f167-107">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="4f167-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="4f167-108">Свойства и методы имеют алфавитный порядок, а не порядок MOF.</span><span class="sxs-lookup"><span data-stu-id="4f167-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f167-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4f167-109">Syntax</span></span>

``` syntax
class MSMCAInfo_RawCMCEvent : WMIEvent
{
  boolean         Active;
  uint32          Count;
  string          InstanceName;
  MSMCAInfo_Entry Records[];
};
```

## <a name="members"></a><span data-ttu-id="4f167-110">Члены</span><span class="sxs-lookup"><span data-stu-id="4f167-110">Members</span></span>

<span data-ttu-id="4f167-111">Класс **мсмкаинфо \_ равкмцевент** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="4f167-111">The **MSMCAInfo\_RawCMCEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="4f167-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="4f167-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4f167-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="4f167-113">Properties</span></span>

<span data-ttu-id="4f167-114">Класс **мсмкаинфо \_ равкмцевент** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="4f167-114">The **MSMCAInfo\_RawCMCEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4f167-115">**Активен**</span><span class="sxs-lookup"><span data-stu-id="4f167-115">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f167-116">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="4f167-116">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4f167-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4f167-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f167-118">Значение TRUE, если данный экземпляр класса активен; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="4f167-118">TRUE, if this instance of the class is active; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="4f167-119">**Количество**</span><span class="sxs-lookup"><span data-stu-id="4f167-119">**Count**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f167-120">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4f167-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4f167-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4f167-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f167-122">Число записей об ошибках.</span><span class="sxs-lookup"><span data-stu-id="4f167-122">Number of error records.</span></span>

</dd> <dt>

<span data-ttu-id="4f167-123">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="4f167-123">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f167-124">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4f167-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4f167-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4f167-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f167-126">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="4f167-126">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="4f167-127">Уникальный идентификатор этого экземпляра класса.</span><span class="sxs-lookup"><span data-stu-id="4f167-127">Unique identifier of this instance of the class.</span></span>

</dd> <dt>

<span data-ttu-id="4f167-128">**Записи**</span><span class="sxs-lookup"><span data-stu-id="4f167-128">**Records**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f167-129">Тип данных: **массив \_ записей мсмкаинфо**</span><span class="sxs-lookup"><span data-stu-id="4f167-129">Data type: **MSMCAInfo\_Entry** array</span></span>
</dt> <dt>

<span data-ttu-id="4f167-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4f167-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f167-131">Массив записей об ошибках архитектуры машинной проверки (MCA).</span><span class="sxs-lookup"><span data-stu-id="4f167-131">Array of Machine Check Architecture (MCA) error records.</span></span> <span data-ttu-id="4f167-132">Число записей об ошибках MCA в массиве задается свойством **Count** .</span><span class="sxs-lookup"><span data-stu-id="4f167-132">The number of MCA error records in the array is specified by the **Count** property.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4f167-133">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4f167-133">Remarks</span></span>

<span data-ttu-id="4f167-134">Класс **мсмкаинфо \_ равкмцевент** является производным от [**WMIEvent**](wmievent.md).</span><span class="sxs-lookup"><span data-stu-id="4f167-134">The **MSMCAInfo\_RawCMCEvent** class is derived from [**WMIEvent**](wmievent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4f167-135">Требования</span><span class="sxs-lookup"><span data-stu-id="4f167-135">Requirements</span></span>



| <span data-ttu-id="4f167-136">Требование</span><span class="sxs-lookup"><span data-stu-id="4f167-136">Requirement</span></span> | <span data-ttu-id="4f167-137">Значение</span><span class="sxs-lookup"><span data-stu-id="4f167-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4f167-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4f167-138">Minimum supported client</span></span><br/> | <span data-ttu-id="4f167-139">Windows XP</span><span class="sxs-lookup"><span data-stu-id="4f167-139">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="4f167-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4f167-140">Minimum supported server</span></span><br/> | <span data-ttu-id="4f167-141">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4f167-141">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="4f167-142">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="4f167-142">Namespace</span></span><br/>                | <span data-ttu-id="4f167-143">Корневой \\ инструментарий WMI</span><span class="sxs-lookup"><span data-stu-id="4f167-143">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="4f167-144">MOF</span><span class="sxs-lookup"><span data-stu-id="4f167-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4f167-145"><dt>Вмикоре. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4f167-145"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="4f167-146">DLL</span><span class="sxs-lookup"><span data-stu-id="4f167-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4f167-147"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4f167-147"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f167-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4f167-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f167-149">Классы МСМКА</span><span class="sxs-lookup"><span data-stu-id="4f167-149">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="4f167-150">**WMIEvent**</span><span class="sxs-lookup"><span data-stu-id="4f167-150">**WMIEvent**</span></span>](wmievent.md)
</dt> </dl>

 

