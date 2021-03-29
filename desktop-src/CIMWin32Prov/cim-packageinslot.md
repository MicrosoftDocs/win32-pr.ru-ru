---
description: Ассоциация CIM \_ паккажеинслот представляет связь между картами устройств и шасси, в котором они подключены.
ms.assetid: 439f28a8-24fd-4a53-9d42-48fabb58e84a
ms.tgt_platform: multiple
title: Класс CIM_PackageInSlot
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PackageInSlot
- CIM_PackageInSlot.Dependent
- CIM_PackageInSlot.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a17e133f16f838d6353b6d74ee2054bd5ec52cd0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141079"
---
# <a name="cim_packageinslot-class"></a><span data-ttu-id="6f3c4-103">\_Класс CIM паккажеинслот</span><span class="sxs-lookup"><span data-stu-id="6f3c4-103">CIM\_PackageInSlot class</span></span>

<span data-ttu-id="6f3c4-104">Ассоциация **CIM \_ паккажеинслот** представляет связь между картами устройств и шасси, в котором они подключены.</span><span class="sxs-lookup"><span data-stu-id="6f3c4-104">The **CIM\_PackageInSlot** association represents the relationship between device cards and the chassis in which they are mounted.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6f3c4-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="6f3c4-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="6f3c4-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="6f3c4-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="6f3c4-107">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="6f3c4-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="6f3c4-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="6f3c4-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f3c4-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6f3c4-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B89-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PackageInSlot : CIM_Dependency
{
  CIM_PhysicalPackage REF Dependent;
  CIM_Slot            REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="6f3c4-110">Члены</span><span class="sxs-lookup"><span data-stu-id="6f3c4-110">Members</span></span>

<span data-ttu-id="6f3c4-111">Класс **CIM \_ паккажеинслот** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="6f3c4-111">The **CIM\_PackageInSlot** class has these types of members:</span></span>

-   [<span data-ttu-id="6f3c4-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="6f3c4-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6f3c4-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="6f3c4-113">Properties</span></span>

<span data-ttu-id="6f3c4-114">Класс **CIM \_ паккажеинслот** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="6f3c4-114">The **CIM\_PackageInSlot** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6f3c4-115">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="6f3c4-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f3c4-116">Тип данных: **\_ слот CIM**</span><span class="sxs-lookup"><span data-stu-id="6f3c4-116">Data type: **CIM\_Slot**</span></span>
</dt> <dt>

<span data-ttu-id="6f3c4-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6f3c4-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f3c4-118">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="6f3c4-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="6f3c4-119">[**\_ Слот CIM**](cim-slot.md) , описывающий слот, в который вставляется физический пакет.</span><span class="sxs-lookup"><span data-stu-id="6f3c4-119">A [**CIM\_Slot**](cim-slot.md) describing the slot into which the physical package is inserted.</span></span>

</dd> <dt>

<span data-ttu-id="6f3c4-120">**Него**</span><span class="sxs-lookup"><span data-stu-id="6f3c4-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f3c4-121">Тип данных: **CIM \_ фисикалпаккаже**</span><span class="sxs-lookup"><span data-stu-id="6f3c4-121">Data type: **CIM\_PhysicalPackage**</span></span>
</dt> <dt>

<span data-ttu-id="6f3c4-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6f3c4-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f3c4-123">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="6f3c4-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="6f3c4-124">[**\_ Фисикалпаккаже CIM**](cim-physicalpackage.md) , описывающий пакет в слоте.</span><span class="sxs-lookup"><span data-stu-id="6f3c4-124">A [**CIM\_PhysicalPackage**](cim-physicalpackage.md) describing the package in the slot.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6f3c4-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6f3c4-125">Remarks</span></span>

<span data-ttu-id="6f3c4-126">**Модель CIM \_ Паккажеинслот** является производным [**от \_ зависимости CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="6f3c4-126">**CIM\_PackageInSlot** is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="6f3c4-127">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="6f3c4-127">WMI does not implement this class.</span></span>

<span data-ttu-id="6f3c4-128">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="6f3c4-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="6f3c4-129">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="6f3c4-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f3c4-130">Требования</span><span class="sxs-lookup"><span data-stu-id="6f3c4-130">Requirements</span></span>



| <span data-ttu-id="6f3c4-131">Требование</span><span class="sxs-lookup"><span data-stu-id="6f3c4-131">Requirement</span></span> | <span data-ttu-id="6f3c4-132">Значение</span><span class="sxs-lookup"><span data-stu-id="6f3c4-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6f3c4-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6f3c4-133">Minimum supported client</span></span><br/> | <span data-ttu-id="6f3c4-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6f3c4-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6f3c4-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6f3c4-135">Minimum supported server</span></span><br/> | <span data-ttu-id="6f3c4-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6f3c4-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6f3c4-137">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="6f3c4-137">Namespace</span></span><br/>                | <span data-ttu-id="6f3c4-138">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="6f3c4-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6f3c4-139">MOF</span><span class="sxs-lookup"><span data-stu-id="6f3c4-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6f3c4-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6f3c4-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6f3c4-141">DLL</span><span class="sxs-lookup"><span data-stu-id="6f3c4-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6f3c4-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6f3c4-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f3c4-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6f3c4-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f3c4-144">**\_Зависимость CIM**</span><span class="sxs-lookup"><span data-stu-id="6f3c4-144">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

