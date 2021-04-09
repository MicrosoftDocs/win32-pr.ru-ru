---
description: '\_Класс WMI взаимосвязей Win32 системпроцессес связывает компьютерную систему и процесс, выполняющийся в этой системе.'
ms.assetid: 0d8c3ec6-265e-4486-8e94-f5acd2845cf5
ms.tgt_platform: multiple
title: Класс Win32_SystemProcesses
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemProcesses
- Win32_SystemProcesses.GroupComponent
- Win32_SystemProcesses.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1b963aea5d9c651e27dc4380200e40dd3dcb9a77
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072455"
---
# <a name="win32_systemprocesses-class"></a><span data-ttu-id="9afd7-103">\_Класс Win32 системпроцессес</span><span class="sxs-lookup"><span data-stu-id="9afd7-103">Win32\_SystemProcesses class</span></span>

<span data-ttu-id="9afd7-104">[Класс WMI](../wmisdk/retrieving-a-class.md) взаимосвязей **Win32 \_ системпроцессес** связывает компьютерную систему и процесс, выполняющийся в этой системе.</span><span class="sxs-lookup"><span data-stu-id="9afd7-104">The **Win32\_SystemProcesses** association [WMI class](../wmisdk/retrieving-a-class.md) relates a computer system and a process running on that system.</span></span>

<span data-ttu-id="9afd7-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="9afd7-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="9afd7-106">Свойства и методы имеют алфавитный порядок, а не порядок MOF.</span><span class="sxs-lookup"><span data-stu-id="9afd7-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="9afd7-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9afd7-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4F3-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemProcesses : CIM_SystemComponent
{
  Win32_ComputerSystem REF GroupComponent;
  Win32_Process        REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="9afd7-108">Члены</span><span class="sxs-lookup"><span data-stu-id="9afd7-108">Members</span></span>

<span data-ttu-id="9afd7-109">Класс **Win32 \_ системпроцессес** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="9afd7-109">The **Win32\_SystemProcesses** class has these types of members:</span></span>

-   [<span data-ttu-id="9afd7-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="9afd7-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9afd7-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="9afd7-111">Properties</span></span>

<span data-ttu-id="9afd7-112">Класс **Win32 \_ системпроцессес** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="9afd7-112">The **Win32\_SystemProcesses** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9afd7-113">**Ссылка**</span><span class="sxs-lookup"><span data-stu-id="9afd7-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9afd7-114">Тип данных: **Win32 \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="9afd7-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="9afd7-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9afd7-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9afd7-116">Квалификаторы: [**ключ**](../wmisdk/key-qualifier.md), [**Переопределение**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ ComputerSystem")</span><span class="sxs-lookup"><span data-stu-id="9afd7-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="9afd7-117">Ссылка на экземпляр, представляющий компьютерную систему, на которой выполняется процесс.</span><span class="sxs-lookup"><span data-stu-id="9afd7-117">Reference to the instance representing the computer system upon which the process is running.</span></span>

</dd> <dt>

<span data-ttu-id="9afd7-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="9afd7-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9afd7-119">Тип данных: **\_ процесс Win32**</span><span class="sxs-lookup"><span data-stu-id="9afd7-119">Data type: **Win32\_Process**</span></span>
</dt> <dt>

<span data-ttu-id="9afd7-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9afd7-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9afd7-121">Квалификаторы: [**ключ**](../wmisdk/key-qualifier.md), [**Переопределение**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ Process")</span><span class="sxs-lookup"><span data-stu-id="9afd7-121">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_Process")</span></span>
</dt> </dl>

<span data-ttu-id="9afd7-122">Ссылка на экземпляр, представляющий процесс, выполняемый в компьютерной системе.</span><span class="sxs-lookup"><span data-stu-id="9afd7-122">Reference to the instance representing the process running on the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9afd7-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9afd7-123">Remarks</span></span>

<span data-ttu-id="9afd7-124">Класс **Win32 \_ системпроцессес** является производным от [**CIM \_ системкомпонент**](cim-systemcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="9afd7-124">The **Win32\_SystemProcesses** class is derived from [**CIM\_SystemComponent**](cim-systemcomponent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9afd7-125">Требования</span><span class="sxs-lookup"><span data-stu-id="9afd7-125">Requirements</span></span>



| <span data-ttu-id="9afd7-126">Требование</span><span class="sxs-lookup"><span data-stu-id="9afd7-126">Requirement</span></span> | <span data-ttu-id="9afd7-127">Значение</span><span class="sxs-lookup"><span data-stu-id="9afd7-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9afd7-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9afd7-128">Minimum supported client</span></span><br/> | <span data-ttu-id="9afd7-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9afd7-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9afd7-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9afd7-130">Minimum supported server</span></span><br/> | <span data-ttu-id="9afd7-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9afd7-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9afd7-132">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="9afd7-132">Namespace</span></span><br/>                | <span data-ttu-id="9afd7-133">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="9afd7-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9afd7-134">MOF</span><span class="sxs-lookup"><span data-stu-id="9afd7-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9afd7-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9afd7-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9afd7-136">DLL</span><span class="sxs-lookup"><span data-stu-id="9afd7-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9afd7-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9afd7-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9afd7-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9afd7-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9afd7-139">**\_СИСТЕМКОМПОНЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="9afd7-139">**CIM\_SystemComponent**</span></span>](cim-systemcomponent.md)
</dt> <dt>

[<span data-ttu-id="9afd7-140">Классы операционной системы</span><span class="sxs-lookup"><span data-stu-id="9afd7-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
