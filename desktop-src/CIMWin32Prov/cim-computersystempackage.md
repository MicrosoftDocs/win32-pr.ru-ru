---
description: Класс CIM \_ компутерсистемпаккаже представляет ассоциацию, которая явно определяет связь между едиными системами компьютеров и одним или несколькими физическими пакетами.
ms.assetid: a91bf09d-0768-4d2a-a0e5-16237b2e6ddc
ms.tgt_platform: multiple
title: Класс CIM_ComputerSystemPackage
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ComputerSystemPackage
- CIM_ComputerSystemPackage.Dependent
- CIM_ComputerSystemPackage.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a5a2f166c4494b6120bfc5e2aaedeaba4721b155
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990636"
---
# <a name="cim_computersystempackage-class"></a><span data-ttu-id="4b4a9-103">\_Класс CIM компутерсистемпаккаже</span><span class="sxs-lookup"><span data-stu-id="4b4a9-103">CIM\_ComputerSystemPackage class</span></span>

<span data-ttu-id="4b4a9-104">Класс **CIM \_ компутерсистемпаккаже** представляет ассоциацию, которая явно определяет связь между едиными системами компьютеров и одним или несколькими физическими пакетами.</span><span class="sxs-lookup"><span data-stu-id="4b4a9-104">The **CIM\_ComputerSystemPackage** class represents an association that explicitly defines the relationship between unitary computer systems and one or more physical packages.</span></span> <span data-ttu-id="4b4a9-105">Ассоциация аналогична тому, как логические устройства реализуются физическими элементами.</span><span class="sxs-lookup"><span data-stu-id="4b4a9-105">The association is similar to the way that logical devices are realized by physical elements.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4b4a9-106">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="4b4a9-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="4b4a9-107">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="4b4a9-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="4b4a9-108">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="4b4a9-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="4b4a9-109">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="4b4a9-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b4a9-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4b4a9-110">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B8D-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_ComputerSystemPackage : CIM_Dependency
{
  CIM_UnitaryComputerSystem REF Dependent;
  CIM_PhysicalPackage       REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="4b4a9-111">Члены</span><span class="sxs-lookup"><span data-stu-id="4b4a9-111">Members</span></span>

<span data-ttu-id="4b4a9-112">Класс **CIM \_ компутерсистемпаккаже** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="4b4a9-112">The **CIM\_ComputerSystemPackage** class has these types of members:</span></span>

-   [<span data-ttu-id="4b4a9-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="4b4a9-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4b4a9-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="4b4a9-114">Properties</span></span>

<span data-ttu-id="4b4a9-115">Класс **CIM \_ компутерсистемпаккаже** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="4b4a9-115">The **CIM\_ComputerSystemPackage** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4b4a9-116">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="4b4a9-116">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4b4a9-117">Тип данных: **CIM \_ фисикалпаккаже**</span><span class="sxs-lookup"><span data-stu-id="4b4a9-117">Data type: **CIM\_PhysicalPackage**</span></span>
</dt> <dt>

<span data-ttu-id="4b4a9-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4b4a9-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4b4a9-119">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="4b4a9-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="4b4a9-120">[**\_ Фисикалпаккаже CIM**](cim-physicalpackage.md) , описывающий физические пакеты, которые реализуют единую компьютерную систему.</span><span class="sxs-lookup"><span data-stu-id="4b4a9-120">A [**CIM\_PhysicalPackage**](cim-physicalpackage.md) that describes the physical package(s) that realize a unitary computer system.</span></span>

</dd> <dt>

<span data-ttu-id="4b4a9-121">**Него**</span><span class="sxs-lookup"><span data-stu-id="4b4a9-121">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4b4a9-122">Тип данных: **CIM \_ унитарикомпутерсистем**</span><span class="sxs-lookup"><span data-stu-id="4b4a9-122">Data type: **CIM\_UnitaryComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="4b4a9-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4b4a9-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4b4a9-124">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")</span><span class="sxs-lookup"><span data-stu-id="4b4a9-124">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="4b4a9-125">[**\_ Унитарикомпутерсистем CIM**](cim-unitarycomputersystem.md) , описывающий единую компьютерную систему.</span><span class="sxs-lookup"><span data-stu-id="4b4a9-125">A [**CIM\_UnitaryComputerSystem**](cim-unitarycomputersystem.md) that describes the unitary computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4b4a9-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4b4a9-126">Remarks</span></span>

<span data-ttu-id="4b4a9-127">Класс **CIM \_ компутерсистемпаккаже** является производным от [**\_ зависимости CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="4b4a9-127">The **CIM\_ComputerSystemPackage** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="4b4a9-128">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="4b4a9-128">WMI does not implement this class.</span></span>

<span data-ttu-id="4b4a9-129">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="4b4a9-129">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="4b4a9-130">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="4b4a9-130">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b4a9-131">Требования</span><span class="sxs-lookup"><span data-stu-id="4b4a9-131">Requirements</span></span>



| <span data-ttu-id="4b4a9-132">Требование</span><span class="sxs-lookup"><span data-stu-id="4b4a9-132">Requirement</span></span> | <span data-ttu-id="4b4a9-133">Значение</span><span class="sxs-lookup"><span data-stu-id="4b4a9-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4b4a9-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4b4a9-134">Minimum supported client</span></span><br/> | <span data-ttu-id="4b4a9-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4b4a9-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4b4a9-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4b4a9-136">Minimum supported server</span></span><br/> | <span data-ttu-id="4b4a9-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4b4a9-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4b4a9-138">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="4b4a9-138">Namespace</span></span><br/>                | <span data-ttu-id="4b4a9-139">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="4b4a9-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4b4a9-140">MOF</span><span class="sxs-lookup"><span data-stu-id="4b4a9-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4b4a9-141"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4b4a9-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4b4a9-142">DLL</span><span class="sxs-lookup"><span data-stu-id="4b4a9-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4b4a9-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4b4a9-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b4a9-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4b4a9-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b4a9-145">**\_Зависимость CIM**</span><span class="sxs-lookup"><span data-stu-id="4b4a9-145">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

