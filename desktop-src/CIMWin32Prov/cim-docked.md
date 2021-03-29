---
description: '\_Прикрепленная Ассоциация CIM представляет связь между двумя корпусами. Например, портативный компьютер (тип корпуса) можно закрепить на стыковочный станции (другой тип корпуса). Эта типичная связь описана явно.'
ms.assetid: 72cb36bb-f79e-4d1a-a859-4024031e4ebc
ms.tgt_platform: multiple
title: Класс CIM_Docked
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Docked
- CIM_Docked.Dependent
- CIM_Docked.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 899b85d63293861f0a36df3d3c30610f8cff05ac
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807517"
---
# <a name="cim_docked-class"></a><span data-ttu-id="33d1d-105">\_Закрепленный класс CIM</span><span class="sxs-lookup"><span data-stu-id="33d1d-105">CIM\_Docked class</span></span>

<span data-ttu-id="33d1d-106">**\_ Прикрепленная Ассоциация CIM** представляет связь между двумя корпусами.</span><span class="sxs-lookup"><span data-stu-id="33d1d-106">The **CIM\_Docked** association represents the relationship between two chassis.</span></span> <span data-ttu-id="33d1d-107">Например, портативный компьютер (тип корпуса) можно закрепить на стыковочный станции (другой тип корпуса).</span><span class="sxs-lookup"><span data-stu-id="33d1d-107">For example, a laptop (a type of chassis) can be docked in a docking station (another type of chassis).</span></span> <span data-ttu-id="33d1d-108">Эта типичная связь описана явно.</span><span class="sxs-lookup"><span data-stu-id="33d1d-108">This typical relationship is explicitly described.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="33d1d-109">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="33d1d-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="33d1d-110">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="33d1d-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="33d1d-111">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="33d1d-111">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="33d1d-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="33d1d-112">Syntax</span></span>

``` syntax
[Abstract, MappingStrings("MIF.DMTF|Dynamic States|001.2"), UUID("{FAF76B75-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_Docked : CIM_Dependency
{
  CIM_Chassis REF Dependent;
  CIM_Chassis REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="33d1d-113">Члены</span><span class="sxs-lookup"><span data-stu-id="33d1d-113">Members</span></span>

<span data-ttu-id="33d1d-114">**\_ Закрепленный класс CIM** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="33d1d-114">The **CIM\_Docked** class has these types of members:</span></span>

-   [<span data-ttu-id="33d1d-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="33d1d-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="33d1d-116">Свойства</span><span class="sxs-lookup"><span data-stu-id="33d1d-116">Properties</span></span>

<span data-ttu-id="33d1d-117">**\_ Прикрепленный класс CIM** имеет эти свойства.</span><span class="sxs-lookup"><span data-stu-id="33d1d-117">The **CIM\_Docked** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="33d1d-118">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="33d1d-118">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33d1d-119">Тип данных: **CIM \_ Chassis**</span><span class="sxs-lookup"><span data-stu-id="33d1d-119">Data type: **CIM\_Chassis**</span></span>
</dt> <dt>

<span data-ttu-id="33d1d-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="33d1d-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="33d1d-121">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="33d1d-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="33d1d-122">[**\_ Корпус CIM**](cim-chassis.md) , описывающий станцию стыковки.</span><span class="sxs-lookup"><span data-stu-id="33d1d-122">A [**CIM\_Chassis**](cim-chassis.md) describing the docking station.</span></span>

</dd> <dt>

<span data-ttu-id="33d1d-123">**Него**</span><span class="sxs-lookup"><span data-stu-id="33d1d-123">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33d1d-124">Тип данных: **CIM \_ Chassis**</span><span class="sxs-lookup"><span data-stu-id="33d1d-124">Data type: **CIM\_Chassis**</span></span>
</dt> <dt>

<span data-ttu-id="33d1d-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="33d1d-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="33d1d-126">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="33d1d-126">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="33d1d-127">[**\_ Корпус CIM**](cim-chassis.md) , описывающий закрепленный портативный компьютер.</span><span class="sxs-lookup"><span data-stu-id="33d1d-127">A [**CIM\_Chassis**](cim-chassis.md) describing the docked laptop.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="33d1d-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="33d1d-128">Remarks</span></span>

<span data-ttu-id="33d1d-129">**\_ Закрепленный класс CIM** является производным от [**\_ зависимости CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="33d1d-129">The **CIM\_Docked** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="33d1d-130">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="33d1d-130">WMI does not implement this class.</span></span>

<span data-ttu-id="33d1d-131">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="33d1d-131">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="33d1d-132">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="33d1d-132">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="33d1d-133">Требования</span><span class="sxs-lookup"><span data-stu-id="33d1d-133">Requirements</span></span>



| <span data-ttu-id="33d1d-134">Требование</span><span class="sxs-lookup"><span data-stu-id="33d1d-134">Requirement</span></span> | <span data-ttu-id="33d1d-135">Значение</span><span class="sxs-lookup"><span data-stu-id="33d1d-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="33d1d-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="33d1d-136">Minimum supported client</span></span><br/> | <span data-ttu-id="33d1d-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="33d1d-137">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="33d1d-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="33d1d-138">Minimum supported server</span></span><br/> | <span data-ttu-id="33d1d-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="33d1d-139">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="33d1d-140">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="33d1d-140">Namespace</span></span><br/>                | <span data-ttu-id="33d1d-141">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="33d1d-141">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="33d1d-142">MOF</span><span class="sxs-lookup"><span data-stu-id="33d1d-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="33d1d-143"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="33d1d-143"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="33d1d-144">DLL</span><span class="sxs-lookup"><span data-stu-id="33d1d-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="33d1d-145"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="33d1d-145"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33d1d-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="33d1d-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33d1d-147">**\_Зависимость CIM**</span><span class="sxs-lookup"><span data-stu-id="33d1d-147">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

