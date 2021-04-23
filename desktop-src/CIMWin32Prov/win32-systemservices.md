---
description: '\_Класс WMI взаимосвязей Win32 системсервицес связывает компьютерную систему и служебную программу, которая существует в системе.'
ms.assetid: b372e696-e1e0-4b1e-9fb8-83af8a75c405
ms.tgt_platform: multiple
title: Класс Win32_SystemServices
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemServices
- Win32_SystemServices.GroupComponent
- Win32_SystemServices.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d8e61469729f3753256bc7fcf5598265b5c1b7dc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807444"
---
# <a name="win32_systemservices-class"></a><span data-ttu-id="81187-103">\_Класс Win32 системсервицес</span><span class="sxs-lookup"><span data-stu-id="81187-103">Win32\_SystemServices class</span></span>

<span data-ttu-id="81187-104">[Класс WMI](../wmisdk/retrieving-a-class.md) взаимосвязей **Win32 \_ системсервицес** связывает компьютерную систему и служебную программу, которая существует в системе.</span><span class="sxs-lookup"><span data-stu-id="81187-104">The **Win32\_SystemServices** association [WMI class](../wmisdk/retrieving-a-class.md) relates a computer system and a service program that exists on the system.</span></span>

<span data-ttu-id="81187-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="81187-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="81187-106">Свойства и методы имеют алфавитный порядок, а не порядок MOF.</span><span class="sxs-lookup"><span data-stu-id="81187-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="81187-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="81187-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4F6-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemServices : CIM_SystemComponent
{
  Win32_ComputerSystem REF GroupComponent;
  Win32_Service        REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="81187-108">Члены</span><span class="sxs-lookup"><span data-stu-id="81187-108">Members</span></span>

<span data-ttu-id="81187-109">Класс **Win32 \_ системсервицес** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="81187-109">The **Win32\_SystemServices** class has these types of members:</span></span>

-   [<span data-ttu-id="81187-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="81187-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="81187-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="81187-111">Properties</span></span>

<span data-ttu-id="81187-112">Класс **Win32 \_ системсервицес** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="81187-112">The **Win32\_SystemServices** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="81187-113">**Ссылка**</span><span class="sxs-lookup"><span data-stu-id="81187-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81187-114">Тип данных: **Win32 \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="81187-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="81187-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="81187-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81187-116">Квалификаторы: [**ключ**](../wmisdk/key-qualifier.md), [**Переопределение**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ ComputerSystem")</span><span class="sxs-lookup"><span data-stu-id="81187-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="81187-117">Ссылка на экземпляр, представляющий свойства компьютерной системы, в которой существует служба.</span><span class="sxs-lookup"><span data-stu-id="81187-117">Reference to the instance representing the properties of the computer system on which the service exists.</span></span>

</dd> <dt>

<span data-ttu-id="81187-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="81187-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81187-119">Тип данных: **\_ служба Win32**</span><span class="sxs-lookup"><span data-stu-id="81187-119">Data type: **Win32\_Service**</span></span>
</dt> <dt>

<span data-ttu-id="81187-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="81187-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81187-121">Квалификаторы: [**ключ**](../wmisdk/key-qualifier.md), [**Переопределение**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| Служба WMI Win32 \_ ")</span><span class="sxs-lookup"><span data-stu-id="81187-121">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_Service")</span></span>
</dt> </dl>

<span data-ttu-id="81187-122">Ссылка на экземпляр, представляющий службу, которая существует в компьютерной системе.</span><span class="sxs-lookup"><span data-stu-id="81187-122">Reference to the instance representing the service that exists on the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="81187-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="81187-123">Remarks</span></span>

<span data-ttu-id="81187-124">Класс **Win32 \_ системсервицес** является производным от [**CIM \_ системкомпонент**](cim-systemcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="81187-124">The **Win32\_SystemServices** class is derived from [**CIM\_SystemComponent**](cim-systemcomponent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="81187-125">Требования</span><span class="sxs-lookup"><span data-stu-id="81187-125">Requirements</span></span>



| <span data-ttu-id="81187-126">Требование</span><span class="sxs-lookup"><span data-stu-id="81187-126">Requirement</span></span> | <span data-ttu-id="81187-127">Значение</span><span class="sxs-lookup"><span data-stu-id="81187-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="81187-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="81187-128">Minimum supported client</span></span><br/> | <span data-ttu-id="81187-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="81187-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="81187-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="81187-130">Minimum supported server</span></span><br/> | <span data-ttu-id="81187-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="81187-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="81187-132">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="81187-132">Namespace</span></span><br/>                | <span data-ttu-id="81187-133">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="81187-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="81187-134">MOF</span><span class="sxs-lookup"><span data-stu-id="81187-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="81187-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="81187-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="81187-136">DLL</span><span class="sxs-lookup"><span data-stu-id="81187-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="81187-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="81187-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81187-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="81187-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81187-139">**\_СИСТЕМКОМПОНЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="81187-139">**CIM\_SystemComponent**</span></span>](cim-systemcomponent.md)
</dt> <dt>

[<span data-ttu-id="81187-140">Классы операционной системы</span><span class="sxs-lookup"><span data-stu-id="81187-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
