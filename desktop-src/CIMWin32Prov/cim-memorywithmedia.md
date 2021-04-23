---
description: Класс CIM \_ меморивисмедиа связывает физическую память с физическим носителем и его картриджем. Память обеспечивает идентификацию носителя и сохраняет данные, относящиеся к пользователю.
ms.assetid: 99806d2d-6575-431d-9149-dc8ea767146c
ms.tgt_platform: multiple
title: Класс CIM_MemoryWithMedia
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MemoryWithMedia
- CIM_MemoryWithMedia.Dependent
- CIM_MemoryWithMedia.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3b990f8ba842f313449b6f24f4e2ce59787f7841
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351635"
---
# <a name="cim_memorywithmedia-class"></a><span data-ttu-id="4b175-104">\_Класс CIM меморивисмедиа</span><span class="sxs-lookup"><span data-stu-id="4b175-104">CIM\_MemoryWithMedia class</span></span>

<span data-ttu-id="4b175-105">Класс **CIM \_ меморивисмедиа** связывает физическую память с физическим носителем и его картриджем.</span><span class="sxs-lookup"><span data-stu-id="4b175-105">The **CIM\_MemoryWithMedia** class associates physical memory with a physical media and its cartridge.</span></span> <span data-ttu-id="4b175-106">Память обеспечивает идентификацию носителя и сохраняет данные, относящиеся к пользователю.</span><span class="sxs-lookup"><span data-stu-id="4b175-106">The memory provides media identification and stores user-specific data.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4b175-107">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="4b175-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="4b175-108">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="4b175-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="4b175-109">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="4b175-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="4b175-110">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="4b175-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b175-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4b175-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B7E-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_MemoryWithMedia : CIM_Dependency
{
  CIM_PhysicalMedia  REF Dependent;
  CIM_PhysicalMemory REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="4b175-112">Члены</span><span class="sxs-lookup"><span data-stu-id="4b175-112">Members</span></span>

<span data-ttu-id="4b175-113">Класс **CIM \_ меморивисмедиа** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="4b175-113">The **CIM\_MemoryWithMedia** class has these types of members:</span></span>

-   [<span data-ttu-id="4b175-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="4b175-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4b175-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="4b175-115">Properties</span></span>

<span data-ttu-id="4b175-116">Класс **CIM \_ меморивисмедиа** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="4b175-116">The **CIM\_MemoryWithMedia** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4b175-117">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="4b175-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4b175-118">Тип данных: **CIM \_ фисикалмемори**</span><span class="sxs-lookup"><span data-stu-id="4b175-118">Data type: **CIM\_PhysicalMemory**</span></span>
</dt> <dt>

<span data-ttu-id="4b175-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4b175-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4b175-120">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="4b175-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="4b175-121">[**\_ Фисикалмемори CIM**](cim-physicalmemory.md) , описывающий память, связанную с физическим носителем.</span><span class="sxs-lookup"><span data-stu-id="4b175-121">A [**CIM\_PhysicalMemory**](cim-physicalmemory.md) that describes the memory associated with physical media.</span></span>

</dd> <dt>

<span data-ttu-id="4b175-122">**Него**</span><span class="sxs-lookup"><span data-stu-id="4b175-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4b175-123">Тип данных: **CIM \_ фисикалмедиа**</span><span class="sxs-lookup"><span data-stu-id="4b175-123">Data type: **CIM\_PhysicalMedia**</span></span>
</dt> <dt>

<span data-ttu-id="4b175-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4b175-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4b175-125">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")</span><span class="sxs-lookup"><span data-stu-id="4b175-125">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="4b175-126">[**\_ Фисикалмедиа CIM**](cim-physicalmedia.md) , описывающий физический носитель.</span><span class="sxs-lookup"><span data-stu-id="4b175-126">A [**CIM\_PhysicalMedia**](cim-physicalmedia.md) that describes the physical media.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4b175-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4b175-127">Remarks</span></span>

<span data-ttu-id="4b175-128">**Модель CIM \_ Меморивисмедиа** наследуется [**от \_ зависимости CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="4b175-128">**CIM\_MemoryWithMedia** is inherited from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="4b175-129">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="4b175-129">WMI does not implement this class.</span></span>

<span data-ttu-id="4b175-130">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="4b175-130">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="4b175-131">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="4b175-131">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b175-132">Требования</span><span class="sxs-lookup"><span data-stu-id="4b175-132">Requirements</span></span>



| <span data-ttu-id="4b175-133">Требование</span><span class="sxs-lookup"><span data-stu-id="4b175-133">Requirement</span></span> | <span data-ttu-id="4b175-134">Значение</span><span class="sxs-lookup"><span data-stu-id="4b175-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4b175-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4b175-135">Minimum supported client</span></span><br/> | <span data-ttu-id="4b175-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4b175-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4b175-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4b175-137">Minimum supported server</span></span><br/> | <span data-ttu-id="4b175-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4b175-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4b175-139">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="4b175-139">Namespace</span></span><br/>                | <span data-ttu-id="4b175-140">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="4b175-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4b175-141">MOF</span><span class="sxs-lookup"><span data-stu-id="4b175-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4b175-142"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4b175-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4b175-143">DLL</span><span class="sxs-lookup"><span data-stu-id="4b175-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4b175-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4b175-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b175-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4b175-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b175-146">**\_Зависимость CIM**</span><span class="sxs-lookup"><span data-stu-id="4b175-146">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

