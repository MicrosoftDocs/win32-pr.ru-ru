---
description: '\_Класс WMI взаимосвязей Win32 системлоадордерграупс связывает компьютерную систему и группу порядка загрузки.'
ms.assetid: fb637300-0f70-465a-a72b-f0ab3f246790
ms.tgt_platform: multiple
title: Класс Win32_SystemLoadOrderGroups
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemLoadOrderGroups
- Win32_SystemLoadOrderGroups.GroupComponent
- Win32_SystemLoadOrderGroups.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 510acfbde2f562493a454abe80a4f7788377e556
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105656039"
---
# <a name="win32_systemloadordergroups-class"></a><span data-ttu-id="dd1cd-103">\_Класс Win32 системлоадордерграупс</span><span class="sxs-lookup"><span data-stu-id="dd1cd-103">Win32\_SystemLoadOrderGroups class</span></span>

<span data-ttu-id="dd1cd-104">[Класс WMI](../wmisdk/retrieving-a-class.md) взаимосвязей **Win32 \_ системлоадордерграупс** связывает компьютерную систему и группу порядка загрузки.</span><span class="sxs-lookup"><span data-stu-id="dd1cd-104">The **Win32\_SystemLoadOrderGroups** association [WMI class](../wmisdk/retrieving-a-class.md) relates a computer system and a load order group.</span></span>

<span data-ttu-id="dd1cd-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="dd1cd-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="dd1cd-106">Свойства и методы имеют алфавитный порядок, а не порядок MOF.</span><span class="sxs-lookup"><span data-stu-id="dd1cd-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd1cd-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dd1cd-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C503-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemLoadOrderGroups : CIM_SystemComponent
{
  Win32_ComputerSystem REF GroupComponent;
  Win32_LoadOrderGroup REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="dd1cd-108">Члены</span><span class="sxs-lookup"><span data-stu-id="dd1cd-108">Members</span></span>

<span data-ttu-id="dd1cd-109">Класс **Win32 \_ системлоадордерграупс** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="dd1cd-109">The **Win32\_SystemLoadOrderGroups** class has these types of members:</span></span>

-   [<span data-ttu-id="dd1cd-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="dd1cd-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="dd1cd-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="dd1cd-111">Properties</span></span>

<span data-ttu-id="dd1cd-112">Класс **Win32 \_ системлоадордерграупс** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="dd1cd-112">The **Win32\_SystemLoadOrderGroups** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dd1cd-113">**Ссылка**</span><span class="sxs-lookup"><span data-stu-id="dd1cd-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd1cd-114">Тип данных: **Win32 \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="dd1cd-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="dd1cd-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dd1cd-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd1cd-116">Квалификаторы: [**ключ**](../wmisdk/key-qualifier.md), [**Переопределение**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ ComputerSystem")</span><span class="sxs-lookup"><span data-stu-id="dd1cd-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="dd1cd-117">Ссылка на экземпляр, представляющий компьютерную систему, в которой существует группа "порядок загрузки".</span><span class="sxs-lookup"><span data-stu-id="dd1cd-117">Reference to the instance representing the computer system where the load order group exists.</span></span>

</dd> <dt>

<span data-ttu-id="dd1cd-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="dd1cd-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd1cd-119">Тип данных: **Win32 \_ лоадордерграуп**</span><span class="sxs-lookup"><span data-stu-id="dd1cd-119">Data type: **Win32\_LoadOrderGroup**</span></span>
</dt> <dt>

<span data-ttu-id="dd1cd-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dd1cd-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd1cd-121">Квалификаторы: [**ключ**](../wmisdk/key-qualifier.md), [**Переопределение**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ лоадордерграуп")</span><span class="sxs-lookup"><span data-stu-id="dd1cd-121">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_LoadOrderGroup")</span></span>
</dt> </dl>

<span data-ttu-id="dd1cd-122">Ссылка на экземпляр, представляющий группу порядка загрузки, существующую в компьютерной системе.</span><span class="sxs-lookup"><span data-stu-id="dd1cd-122">Reference to the instance representing the load order group existing on the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dd1cd-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dd1cd-123">Remarks</span></span>

<span data-ttu-id="dd1cd-124">Класс **Win32 \_ системлоадордерграупс** является производным от [**CIM \_ системкомпонент**](cim-systemcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="dd1cd-124">The **Win32\_SystemLoadOrderGroups** class is derived from [**CIM\_SystemComponent**](cim-systemcomponent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="dd1cd-125">Требования</span><span class="sxs-lookup"><span data-stu-id="dd1cd-125">Requirements</span></span>



| <span data-ttu-id="dd1cd-126">Требование</span><span class="sxs-lookup"><span data-stu-id="dd1cd-126">Requirement</span></span> | <span data-ttu-id="dd1cd-127">Значение</span><span class="sxs-lookup"><span data-stu-id="dd1cd-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dd1cd-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dd1cd-128">Minimum supported client</span></span><br/> | <span data-ttu-id="dd1cd-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dd1cd-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="dd1cd-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dd1cd-130">Minimum supported server</span></span><br/> | <span data-ttu-id="dd1cd-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dd1cd-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="dd1cd-132">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="dd1cd-132">Namespace</span></span><br/>                | <span data-ttu-id="dd1cd-133">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="dd1cd-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="dd1cd-134">MOF</span><span class="sxs-lookup"><span data-stu-id="dd1cd-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dd1cd-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dd1cd-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="dd1cd-136">DLL</span><span class="sxs-lookup"><span data-stu-id="dd1cd-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dd1cd-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dd1cd-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd1cd-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dd1cd-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd1cd-139">**\_СИСТЕМКОМПОНЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="dd1cd-139">**CIM\_SystemComponent**</span></span>](cim-systemcomponent.md)
</dt> <dt>

[<span data-ttu-id="dd1cd-140">Классы операционной системы</span><span class="sxs-lookup"><span data-stu-id="dd1cd-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
