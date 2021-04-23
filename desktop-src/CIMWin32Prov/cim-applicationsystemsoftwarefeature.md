---
description: Класс CIM \_ аппликатионсистемсофтварефеатуре представляет ассоциацию, которая определяет программные компоненты, составляющие конкретную систему приложений. Функции программного обеспечения могут включаться в различные продукты.
ms.assetid: e40d0d64-f9f0-4c05-aef6-c759256e408b
ms.tgt_platform: multiple
title: Класс CIM_ApplicationSystemSoftwareFeature
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ApplicationSystemSoftwareFeature
- CIM_ApplicationSystemSoftwareFeature.PartComponent
- CIM_ApplicationSystemSoftwareFeature.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6b13a15370b19583eef61fb36fda2d63fcb61989
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896193"
---
# <a name="cim_applicationsystemsoftwarefeature-class"></a><span data-ttu-id="be55e-104">\_Класс CIM аппликатионсистемсофтварефеатуре</span><span class="sxs-lookup"><span data-stu-id="be55e-104">CIM\_ApplicationSystemSoftwareFeature class</span></span>

<span data-ttu-id="be55e-105">Класс **CIM \_ аппликатионсистемсофтварефеатуре** представляет ассоциацию, которая определяет программные компоненты, составляющие конкретную систему приложений.</span><span class="sxs-lookup"><span data-stu-id="be55e-105">The **CIM\_ApplicationSystemSoftwareFeature** class represents an association that identifies the software features that make up a particular application system.</span></span> <span data-ttu-id="be55e-106">Функции программного обеспечения могут включаться в различные продукты.</span><span class="sxs-lookup"><span data-stu-id="be55e-106">The software features can be included in different products.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="be55e-107">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="be55e-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="be55e-108">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="be55e-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="be55e-109">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="be55e-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="be55e-110">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="be55e-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="be55e-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="be55e-111">Syntax</span></span>

``` syntax
[UUID("{0E17B9EA-E3D3-11d2-8601-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_ApplicationSystemSoftwareFeature : CIM_SystemComponent
{
  CIM_SoftwareFeature   REF PartComponent;
  CIM_ApplicationSystem REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="be55e-112">Члены</span><span class="sxs-lookup"><span data-stu-id="be55e-112">Members</span></span>

<span data-ttu-id="be55e-113">Класс **CIM \_ аппликатионсистемсофтварефеатуре** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="be55e-113">The **CIM\_ApplicationSystemSoftwareFeature** class has these types of members:</span></span>

-   [<span data-ttu-id="be55e-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="be55e-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="be55e-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="be55e-115">Properties</span></span>

<span data-ttu-id="be55e-116">Класс **CIM \_ аппликатионсистемсофтварефеатуре** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="be55e-116">The **CIM\_ApplicationSystemSoftwareFeature** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="be55e-117">**Ссылка**</span><span class="sxs-lookup"><span data-stu-id="be55e-117">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be55e-118">Тип данных: **CIM \_ аппликатионсистем**</span><span class="sxs-lookup"><span data-stu-id="be55e-118">Data type: **CIM\_ApplicationSystem**</span></span>
</dt> <dt>

<span data-ttu-id="be55e-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="be55e-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="be55e-120">Квалификаторы: [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="be55e-120">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="be55e-121">[**\_ Аппликатионсистем CIM**](cim-applicationsystem.md) , которая содержит родительскую систему в ассоциации.</span><span class="sxs-lookup"><span data-stu-id="be55e-121">A [**CIM\_ApplicationSystem**](cim-applicationsystem.md) that contains the parent system in the association.</span></span>

</dd> <dt>

<span data-ttu-id="be55e-122">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="be55e-122">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be55e-123">Тип данных: **CIM \_ софтварефеатуре**</span><span class="sxs-lookup"><span data-stu-id="be55e-123">Data type: **CIM\_SoftwareFeature**</span></span>
</dt> <dt>

<span data-ttu-id="be55e-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="be55e-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="be55e-125">Квалификаторы: [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="be55e-125">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="be55e-126">[**\_ Софтварефеатуре CIM**](cim-softwarefeature.md) , содержащий дочерний элемент, являющийся компонентом системы.</span><span class="sxs-lookup"><span data-stu-id="be55e-126">A [**CIM\_SoftwareFeature**](cim-softwarefeature.md) that contain the child element that is a component of a system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="be55e-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="be55e-127">Remarks</span></span>

<span data-ttu-id="be55e-128">Класс **CIM \_ аппликатионсистемсофтварефеатуре** является производным от [**CIM \_ системкомпонент**](cim-systemcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="be55e-128">The **CIM\_ApplicationSystemSoftwareFeature** class is derived from [**CIM\_SystemComponent**](cim-systemcomponent.md).</span></span>

<span data-ttu-id="be55e-129">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="be55e-129">WMI does not implement this class.</span></span>

<span data-ttu-id="be55e-130">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="be55e-130">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="be55e-131">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="be55e-131">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="be55e-132">Требования</span><span class="sxs-lookup"><span data-stu-id="be55e-132">Requirements</span></span>



| <span data-ttu-id="be55e-133">Требование</span><span class="sxs-lookup"><span data-stu-id="be55e-133">Requirement</span></span> | <span data-ttu-id="be55e-134">Значение</span><span class="sxs-lookup"><span data-stu-id="be55e-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="be55e-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="be55e-135">Minimum supported client</span></span><br/> | <span data-ttu-id="be55e-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="be55e-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="be55e-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="be55e-137">Minimum supported server</span></span><br/> | <span data-ttu-id="be55e-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="be55e-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="be55e-139">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="be55e-139">Namespace</span></span><br/>                | <span data-ttu-id="be55e-140">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="be55e-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="be55e-141">MOF</span><span class="sxs-lookup"><span data-stu-id="be55e-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="be55e-142"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="be55e-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="be55e-143">DLL</span><span class="sxs-lookup"><span data-stu-id="be55e-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="be55e-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="be55e-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be55e-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="be55e-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be55e-146">**\_СИСТЕМКОМПОНЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="be55e-146">**CIM\_SystemComponent**</span></span>](cim-systemcomponent.md)
</dt> </dl>

 

