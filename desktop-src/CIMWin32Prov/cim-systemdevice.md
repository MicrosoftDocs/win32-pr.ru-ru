---
description: Ассоциация CIM \_ системдевице представляет собой явную связь, в которой логические устройства могут быть агрегированы системой.
ms.assetid: df624a9f-0c10-44a3-8075-908e5e481e3c
ms.tgt_platform: multiple
title: Класс CIM_SystemDevice (поставщики WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SystemDevice
- CIM_SystemDevice.PartComponent
- CIM_SystemDevice.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: dbff9a0ead8790de9ab323509c8b2f1392e6ed6e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655937"
---
# <a name="cim_systemdevice-class-cimwin32-wmi-providers"></a><span data-ttu-id="82422-103">Класс CIM_SystemDevice (поставщики WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="82422-103">CIM_SystemDevice class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="82422-104">Ассоциация **CIM \_ системдевице** представляет собой явную связь, в которой логические устройства могут быть агрегированы системой.</span><span class="sxs-lookup"><span data-stu-id="82422-104">The **CIM\_SystemDevice** association represents an explicit relationship in which logical devices can be aggregated by a system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="82422-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="82422-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="82422-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="82422-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="82422-107">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="82422-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="82422-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="82422-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="82422-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="82422-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{4B2C30D7-BAFE-11d2-85E5-0000F8102E5F}"), AMENDMENT]
class CIM_SystemDevice : CIM_SystemComponent
{
  CIM_LogicalDevice REF PartComponent;
  CIM_System        REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="82422-110">Члены</span><span class="sxs-lookup"><span data-stu-id="82422-110">Members</span></span>

<span data-ttu-id="82422-111">Класс **CIM \_ системдевице** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="82422-111">The **CIM\_SystemDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="82422-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="82422-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="82422-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="82422-113">Properties</span></span>

<span data-ttu-id="82422-114">Класс **CIM \_ системдевице** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="82422-114">The **CIM\_SystemDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="82422-115">**Ссылка**</span><span class="sxs-lookup"><span data-stu-id="82422-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82422-116">Тип данных: **\_ система CIM**</span><span class="sxs-lookup"><span data-stu-id="82422-116">Data type: **CIM\_System**</span></span>
</dt> <dt>

<span data-ttu-id="82422-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="82422-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="82422-118">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="82422-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="82422-119">[**\_ Система CIM**](cim-system.md) , которая описывает родительскую систему в ассоциации.</span><span class="sxs-lookup"><span data-stu-id="82422-119">A [**CIM\_System**](cim-system.md) that describes the parent system in the association.</span></span>

</dd> <dt>

<span data-ttu-id="82422-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="82422-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82422-121">Тип данных: **CIM \_** с типом "модель"</span><span class="sxs-lookup"><span data-stu-id="82422-121">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="82422-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="82422-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="82422-123">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**слабый**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="82422-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="82422-124">[**Модель CIM \_**](cim-logicaldevice.md) , описывающая логическое устройство, которое является компонентом системы.</span><span class="sxs-lookup"><span data-stu-id="82422-124">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that describes the logical device that is a component of a system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="82422-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="82422-125">Remarks</span></span>

<span data-ttu-id="82422-126">Класс **CIM \_ системдевице** является производным от [**CIM \_ системкомпонент**](cim-systemcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="82422-126">The **CIM\_SystemDevice** class is derived from [**CIM\_SystemComponent**](cim-systemcomponent.md).</span></span>

<span data-ttu-id="82422-127">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="82422-127">WMI does not implement this class.</span></span> <span data-ttu-id="82422-128">Классы WMI, производные от **CIM \_ системдевице**, см. в разделе [Классы Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="82422-128">For WMI classes derived from **CIM\_SystemDevice**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="82422-129">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="82422-129">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="82422-130">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="82422-130">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="82422-131">Требования</span><span class="sxs-lookup"><span data-stu-id="82422-131">Requirements</span></span>



| <span data-ttu-id="82422-132">Требование</span><span class="sxs-lookup"><span data-stu-id="82422-132">Requirement</span></span> | <span data-ttu-id="82422-133">Значение</span><span class="sxs-lookup"><span data-stu-id="82422-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="82422-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="82422-134">Minimum supported client</span></span><br/> | <span data-ttu-id="82422-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="82422-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="82422-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="82422-136">Minimum supported server</span></span><br/> | <span data-ttu-id="82422-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="82422-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="82422-138">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="82422-138">Namespace</span></span><br/>                | <span data-ttu-id="82422-139">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="82422-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="82422-140">MOF</span><span class="sxs-lookup"><span data-stu-id="82422-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="82422-141"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="82422-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="82422-142">DLL</span><span class="sxs-lookup"><span data-stu-id="82422-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="82422-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="82422-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82422-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="82422-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82422-145">**\_СИСТЕМКОМПОНЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="82422-145">**CIM\_SystemComponent**</span></span>](cim-systemcomponent.md)
</dt> </dl>

 

