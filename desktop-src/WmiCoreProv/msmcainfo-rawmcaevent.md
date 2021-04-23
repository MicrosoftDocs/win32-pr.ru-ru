---
description: Содержит событие архитектуры проверки компьютера (MCA). Этот класс доступен только в 64-разрядных системах Windows.
ms.assetid: d1806b91-43a3-4329-8fe5-de1e4755740f
title: Класс MSMCAInfo_RawMCAEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAInfo_RawMCAEvent
- MSMCAInfo_RawMCAEvent.Active
- MSMCAInfo_RawMCAEvent.Count
- MSMCAInfo_RawMCAEvent.InstanceName
- MSMCAInfo_RawMCAEvent.Records
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: e15af79c67265823e0025849e4c2ef27f690265c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999199"
---
# <a name="msmcainfo_rawmcaevent-class"></a><span data-ttu-id="c337c-104">\_Класс мсмкаинфо равмкаевент</span><span class="sxs-lookup"><span data-stu-id="c337c-104">MSMCAInfo\_RawMCAEvent class</span></span>

<span data-ttu-id="c337c-105">Класс **мсмкаинфо \_ равмкаевент** содержит событие архитектура проверки компьютера (MCA).</span><span class="sxs-lookup"><span data-stu-id="c337c-105">The **MSMCAInfo\_RawMCAEvent** class contains a Machine Check Architecture (MCA) event.</span></span> <span data-ttu-id="c337c-106">Этот класс доступен только в 64-разрядных системах Windows.</span><span class="sxs-lookup"><span data-stu-id="c337c-106">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="c337c-107">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="c337c-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="c337c-108">Свойства и методы имеют алфавитный порядок, а не порядок MOF.</span><span class="sxs-lookup"><span data-stu-id="c337c-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c337c-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c337c-109">Syntax</span></span>

``` syntax
class MSMCAInfo_RawMCAEvent : WMIEvent
{
  boolean         Active;
  uint32          Count;
  string          InstanceName;
  MSMCAInfo_Entry Records[];
};
```

## <a name="members"></a><span data-ttu-id="c337c-110">Члены</span><span class="sxs-lookup"><span data-stu-id="c337c-110">Members</span></span>

<span data-ttu-id="c337c-111">Класс **мсмкаинфо \_ равмкаевент** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="c337c-111">The **MSMCAInfo\_RawMCAEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="c337c-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="c337c-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c337c-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="c337c-113">Properties</span></span>

<span data-ttu-id="c337c-114">Класс **мсмкаинфо \_ равмкаевент** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="c337c-114">The **MSMCAInfo\_RawMCAEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c337c-115">**Активен**</span><span class="sxs-lookup"><span data-stu-id="c337c-115">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c337c-116">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="c337c-116">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c337c-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c337c-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c337c-118">Значение TRUE, если данный экземпляр класса активен; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="c337c-118">TRUE, if this instance of the class is active; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="c337c-119">**Количество**</span><span class="sxs-lookup"><span data-stu-id="c337c-119">**Count**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c337c-120">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c337c-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c337c-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c337c-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c337c-122">Число записей об ошибках.</span><span class="sxs-lookup"><span data-stu-id="c337c-122">Number of error records.</span></span>

</dd> <dt>

<span data-ttu-id="c337c-123">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="c337c-123">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c337c-124">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c337c-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c337c-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c337c-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c337c-126">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c337c-126">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c337c-127">Строка, однозначно идентифицирующая данный экземпляр класса **мсмкаинфо \_ равмкаевент** .</span><span class="sxs-lookup"><span data-stu-id="c337c-127">String that uniquely identifies this instance of the **MSMCAInfo\_RawMCAEvent** class.</span></span>

</dd> <dt>

<span data-ttu-id="c337c-128">**Записи**</span><span class="sxs-lookup"><span data-stu-id="c337c-128">**Records**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c337c-129">Тип данных: **массив \_ записей мсмкаинфо**</span><span class="sxs-lookup"><span data-stu-id="c337c-129">Data type: **MSMCAInfo\_Entry** array</span></span>
</dt> <dt>

<span data-ttu-id="c337c-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c337c-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c337c-131">Массив записей об ошибках MCA.</span><span class="sxs-lookup"><span data-stu-id="c337c-131">Array of MCA error records.</span></span> <span data-ttu-id="c337c-132">Число записей об ошибках MCA в массиве задается свойством **Count** .</span><span class="sxs-lookup"><span data-stu-id="c337c-132">The number of MCA error records in the array is specified by the **Count** property.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c337c-133">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c337c-133">Remarks</span></span>

<span data-ttu-id="c337c-134">Класс **мсмкаинфо \_ равмкаевент** является производным от [**WMIEvent**](wmievent.md).</span><span class="sxs-lookup"><span data-stu-id="c337c-134">The **MSMCAInfo\_RawMCAEvent** class is derived from [**WMIEvent**](wmievent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c337c-135">Требования</span><span class="sxs-lookup"><span data-stu-id="c337c-135">Requirements</span></span>



| <span data-ttu-id="c337c-136">Требование</span><span class="sxs-lookup"><span data-stu-id="c337c-136">Requirement</span></span> | <span data-ttu-id="c337c-137">Значение</span><span class="sxs-lookup"><span data-stu-id="c337c-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c337c-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c337c-138">Minimum supported client</span></span><br/> | <span data-ttu-id="c337c-139">Windows XP</span><span class="sxs-lookup"><span data-stu-id="c337c-139">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="c337c-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c337c-140">Minimum supported server</span></span><br/> | <span data-ttu-id="c337c-141">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c337c-141">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="c337c-142">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="c337c-142">Namespace</span></span><br/>                | <span data-ttu-id="c337c-143">Корневой \\ инструментарий WMI</span><span class="sxs-lookup"><span data-stu-id="c337c-143">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="c337c-144">MOF</span><span class="sxs-lookup"><span data-stu-id="c337c-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c337c-145"><dt>Вмикоре. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c337c-145"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="c337c-146">DLL</span><span class="sxs-lookup"><span data-stu-id="c337c-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c337c-147"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c337c-147"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c337c-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c337c-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c337c-149">Классы МСМКА</span><span class="sxs-lookup"><span data-stu-id="c337c-149">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="c337c-150">**WMIEvent**</span><span class="sxs-lookup"><span data-stu-id="c337c-150">**WMIEvent**</span></span>](wmievent.md)
</dt> </dl>

 

