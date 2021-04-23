---
description: '\_Класс WMI взаимосвязей Win32 системоператингсистем связывает компьютерную систему и ее операционную систему.'
ms.assetid: dc71f80b-6fbd-4bc8-8783-3922d8050518
ms.tgt_platform: multiple
title: Класс Win32_SystemOperatingSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemOperatingSystem
- Win32_SystemOperatingSystem.PrimaryOS
- Win32_SystemOperatingSystem.GroupComponent
- Win32_SystemOperatingSystem.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ba3f8ac94ec882ee1df96da51d93d2c24fde9b3f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142691"
---
# <a name="win32_systemoperatingsystem-class"></a><span data-ttu-id="73208-103">\_Класс Win32 системоператингсистем</span><span class="sxs-lookup"><span data-stu-id="73208-103">Win32\_SystemOperatingSystem class</span></span>

<span data-ttu-id="73208-104">[Класс WMI](../wmisdk/retrieving-a-class.md) взаимосвязей **Win32 \_ системоператингсистем** связывает компьютерную систему и ее операционную систему.</span><span class="sxs-lookup"><span data-stu-id="73208-104">The **Win32\_SystemOperatingSystem** association [WMI class](../wmisdk/retrieving-a-class.md) relates a computer system and its operating system.</span></span>

<span data-ttu-id="73208-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="73208-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="73208-106">Свойства и методы имеют алфавитный порядок, а не порядок MOF.</span><span class="sxs-lookup"><span data-stu-id="73208-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="73208-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="73208-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4F0-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemOperatingSystem : CIM_InstalledOS
{
  boolean                   PrimaryOS;
  Win32_ComputerSystem  REF GroupComponent;
  Win32_OperatingSystem REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="73208-108">Члены</span><span class="sxs-lookup"><span data-stu-id="73208-108">Members</span></span>

<span data-ttu-id="73208-109">Класс **Win32 \_ системоператингсистем** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="73208-109">The **Win32\_SystemOperatingSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="73208-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="73208-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="73208-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="73208-111">Properties</span></span>

<span data-ttu-id="73208-112">Класс **Win32 \_ системоператингсистем** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="73208-112">The **Win32\_SystemOperatingSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="73208-113">**Ссылка**</span><span class="sxs-lookup"><span data-stu-id="73208-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73208-114">Тип данных: **Win32 \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="73208-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="73208-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="73208-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="73208-116">Квалификаторы: [**ключ**](../wmisdk/key-qualifier.md), [**Переопределение**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ ComputerSystem")</span><span class="sxs-lookup"><span data-stu-id="73208-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="73208-117">[**Платформа Win32 \_ ComputerSystem**](win32-computersystemprocessor.md) , описывающая свойства компьютерной системы, на которой установлена операционная система.</span><span class="sxs-lookup"><span data-stu-id="73208-117">A [**Win32\_ComputerSystem**](win32-computersystemprocessor.md) that describes the properties of the computer system upon which the operating system is installed.</span></span>

</dd> <dt>

<span data-ttu-id="73208-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="73208-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73208-119">Тип данных: **Win32 с \_ операционной** системы</span><span class="sxs-lookup"><span data-stu-id="73208-119">Data type: **Win32\_OperatingSystem**</span></span>
</dt> <dt>

<span data-ttu-id="73208-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="73208-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="73208-121">Квалификаторы: [**ключ**](../wmisdk/key-qualifier.md), [**Переопределение**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Инструментарий WMI \| Win32 \_ ")</span><span class="sxs-lookup"><span data-stu-id="73208-121">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_OperatingSystem")</span></span>
</dt> </dl>

<span data-ttu-id="73208-122">Операционная [**система \_ Win32**](win32-operatingsystem.md) с описанием свойств операционной системы, работающей на данной компьютерной системе.</span><span class="sxs-lookup"><span data-stu-id="73208-122">A [**Win32\_OperatingSystem**](win32-operatingsystem.md) that describes properties of the operating system running on this computer system.</span></span>

</dd> <dt>

<span data-ttu-id="73208-123">**примарйос**</span><span class="sxs-lookup"><span data-stu-id="73208-123">**PrimaryOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73208-124">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="73208-124">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="73208-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="73208-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="73208-126">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. \|Операционная система DMTF \| 001,4 ")</span><span class="sxs-lookup"><span data-stu-id="73208-126">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operating System\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="73208-127">Если **значение равно true**, то установленная операционная система является операционной системой по умолчанию для компьютерной системы.</span><span class="sxs-lookup"><span data-stu-id="73208-127">If **TRUE**, the installed operating system is the default operating system for the computer system.</span></span>

<span data-ttu-id="73208-128">Это свойство наследуется от [**CIM \_ инсталледос**](cim-installedos.md).</span><span class="sxs-lookup"><span data-stu-id="73208-128">This property is inherited from [**CIM\_InstalledOS**](cim-installedos.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="73208-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="73208-129">Remarks</span></span>

<span data-ttu-id="73208-130">Класс **Win32 \_ системоператингсистем** является производным от [**CIM \_ инсталледос**](cim-installedos.md).</span><span class="sxs-lookup"><span data-stu-id="73208-130">The **Win32\_SystemOperatingSystem** class is derived from [**CIM\_InstalledOS**](cim-installedos.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="73208-131">Требования</span><span class="sxs-lookup"><span data-stu-id="73208-131">Requirements</span></span>



| <span data-ttu-id="73208-132">Требование</span><span class="sxs-lookup"><span data-stu-id="73208-132">Requirement</span></span> | <span data-ttu-id="73208-133">Значение</span><span class="sxs-lookup"><span data-stu-id="73208-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="73208-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="73208-134">Minimum supported client</span></span><br/> | <span data-ttu-id="73208-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="73208-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="73208-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="73208-136">Minimum supported server</span></span><br/> | <span data-ttu-id="73208-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="73208-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="73208-138">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="73208-138">Namespace</span></span><br/>                | <span data-ttu-id="73208-139">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="73208-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="73208-140">MOF</span><span class="sxs-lookup"><span data-stu-id="73208-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="73208-141"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="73208-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="73208-142">DLL</span><span class="sxs-lookup"><span data-stu-id="73208-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="73208-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="73208-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73208-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="73208-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73208-145">**\_ИНСТАЛЛЕДОС CIM**</span><span class="sxs-lookup"><span data-stu-id="73208-145">**CIM\_InstalledOS**</span></span>](cim-installedos.md)
</dt> <dt>

[<span data-ttu-id="73208-146">Классы операционной системы</span><span class="sxs-lookup"><span data-stu-id="73208-146">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
