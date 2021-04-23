---
description: Класс CIM \_ биослоадединнв связывает элемент BIOS и долговременное хранилище, в котором он загружается.
ms.assetid: 11641616-e11d-49ff-bfe4-f95fe27f00b8
ms.tgt_platform: multiple
title: Класс CIM_BIOSLoadedInNV
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BIOSLoadedInNV
- CIM_BIOSLoadedInNV.Dependent
- CIM_BIOSLoadedInNV.Antecedent
- CIM_BIOSLoadedInNV.EndingAddress
- CIM_BIOSLoadedInNV.StartingAddress
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0de07e1d4b886ad14f6a7fd8dbb96c1c0f2d2079
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990646"
---
# <a name="cim_biosloadedinnv-class"></a><span data-ttu-id="0a47a-103">\_Класс CIM биослоадединнв</span><span class="sxs-lookup"><span data-stu-id="0a47a-103">CIM\_BIOSLoadedInNV class</span></span>

<span data-ttu-id="0a47a-104">Класс **CIM \_ биослоадединнв** связывает элемент BIOS и долговременное хранилище, в котором он загружается.</span><span class="sxs-lookup"><span data-stu-id="0a47a-104">The **CIM\_BIOSLoadedInNV** class associates a BIOS element and the non-volatile storage in which it is loaded.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0a47a-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="0a47a-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="0a47a-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="0a47a-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="0a47a-107">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="0a47a-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="0a47a-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="0a47a-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a47a-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0a47a-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{524ED194-DB35-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_BIOSLoadedInNV : CIM_Dependency
{
  CIM_BIOSElement        REF Dependent;
  CIM_NonVolatileStorage REF Antecedent;
  uint64                     EndingAddress;
  uint64                     StartingAddress;
};
```

## <a name="members"></a><span data-ttu-id="0a47a-110">Члены</span><span class="sxs-lookup"><span data-stu-id="0a47a-110">Members</span></span>

<span data-ttu-id="0a47a-111">Класс **CIM \_ биослоадединнв** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="0a47a-111">The **CIM\_BIOSLoadedInNV** class has these types of members:</span></span>

-   [<span data-ttu-id="0a47a-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="0a47a-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0a47a-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="0a47a-113">Properties</span></span>

<span data-ttu-id="0a47a-114">Класс **CIM \_ биослоадединнв** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="0a47a-114">The **CIM\_BIOSLoadedInNV** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0a47a-115">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="0a47a-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a47a-116">Тип данных: **CIM \_ нонволатилестораже**</span><span class="sxs-lookup"><span data-stu-id="0a47a-116">Data type: **CIM\_NonVolatileStorage**</span></span>
</dt> <dt>

<span data-ttu-id="0a47a-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0a47a-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0a47a-118">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="0a47a-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="0a47a-119">[**\_ Нонволатилестораже CIM**](cim-nonvolatilestorage.md) , описывающий долговременное хранилище.</span><span class="sxs-lookup"><span data-stu-id="0a47a-119">A [**CIM\_NonVolatileStorage**](cim-nonvolatilestorage.md) that describes the non-volatile storage.</span></span>

</dd> <dt>

<span data-ttu-id="0a47a-120">**Него**</span><span class="sxs-lookup"><span data-stu-id="0a47a-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a47a-121">Тип данных: **CIM \_ биоселемент**</span><span class="sxs-lookup"><span data-stu-id="0a47a-121">Data type: **CIM\_BIOSElement**</span></span>
</dt> <dt>

<span data-ttu-id="0a47a-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0a47a-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0a47a-123">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")</span><span class="sxs-lookup"><span data-stu-id="0a47a-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="0a47a-124">[**\_ Биоселемент CIM**](cim-bioselement.md) , описывающий BIOS, хранящийся в энергонезависимым экстенте.</span><span class="sxs-lookup"><span data-stu-id="0a47a-124">A [**CIM\_BIOSElement**](cim-bioselement.md) that describes the BIOS stored in the non-volatile extent.</span></span>

</dd> <dt>

<span data-ttu-id="0a47a-125">**ендингаддресс**</span><span class="sxs-lookup"><span data-stu-id="0a47a-125">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a47a-126">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0a47a-126">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0a47a-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0a47a-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0a47a-128">Конечный адрес, по которому BIOS находится в долговременном хранилище.</span><span class="sxs-lookup"><span data-stu-id="0a47a-128">Ending address where the BIOS is located in non-volatile storage.</span></span>

<span data-ttu-id="0a47a-129">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="0a47a-129">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="0a47a-130">**стартингаддресс**</span><span class="sxs-lookup"><span data-stu-id="0a47a-130">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a47a-131">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0a47a-131">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0a47a-132">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0a47a-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0a47a-133">Начальный адрес, по которому BIOS находится в долговременном хранилище.</span><span class="sxs-lookup"><span data-stu-id="0a47a-133">Starting address where the BIOS is located in non-volatile storage.</span></span>

<span data-ttu-id="0a47a-134">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="0a47a-134">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0a47a-135">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0a47a-135">Remarks</span></span>

<span data-ttu-id="0a47a-136">Класс **CIM \_ биослоадединнв** является производным от [**\_ зависимости CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="0a47a-136">The **CIM\_BIOSLoadedInNV** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="0a47a-137">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="0a47a-137">WMI does not implement this class.</span></span>

<span data-ttu-id="0a47a-138">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="0a47a-138">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="0a47a-139">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="0a47a-139">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a47a-140">Требования</span><span class="sxs-lookup"><span data-stu-id="0a47a-140">Requirements</span></span>



| <span data-ttu-id="0a47a-141">Требование</span><span class="sxs-lookup"><span data-stu-id="0a47a-141">Requirement</span></span> | <span data-ttu-id="0a47a-142">Значение</span><span class="sxs-lookup"><span data-stu-id="0a47a-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0a47a-143">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0a47a-143">Minimum supported client</span></span><br/> | <span data-ttu-id="0a47a-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0a47a-144">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0a47a-145">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0a47a-145">Minimum supported server</span></span><br/> | <span data-ttu-id="0a47a-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0a47a-146">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0a47a-147">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="0a47a-147">Namespace</span></span><br/>                | <span data-ttu-id="0a47a-148">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="0a47a-148">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0a47a-149">MOF</span><span class="sxs-lookup"><span data-stu-id="0a47a-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0a47a-150"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0a47a-150"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0a47a-151">DLL</span><span class="sxs-lookup"><span data-stu-id="0a47a-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0a47a-152"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0a47a-152"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a47a-153">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0a47a-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a47a-154">**\_Зависимость CIM**</span><span class="sxs-lookup"><span data-stu-id="0a47a-154">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

