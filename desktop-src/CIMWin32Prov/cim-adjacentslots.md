---
description: '\_Ассоциация АДЖАЦЕНТСЛОТС CIM описывает расположение слотов на плате размещения или адаптере карты.'
ms.assetid: d604647f-7b2f-4f99-8d98-adf115ae9dfb
ms.tgt_platform: multiple
title: Класс CIM_AdjacentSlots
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AdjacentSlots
- CIM_AdjacentSlots.DistanceBetweenSlots
- CIM_AdjacentSlots.SharedSlots
- CIM_AdjacentSlots.SlotA
- CIM_AdjacentSlots.SlotB
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 695f9c668d6f75864e46026deac9a969993596ff
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142109"
---
# <a name="cim_adjacentslots-class"></a><span data-ttu-id="1b7dd-103">\_Класс CIM аджацентслотс</span><span class="sxs-lookup"><span data-stu-id="1b7dd-103">CIM\_AdjacentSlots class</span></span>

<span data-ttu-id="1b7dd-104">Ассоциация **\_ аджацентслотс CIM** описывает расположение слотов на плате размещения или адаптере карты.</span><span class="sxs-lookup"><span data-stu-id="1b7dd-104">The **CIM\_AdjacentSlots** association describes the layout of slots on a hosting board or adapter card.</span></span> <span data-ttu-id="1b7dd-105">Такие сведения, как расстояние между слотами и то, являются ли они общими (если один из них заполнен, другие слоты не могут использоваться), передаются как свойства связи.</span><span class="sxs-lookup"><span data-stu-id="1b7dd-105">Information, such as the distance between the slots and whether they are "shared" (if one is populated, then the other slot cannot be used), is conveyed as association properties.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1b7dd-106">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="1b7dd-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="1b7dd-107">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="1b7dd-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="1b7dd-108">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="1b7dd-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="1b7dd-109">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="1b7dd-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b7dd-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1b7dd-110">Syntax</span></span>

``` syntax
[Abstract, Association, UUID("{FAF76B88-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_AdjacentSlots
{
  real32       DistanceBetweenSlots;
  boolean      SharedSlots;
  CIM_Slot REF SlotA;
  CIM_Slot REF SlotB;
};
```

## <a name="members"></a><span data-ttu-id="1b7dd-111">Члены</span><span class="sxs-lookup"><span data-stu-id="1b7dd-111">Members</span></span>

<span data-ttu-id="1b7dd-112">Класс **CIM \_ аджацентслотс** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="1b7dd-112">The **CIM\_AdjacentSlots** class has these types of members:</span></span>

-   [<span data-ttu-id="1b7dd-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="1b7dd-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1b7dd-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="1b7dd-114">Properties</span></span>

<span data-ttu-id="1b7dd-115">Класс **CIM \_ аджацентслотс** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="1b7dd-115">The **CIM\_AdjacentSlots** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1b7dd-116">**дистанцебетвинслотс**</span><span class="sxs-lookup"><span data-stu-id="1b7dd-116">**DistanceBetweenSlots**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b7dd-117">Тип данных: **real32**</span><span class="sxs-lookup"><span data-stu-id="1b7dd-117">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="1b7dd-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1b7dd-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1b7dd-119">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("дюймы")</span><span class="sxs-lookup"><span data-stu-id="1b7dd-119">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="1b7dd-120">Расстояние в дюймах между соседними слотами.</span><span class="sxs-lookup"><span data-stu-id="1b7dd-120">Distance, in inches, between adjacent slots.</span></span>

</dd> <dt>

<span data-ttu-id="1b7dd-121">**шаредслотс**</span><span class="sxs-lookup"><span data-stu-id="1b7dd-121">**SharedSlots**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b7dd-122">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="1b7dd-122">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1b7dd-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1b7dd-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1b7dd-124">Если **значение равно true**, один из слотов заполняется платой адаптера; другой слот необходимо оставить пустым.</span><span class="sxs-lookup"><span data-stu-id="1b7dd-124">If **TRUE**, one of the slots is populated by an adapter card; the other slot must be left empty.</span></span>

</dd> <dt>

<span data-ttu-id="1b7dd-125">**Разъем a**</span><span class="sxs-lookup"><span data-stu-id="1b7dd-125">**SlotA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b7dd-126">Тип данных: **\_ слот CIM**</span><span class="sxs-lookup"><span data-stu-id="1b7dd-126">Data type: **CIM\_Slot**</span></span>
</dt> <dt>

<span data-ttu-id="1b7dd-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1b7dd-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1b7dd-128">Ссылка на один из соседних слотов.</span><span class="sxs-lookup"><span data-stu-id="1b7dd-128">Reference to one of the adjacent slots.</span></span>

</dd> <dt>

<span data-ttu-id="1b7dd-129">**слотб**</span><span class="sxs-lookup"><span data-stu-id="1b7dd-129">**SlotB**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b7dd-130">Тип данных: **\_ слот CIM**</span><span class="sxs-lookup"><span data-stu-id="1b7dd-130">Data type: **CIM\_Slot**</span></span>
</dt> <dt>

<span data-ttu-id="1b7dd-131">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1b7dd-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1b7dd-132">Ссылка на смежный слот.</span><span class="sxs-lookup"><span data-stu-id="1b7dd-132">Reference to the "other" adjacent slot.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1b7dd-133">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1b7dd-133">Remarks</span></span>

<span data-ttu-id="1b7dd-134">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="1b7dd-134">WMI does not implement this class.</span></span>

<span data-ttu-id="1b7dd-135">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="1b7dd-135">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="1b7dd-136">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="1b7dd-136">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b7dd-137">Требования</span><span class="sxs-lookup"><span data-stu-id="1b7dd-137">Requirements</span></span>



| <span data-ttu-id="1b7dd-138">Требование</span><span class="sxs-lookup"><span data-stu-id="1b7dd-138">Requirement</span></span> | <span data-ttu-id="1b7dd-139">Значение</span><span class="sxs-lookup"><span data-stu-id="1b7dd-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1b7dd-140">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1b7dd-140">Minimum supported client</span></span><br/> | <span data-ttu-id="1b7dd-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1b7dd-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1b7dd-142">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1b7dd-142">Minimum supported server</span></span><br/> | <span data-ttu-id="1b7dd-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1b7dd-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1b7dd-144">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="1b7dd-144">Namespace</span></span><br/>                | <span data-ttu-id="1b7dd-145">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="1b7dd-145">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1b7dd-146">MOF</span><span class="sxs-lookup"><span data-stu-id="1b7dd-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1b7dd-147"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1b7dd-147"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1b7dd-148">DLL</span><span class="sxs-lookup"><span data-stu-id="1b7dd-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1b7dd-149"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1b7dd-149"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b7dd-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1b7dd-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b7dd-151">Классы CIM</span><span class="sxs-lookup"><span data-stu-id="1b7dd-151">CIM Classes</span></span>](/windows/desktop/WmiSdk/cimclas)
</dt> </dl>

 

