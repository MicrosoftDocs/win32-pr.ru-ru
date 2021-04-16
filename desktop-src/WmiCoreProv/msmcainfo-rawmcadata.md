---
description: Указывает журналы необработанных проверок компьютеров (MCA). Этот класс доступен только в 64-разрядных системах Windows.
ms.assetid: d465ba8d-14b2-4911-ae19-19ebeb32126e
title: Класс MSMCAInfo_RawMCAData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAInfo_RawMCAData
- MSMCAInfo_RawMCAData.Active
- MSMCAInfo_RawMCAData.Count
- MSMCAInfo_RawMCAData.InstanceName
- MSMCAInfo_RawMCAData.Records
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 6cafc16ddbc91181cc2114def07a193941988228
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541495"
---
# <a name="msmcainfo_rawmcadata-class"></a><span data-ttu-id="eb12d-104">\_Класс мсмкаинфо равмкадата</span><span class="sxs-lookup"><span data-stu-id="eb12d-104">MSMCAInfo\_RawMCAData class</span></span>

<span data-ttu-id="eb12d-105">**Мсмкаинфо \_ равмкадата** указывает журнал необработанных проверок машин (MCA).</span><span class="sxs-lookup"><span data-stu-id="eb12d-105">The **MSMCAInfo\_RawMCAData** specifies the raw Machine Check Architecture (MCA) logs.</span></span> <span data-ttu-id="eb12d-106">Этот класс доступен только в 64-разрядных системах Windows.</span><span class="sxs-lookup"><span data-stu-id="eb12d-106">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="eb12d-107">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="eb12d-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="eb12d-108">Свойства и методы имеют алфавитный порядок, а не порядок MOF.</span><span class="sxs-lookup"><span data-stu-id="eb12d-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb12d-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="eb12d-109">Syntax</span></span>

``` syntax
class MSMCAInfo_RawMCAData : MSMCAInfo
{
  boolean         Active;
  uint32          Count;
  string          InstanceName;
  MSMCAInfo_Entry Records[];
};
```

## <a name="members"></a><span data-ttu-id="eb12d-110">Члены</span><span class="sxs-lookup"><span data-stu-id="eb12d-110">Members</span></span>

<span data-ttu-id="eb12d-111">Класс **мсмкаинфо \_ равмкадата** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="eb12d-111">The **MSMCAInfo\_RawMCAData** class has these types of members:</span></span>

-   [<span data-ttu-id="eb12d-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="eb12d-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="eb12d-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="eb12d-113">Properties</span></span>

<span data-ttu-id="eb12d-114">Класс **мсмкаинфо \_ равмкадата** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="eb12d-114">The **MSMCAInfo\_RawMCAData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="eb12d-115">**Активен**</span><span class="sxs-lookup"><span data-stu-id="eb12d-115">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb12d-116">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="eb12d-116">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="eb12d-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="eb12d-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb12d-118">Значение TRUE, если данный экземпляр класса активен; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="eb12d-118">TRUE, if this instance of the class is active; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="eb12d-119">**Количество**</span><span class="sxs-lookup"><span data-stu-id="eb12d-119">**Count**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb12d-120">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="eb12d-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="eb12d-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="eb12d-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb12d-122">Число записей об ошибках.</span><span class="sxs-lookup"><span data-stu-id="eb12d-122">Number of error records.</span></span>

</dd> <dt>

<span data-ttu-id="eb12d-123">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="eb12d-123">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb12d-124">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="eb12d-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb12d-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="eb12d-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb12d-126">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="eb12d-126">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="eb12d-127">Уникальный идентификатор этого экземпляра класса.</span><span class="sxs-lookup"><span data-stu-id="eb12d-127">Unique identifier of this instance of the class.</span></span>

</dd> <dt>

<span data-ttu-id="eb12d-128">**Записи**</span><span class="sxs-lookup"><span data-stu-id="eb12d-128">**Records**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb12d-129">Тип данных: **массив \_ записей мсмкаинфо**</span><span class="sxs-lookup"><span data-stu-id="eb12d-129">Data type: **MSMCAInfo\_Entry** array</span></span>
</dt> <dt>

<span data-ttu-id="eb12d-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="eb12d-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb12d-131">Массив записей об ошибках MCA.</span><span class="sxs-lookup"><span data-stu-id="eb12d-131">Array of MCA error records.</span></span> <span data-ttu-id="eb12d-132">Число записей об ошибках MCA в массиве задается свойством **Count** .</span><span class="sxs-lookup"><span data-stu-id="eb12d-132">The number of MCA error records in the array is specified by the **Count** property.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="eb12d-133">Комментарии</span><span class="sxs-lookup"><span data-stu-id="eb12d-133">Remarks</span></span>

<span data-ttu-id="eb12d-134">Класс **мсмкаинфо \_ равмкадата** является производным от [**мсмкаинфо**](msmcainfo.md).</span><span class="sxs-lookup"><span data-stu-id="eb12d-134">The **MSMCAInfo\_RawMCAData** class is derived from [**MSMCAInfo**](msmcainfo.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="eb12d-135">Требования</span><span class="sxs-lookup"><span data-stu-id="eb12d-135">Requirements</span></span>



| <span data-ttu-id="eb12d-136">Требование</span><span class="sxs-lookup"><span data-stu-id="eb12d-136">Requirement</span></span> | <span data-ttu-id="eb12d-137">Значение</span><span class="sxs-lookup"><span data-stu-id="eb12d-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="eb12d-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="eb12d-138">Minimum supported client</span></span><br/> | <span data-ttu-id="eb12d-139">Windows XP</span><span class="sxs-lookup"><span data-stu-id="eb12d-139">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="eb12d-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="eb12d-140">Minimum supported server</span></span><br/> | <span data-ttu-id="eb12d-141">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="eb12d-141">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="eb12d-142">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="eb12d-142">Namespace</span></span><br/>                | <span data-ttu-id="eb12d-143">Корневой \\ инструментарий WMI</span><span class="sxs-lookup"><span data-stu-id="eb12d-143">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="eb12d-144">MOF</span><span class="sxs-lookup"><span data-stu-id="eb12d-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="eb12d-145"><dt>Вмикоре. mof</dt></span><span class="sxs-lookup"><span data-stu-id="eb12d-145"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="eb12d-146">DLL</span><span class="sxs-lookup"><span data-stu-id="eb12d-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eb12d-147"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eb12d-147"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb12d-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="eb12d-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb12d-149">Классы МСМКА</span><span class="sxs-lookup"><span data-stu-id="eb12d-149">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="eb12d-150">**мсмкаинфо**</span><span class="sxs-lookup"><span data-stu-id="eb12d-150">**MSMCAInfo**</span></span>](msmcainfo.md)
</dt> </dl>

 

