---
description: '\_Класс СОПОСТАВЛЕНИЯ CIM инсталледос представляет связь между компьютерной системой и установленной операционной системой.'
ms.assetid: 6db5b5a2-91b6-4540-83b8-bb9c86c7f94e
ms.tgt_platform: multiple
title: Класс CIM_InstalledOS
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_InstalledOS
- CIM_InstalledOS.PartComponent
- CIM_InstalledOS.GroupComponent
- CIM_InstalledOS.PrimaryOS
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 53e01be6a87fa6e5ef91ad6e8a81dbbddff4a576
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538975"
---
# <a name="cim_installedos-class"></a><span data-ttu-id="4cf08-103">\_Класс CIM инсталледос</span><span class="sxs-lookup"><span data-stu-id="4cf08-103">CIM\_InstalledOS class</span></span>

<span data-ttu-id="4cf08-104">Класс сопоставления **CIM \_ инсталледос** представляет связь между компьютерной системой и установленной операционной системой.</span><span class="sxs-lookup"><span data-stu-id="4cf08-104">The **CIM\_InstalledOS** association class represents a link between the computer system and the installed operating system.</span></span> <span data-ttu-id="4cf08-105">Операционная система устанавливается, когда она находится в системе хранения данных компьютера (например, копируется на диск или загружается в память).</span><span class="sxs-lookup"><span data-stu-id="4cf08-105">An operating system is installed when it is in a computer system's storage extent (for example, copied to a disk drive or downloaded to memory).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4cf08-106">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="4cf08-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="4cf08-107">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="4cf08-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="4cf08-108">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="4cf08-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="4cf08-109">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="4cf08-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="4cf08-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4cf08-110">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C575-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_InstalledOS : CIM_SystemComponent
{
  CIM_OperatingSystem REF PartComponent;
  CIM_ComputerSystem  REF GroupComponent;
  boolean                 PrimaryOS;
};
```

## <a name="members"></a><span data-ttu-id="4cf08-111">Члены</span><span class="sxs-lookup"><span data-stu-id="4cf08-111">Members</span></span>

<span data-ttu-id="4cf08-112">Класс **CIM \_ инсталледос** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="4cf08-112">The **CIM\_InstalledOS** class has these types of members:</span></span>

-   [<span data-ttu-id="4cf08-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="4cf08-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4cf08-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="4cf08-114">Properties</span></span>

<span data-ttu-id="4cf08-115">Класс **CIM \_ инсталледос** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="4cf08-115">The **CIM\_InstalledOS** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4cf08-116">**Ссылка**</span><span class="sxs-lookup"><span data-stu-id="4cf08-116">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4cf08-117">Тип данных: **CIM \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="4cf08-117">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="4cf08-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4cf08-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4cf08-119">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="4cf08-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="4cf08-120">[**CIM- \_**](cim-computersystem.md) объект, описывающий компьютерную систему.</span><span class="sxs-lookup"><span data-stu-id="4cf08-120">A [**CIM\_ComputerSystem**](cim-computersystem.md) describing the computer system.</span></span>

</dd> <dt>

<span data-ttu-id="4cf08-121">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="4cf08-121">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4cf08-122">Тип данных: **\_ Операционная система CIM**</span><span class="sxs-lookup"><span data-stu-id="4cf08-122">Data type: **CIM\_OperatingSystem**</span></span>
</dt> <dt>

<span data-ttu-id="4cf08-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4cf08-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4cf08-124">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**слабый**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="4cf08-124">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="4cf08-125">Операционная система CIM, описывающая операционную систему, установленную в компьютерной системе. [**\_**](cim-operatingsystem.md)</span><span class="sxs-lookup"><span data-stu-id="4cf08-125">A [**CIM\_OperatingSystem**](cim-operatingsystem.md) that describes the operating system installed on the computer system.</span></span>

</dd> <dt>

<span data-ttu-id="4cf08-126">**примарйос**</span><span class="sxs-lookup"><span data-stu-id="4cf08-126">**PrimaryOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4cf08-127">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="4cf08-127">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4cf08-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4cf08-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4cf08-129">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Операционная система DMTF \| 001,4 ")</span><span class="sxs-lookup"><span data-stu-id="4cf08-129">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operating System\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="4cf08-130">Если **значение равно true**, то установленная операционная система является операционной системой по умолчанию для компьютерной системы.</span><span class="sxs-lookup"><span data-stu-id="4cf08-130">If **TRUE**, the installed operating system is the default operating system for the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4cf08-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4cf08-131">Remarks</span></span>

<span data-ttu-id="4cf08-132">Класс **CIM \_ инсталледос** является производным от [**CIM \_ системкомпонент**](cim-systemcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="4cf08-132">The **CIM\_InstalledOS** class is derived from [**CIM\_SystemComponent**](cim-systemcomponent.md).</span></span>

<span data-ttu-id="4cf08-133">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="4cf08-133">WMI does not implement this class.</span></span> <span data-ttu-id="4cf08-134">Классы, производные от **CIM \_ инсталледос**, см. в разделе [Классы Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="4cf08-134">For classes derived from **CIM\_InstalledOS**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="4cf08-135">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="4cf08-135">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="4cf08-136">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="4cf08-136">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="4cf08-137">Требования</span><span class="sxs-lookup"><span data-stu-id="4cf08-137">Requirements</span></span>



| <span data-ttu-id="4cf08-138">Требование</span><span class="sxs-lookup"><span data-stu-id="4cf08-138">Requirement</span></span> | <span data-ttu-id="4cf08-139">Значение</span><span class="sxs-lookup"><span data-stu-id="4cf08-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4cf08-140">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4cf08-140">Minimum supported client</span></span><br/> | <span data-ttu-id="4cf08-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4cf08-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4cf08-142">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4cf08-142">Minimum supported server</span></span><br/> | <span data-ttu-id="4cf08-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4cf08-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4cf08-144">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="4cf08-144">Namespace</span></span><br/>                | <span data-ttu-id="4cf08-145">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="4cf08-145">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4cf08-146">MOF</span><span class="sxs-lookup"><span data-stu-id="4cf08-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4cf08-147"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4cf08-147"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4cf08-148">DLL</span><span class="sxs-lookup"><span data-stu-id="4cf08-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4cf08-149"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4cf08-149"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4cf08-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4cf08-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cf08-151">**\_СИСТЕМКОМПОНЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="4cf08-151">**CIM\_SystemComponent**</span></span>](cim-systemcomponent.md)
</dt> </dl>

 

