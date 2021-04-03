---
description: '\_Класс WMI взаимосвязей Win32 систембиос связывает компьютерную систему (включая такие данные, как свойства запуска, часовые пояса, конфигурации загрузки или административные пароли) и системную BIOS (службы, языки и свойства управления системой).'
ms.assetid: 92747b1b-ef28-40ab-868a-6755aee8c723
ms.tgt_platform: multiple
title: Класс Win32_SystemBIOS
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemBIOS
- Win32_SystemBIOS.PartComponent
- Win32_SystemBIOS.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: bc8ec1f3526e2faefe0e63c9dea357accd025c13
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896342"
---
# <a name="win32_systembios-class"></a><span data-ttu-id="4f67b-103">\_Класс Win32 систембиос</span><span class="sxs-lookup"><span data-stu-id="4f67b-103">Win32\_SystemBIOS class</span></span>

<span data-ttu-id="4f67b-104">[Класс WMI](../wmisdk/retrieving-a-class.md) взаимосвязей **Win32 \_ систембиос** связывает компьютерную систему (включая такие данные, как свойства запуска, часовые пояса, конфигурации загрузки или административные пароли) и системную BIOS (службы, языки и свойства управления системой).</span><span class="sxs-lookup"><span data-stu-id="4f67b-104">The **Win32\_SystemBIOS** association [WMI class](../wmisdk/retrieving-a-class.md) relates a computer system (including data such as startup properties, time zones, boot configurations, or administrative passwords), and a system BIOS (services, languages, and system management properties).</span></span>

<span data-ttu-id="4f67b-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="4f67b-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="4f67b-106">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="4f67b-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f67b-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4f67b-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4EE-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemBIOS : CIM_SystemComponent
{
  Win32_BIOS           REF PartComponent;
  Win32_ComputerSystem REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="4f67b-108">Члены</span><span class="sxs-lookup"><span data-stu-id="4f67b-108">Members</span></span>

<span data-ttu-id="4f67b-109">Класс **Win32 \_ систембиос** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="4f67b-109">The **Win32\_SystemBIOS** class has these types of members:</span></span>

-   [<span data-ttu-id="4f67b-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="4f67b-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4f67b-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="4f67b-111">Properties</span></span>

<span data-ttu-id="4f67b-112">Класс **Win32 \_ систембиос** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="4f67b-112">The **Win32\_SystemBIOS** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4f67b-113">**Ссылка**</span><span class="sxs-lookup"><span data-stu-id="4f67b-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f67b-114">Тип данных: **Win32 \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="4f67b-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="4f67b-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4f67b-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f67b-116">Квалификаторы: [**ключ**](../wmisdk/key-qualifier.md), [**Переопределение**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ ComputerSystem")</span><span class="sxs-lookup"><span data-stu-id="4f67b-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="4f67b-117">[**Платформа Win32 \_ ComputerSystem**](win32-computersystemprocessor.md) , содержащая BIOS ассоциации.</span><span class="sxs-lookup"><span data-stu-id="4f67b-117">The [**Win32\_ComputerSystem**](win32-computersystemprocessor.md) containing the BIOS of the association.</span></span>

</dd> <dt>

<span data-ttu-id="4f67b-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="4f67b-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f67b-119">Тип данных: **Win32 \_ BIOS**</span><span class="sxs-lookup"><span data-stu-id="4f67b-119">Data type: **Win32\_BIOS**</span></span>
</dt> <dt>

<span data-ttu-id="4f67b-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4f67b-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f67b-121">Квалификаторы: [**ключ**](../wmisdk/key-qualifier.md), [**Переопределение**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ BIOS")</span><span class="sxs-lookup"><span data-stu-id="4f67b-121">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_BIOS")</span></span>
</dt> </dl>

<span data-ttu-id="4f67b-122">[**Win32 \_ BIOS**](win32-bios.md) , содержащийся в компьютерной системе этой ассоциации.</span><span class="sxs-lookup"><span data-stu-id="4f67b-122">A [**Win32\_BIOS**](win32-bios.md) contained in the computer system of this association.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4f67b-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4f67b-123">Remarks</span></span>

<span data-ttu-id="4f67b-124">Класс **Win32 \_ систембиос** является производным от [**CIM \_ системкомпонент**](cim-systemcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="4f67b-124">The **Win32\_SystemBIOS** class is derived from [**CIM\_SystemComponent**](cim-systemcomponent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4f67b-125">Требования</span><span class="sxs-lookup"><span data-stu-id="4f67b-125">Requirements</span></span>



| <span data-ttu-id="4f67b-126">Требование</span><span class="sxs-lookup"><span data-stu-id="4f67b-126">Requirement</span></span> | <span data-ttu-id="4f67b-127">Значение</span><span class="sxs-lookup"><span data-stu-id="4f67b-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4f67b-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4f67b-128">Minimum supported client</span></span><br/> | <span data-ttu-id="4f67b-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4f67b-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4f67b-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4f67b-130">Minimum supported server</span></span><br/> | <span data-ttu-id="4f67b-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4f67b-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4f67b-132">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="4f67b-132">Namespace</span></span><br/>                | <span data-ttu-id="4f67b-133">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="4f67b-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4f67b-134">MOF</span><span class="sxs-lookup"><span data-stu-id="4f67b-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4f67b-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4f67b-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4f67b-136">DLL</span><span class="sxs-lookup"><span data-stu-id="4f67b-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4f67b-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4f67b-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f67b-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4f67b-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f67b-139">**\_СИСТЕМКОМПОНЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="4f67b-139">**CIM\_SystemComponent**</span></span>](cim-systemcomponent.md)
</dt> <dt>

[<span data-ttu-id="4f67b-140">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="4f67b-140">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
