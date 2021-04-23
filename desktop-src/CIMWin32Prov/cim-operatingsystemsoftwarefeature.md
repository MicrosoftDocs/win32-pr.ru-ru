---
description: Класс CIM \_ оператингсистемсофтварефеатуре представляет программные функции, составляющие операционную систему.
ms.assetid: 9ffc709c-213e-4252-9662-76f01e1685e5
ms.tgt_platform: multiple
title: Класс CIM_OperatingSystemSoftwareFeature
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_OperatingSystemSoftwareFeature
- CIM_OperatingSystemSoftwareFeature.PartComponent
- CIM_OperatingSystemSoftwareFeature.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b9d74478f211b23e103854cedb09a1e0186618b8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655941"
---
# <a name="cim_operatingsystemsoftwarefeature-class"></a><span data-ttu-id="4324d-103">\_Класс CIM оператингсистемсофтварефеатуре</span><span class="sxs-lookup"><span data-stu-id="4324d-103">CIM\_OperatingSystemSoftwareFeature class</span></span>

<span data-ttu-id="4324d-104">Класс **CIM \_ оператингсистемсофтварефеатуре** представляет программные функции, составляющие операционную систему.</span><span class="sxs-lookup"><span data-stu-id="4324d-104">The **CIM\_OperatingSystemSoftwareFeature** class represents the software features that make up the operating system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4324d-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="4324d-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="4324d-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="4324d-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="4324d-107">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="4324d-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="4324d-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="4324d-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="4324d-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4324d-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{96B4C734-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_OperatingSystemSoftwareFeature : CIM_Component
{
  CIM_SoftwareFeature REF PartComponent;
  CIM_OperatingSystem REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="4324d-110">Члены</span><span class="sxs-lookup"><span data-stu-id="4324d-110">Members</span></span>

<span data-ttu-id="4324d-111">Класс **CIM \_ оператингсистемсофтварефеатуре** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="4324d-111">The **CIM\_OperatingSystemSoftwareFeature** class has these types of members:</span></span>

-   [<span data-ttu-id="4324d-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="4324d-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4324d-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="4324d-113">Properties</span></span>

<span data-ttu-id="4324d-114">Класс **CIM \_ оператингсистемсофтварефеатуре** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="4324d-114">The **CIM\_OperatingSystemSoftwareFeature** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4324d-115">**Ссылка**</span><span class="sxs-lookup"><span data-stu-id="4324d-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4324d-116">Тип данных: **\_ Операционная система CIM**</span><span class="sxs-lookup"><span data-stu-id="4324d-116">Data type: **CIM\_OperatingSystem**</span></span>
</dt> <dt>

<span data-ttu-id="4324d-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4324d-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4324d-118">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="4324d-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="4324d-119">Система [**CIM \_**](cim-operatingsystem.md) , описывающая операционную систему.</span><span class="sxs-lookup"><span data-stu-id="4324d-119">A [**CIM\_OperatingSystem**](cim-operatingsystem.md) describing the operating system.</span></span>

</dd> <dt>

<span data-ttu-id="4324d-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="4324d-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4324d-121">Тип данных: **CIM \_ софтварефеатуре**</span><span class="sxs-lookup"><span data-stu-id="4324d-121">Data type: **CIM\_SoftwareFeature**</span></span>
</dt> <dt>

<span data-ttu-id="4324d-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4324d-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4324d-123">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="4324d-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="4324d-124">[**\_ Софтварефеатуре CIM**](cim-softwarefeature.md) , описывающий функции программного обеспечения, составляющие операционную систему.</span><span class="sxs-lookup"><span data-stu-id="4324d-124">A [**CIM\_SoftwareFeature**](cim-softwarefeature.md) describing the software features that make up the operating system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4324d-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4324d-125">Remarks</span></span>

<span data-ttu-id="4324d-126">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="4324d-126">WMI does not implement this class.</span></span>

<span data-ttu-id="4324d-127">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="4324d-127">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="4324d-128">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="4324d-128">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="4324d-129">Требования</span><span class="sxs-lookup"><span data-stu-id="4324d-129">Requirements</span></span>



| <span data-ttu-id="4324d-130">Требование</span><span class="sxs-lookup"><span data-stu-id="4324d-130">Requirement</span></span> | <span data-ttu-id="4324d-131">Значение</span><span class="sxs-lookup"><span data-stu-id="4324d-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4324d-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4324d-132">Minimum supported client</span></span><br/> | <span data-ttu-id="4324d-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4324d-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4324d-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4324d-134">Minimum supported server</span></span><br/> | <span data-ttu-id="4324d-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4324d-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4324d-136">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="4324d-136">Namespace</span></span><br/>                | <span data-ttu-id="4324d-137">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="4324d-137">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4324d-138">MOF</span><span class="sxs-lookup"><span data-stu-id="4324d-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4324d-139"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4324d-139"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4324d-140">DLL</span><span class="sxs-lookup"><span data-stu-id="4324d-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4324d-141"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4324d-141"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4324d-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4324d-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4324d-143">**\_Компонент CIM**</span><span class="sxs-lookup"><span data-stu-id="4324d-143">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 

