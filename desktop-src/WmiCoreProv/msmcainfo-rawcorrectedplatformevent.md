---
description: Содержит исправленное событие платформы (CPE). Этот класс доступен только в 64-разрядных системах Windows.
ms.assetid: b24a390e-293d-4dd4-b747-33c298a5d45f
title: Класс MSMCAInfo_RawCorrectedPlatformEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAInfo_RawCorrectedPlatformEvent
- MSMCAInfo_RawCorrectedPlatformEvent.Active
- MSMCAInfo_RawCorrectedPlatformEvent.Count
- MSMCAInfo_RawCorrectedPlatformEvent.Records
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 906587ca9ee153eb93542c3e749e8164e6a5ee7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712611"
---
# <a name="msmcainfo_rawcorrectedplatformevent-class"></a><span data-ttu-id="1744a-104">\_Класс мсмкаинфо равкорректедплатформевент</span><span class="sxs-lookup"><span data-stu-id="1744a-104">MSMCAInfo\_RawCorrectedPlatformEvent class</span></span>

<span data-ttu-id="1744a-105">Класс **мсмкаинфо \_ Равкорректедплатформевент** содержит исправленное событие платформы (CPE).</span><span class="sxs-lookup"><span data-stu-id="1744a-105">The **MSMCAInfo\_RawCorrectedPlatformEvent** class contains a Corrected Platform Event (CPE).</span></span> <span data-ttu-id="1744a-106">Этот класс доступен только в 64-разрядных системах Windows.</span><span class="sxs-lookup"><span data-stu-id="1744a-106">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="1744a-107">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="1744a-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="1744a-108">Свойства и методы имеют алфавитный порядок, а не порядок MOF.</span><span class="sxs-lookup"><span data-stu-id="1744a-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="1744a-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1744a-109">Syntax</span></span>

``` syntax
class MSMCAInfo_RawCorrectedPlatformEvent : WMIEvent
{
  boolean         Active;
  uint32          Count;
  MSMCAInfo_Entry Records[];
};
```

## <a name="members"></a><span data-ttu-id="1744a-110">Члены</span><span class="sxs-lookup"><span data-stu-id="1744a-110">Members</span></span>

<span data-ttu-id="1744a-111">Класс **мсмкаинфо \_ равкорректедплатформевент** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="1744a-111">The **MSMCAInfo\_RawCorrectedPlatformEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="1744a-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="1744a-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1744a-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="1744a-113">Properties</span></span>

<span data-ttu-id="1744a-114">Класс **мсмкаинфо \_ равкорректедплатформевент** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="1744a-114">The **MSMCAInfo\_RawCorrectedPlatformEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1744a-115">**Активен**</span><span class="sxs-lookup"><span data-stu-id="1744a-115">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1744a-116">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="1744a-116">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1744a-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1744a-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1744a-118">Значение TRUE, если данный экземпляр класса активен; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="1744a-118">TRUE, if this instance of the class is active; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="1744a-119">**Количество**</span><span class="sxs-lookup"><span data-stu-id="1744a-119">**Count**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1744a-120">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1744a-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1744a-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1744a-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1744a-122">Число записей об ошибках.</span><span class="sxs-lookup"><span data-stu-id="1744a-122">Number of error records.</span></span>

</dd> <dt>

<span data-ttu-id="1744a-123">**Записи**</span><span class="sxs-lookup"><span data-stu-id="1744a-123">**Records**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1744a-124">Тип данных: **массив \_ записей мсмкаинфо**</span><span class="sxs-lookup"><span data-stu-id="1744a-124">Data type: **MSMCAInfo\_Entry** array</span></span>
</dt> <dt>

<span data-ttu-id="1744a-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1744a-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1744a-126">Массив записей об ошибках MCA.</span><span class="sxs-lookup"><span data-stu-id="1744a-126">Array of MCA error records.</span></span> <span data-ttu-id="1744a-127">Число записей об ошибках MCA в массиве задается свойством **Count** .</span><span class="sxs-lookup"><span data-stu-id="1744a-127">The number of MCA error records in the array is specified by the **Count** property.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1744a-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1744a-128">Remarks</span></span>

<span data-ttu-id="1744a-129">Класс **мсмкаинфо \_ равкорректедплатформевент** является производным от [**WMIEvent**](wmievent.md).</span><span class="sxs-lookup"><span data-stu-id="1744a-129">The **MSMCAInfo\_RawCorrectedPlatformEvent** class is derived from [**WMIEvent**](wmievent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1744a-130">Требования</span><span class="sxs-lookup"><span data-stu-id="1744a-130">Requirements</span></span>



| <span data-ttu-id="1744a-131">Требование</span><span class="sxs-lookup"><span data-stu-id="1744a-131">Requirement</span></span> | <span data-ttu-id="1744a-132">Значение</span><span class="sxs-lookup"><span data-stu-id="1744a-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1744a-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1744a-133">Minimum supported client</span></span><br/> | <span data-ttu-id="1744a-134">Windows XP</span><span class="sxs-lookup"><span data-stu-id="1744a-134">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="1744a-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1744a-135">Minimum supported server</span></span><br/> | <span data-ttu-id="1744a-136">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1744a-136">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="1744a-137">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="1744a-137">Namespace</span></span><br/>                | <span data-ttu-id="1744a-138">Корневой \\ инструментарий WMI</span><span class="sxs-lookup"><span data-stu-id="1744a-138">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="1744a-139">MOF</span><span class="sxs-lookup"><span data-stu-id="1744a-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1744a-140"><dt>Вмикоре. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1744a-140"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="1744a-141">DLL</span><span class="sxs-lookup"><span data-stu-id="1744a-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1744a-142"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1744a-142"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1744a-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1744a-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1744a-144">Классы МСМКА</span><span class="sxs-lookup"><span data-stu-id="1744a-144">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="1744a-145">**WMIEvent**</span><span class="sxs-lookup"><span data-stu-id="1744a-145">**WMIEvent**</span></span>](wmievent.md)
</dt> </dl>

 

 




