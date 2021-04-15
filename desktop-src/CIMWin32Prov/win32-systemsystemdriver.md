---
description: '\_Класс WMI взаимосвязей Win32 системсистемдривер связывает компьютерную систему и системный драйвер, работающий на этой компьютерной системе.'
ms.assetid: 82638c29-6769-4410-90bc-b408b27adad4
ms.tgt_platform: multiple
title: Класс Win32_SystemSystemDriver
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemSystemDriver
- Win32_SystemSystemDriver.GroupComponent
- Win32_SystemSystemDriver.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b193d173fa0592a44ba437543659dec456e432ea
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539326"
---
# <a name="win32_systemsystemdriver-class"></a><span data-ttu-id="eedcf-103">\_Класс Win32 системсистемдривер</span><span class="sxs-lookup"><span data-stu-id="eedcf-103">Win32\_SystemSystemDriver class</span></span>

<span data-ttu-id="eedcf-104">[Класс WMI](../wmisdk/retrieving-a-class.md) взаимосвязей **Win32 \_ системсистемдривер** связывает компьютерную систему и системный драйвер, работающий на этой компьютерной системе.</span><span class="sxs-lookup"><span data-stu-id="eedcf-104">The **Win32\_SystemSystemDriver** association [WMI class](../wmisdk/retrieving-a-class.md) relates a computer system and a system driver running on that computer system.</span></span>

<span data-ttu-id="eedcf-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="eedcf-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="eedcf-106">Свойства и методы имеют алфавитный порядок, а не порядок MOF.</span><span class="sxs-lookup"><span data-stu-id="eedcf-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="eedcf-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="eedcf-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4F1-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemSystemDriver : CIM_SystemComponent
{
  Win32_ComputerSystem REF GroupComponent;
  Win32_SystemDriver   REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="eedcf-108">Члены</span><span class="sxs-lookup"><span data-stu-id="eedcf-108">Members</span></span>

<span data-ttu-id="eedcf-109">Класс **Win32 \_ системсистемдривер** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="eedcf-109">The **Win32\_SystemSystemDriver** class has these types of members:</span></span>

-   [<span data-ttu-id="eedcf-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="eedcf-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="eedcf-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="eedcf-111">Properties</span></span>

<span data-ttu-id="eedcf-112">Класс **Win32 \_ системсистемдривер** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="eedcf-112">The **Win32\_SystemSystemDriver** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="eedcf-113">**Ссылка**</span><span class="sxs-lookup"><span data-stu-id="eedcf-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eedcf-114">Тип данных: **Win32 \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="eedcf-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="eedcf-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="eedcf-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eedcf-116">Квалификаторы: [**ключ**](../wmisdk/key-qualifier.md), [**Переопределение**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ ComputerSystem")</span><span class="sxs-lookup"><span data-stu-id="eedcf-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="eedcf-117">Ссылка на экземпляр, представляющий свойства компьютерной системы, на которой выполняется драйвер.</span><span class="sxs-lookup"><span data-stu-id="eedcf-117">Reference to the instance representing the properties of the computer system upon which the driver is running.</span></span>

</dd> <dt>

<span data-ttu-id="eedcf-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="eedcf-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eedcf-119">Тип данных: **Win32 \_ SystemDriver**</span><span class="sxs-lookup"><span data-stu-id="eedcf-119">Data type: **Win32\_SystemDriver**</span></span>
</dt> <dt>

<span data-ttu-id="eedcf-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="eedcf-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eedcf-121">Квалификаторы: [**ключ**](../wmisdk/key-qualifier.md), [**Переопределение**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ SystemDriver")</span><span class="sxs-lookup"><span data-stu-id="eedcf-121">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_SystemDriver")</span></span>
</dt> </dl>

<span data-ttu-id="eedcf-122">Ссылка на экземпляр, представляющий системный драйвер, работающий в компьютерной системе.</span><span class="sxs-lookup"><span data-stu-id="eedcf-122">Reference to the instance representing the system driver running on the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="eedcf-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="eedcf-123">Remarks</span></span>

<span data-ttu-id="eedcf-124">Класс **Win32 \_ системсистемдривер** является производным от [**CIM \_ системкомпонент**](cim-systemcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="eedcf-124">The **Win32\_SystemSystemDriver** class is derived from [**CIM\_SystemComponent**](cim-systemcomponent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="eedcf-125">Требования</span><span class="sxs-lookup"><span data-stu-id="eedcf-125">Requirements</span></span>



| <span data-ttu-id="eedcf-126">Требование</span><span class="sxs-lookup"><span data-stu-id="eedcf-126">Requirement</span></span> | <span data-ttu-id="eedcf-127">Значение</span><span class="sxs-lookup"><span data-stu-id="eedcf-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="eedcf-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="eedcf-128">Minimum supported client</span></span><br/> | <span data-ttu-id="eedcf-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="eedcf-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="eedcf-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="eedcf-130">Minimum supported server</span></span><br/> | <span data-ttu-id="eedcf-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="eedcf-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="eedcf-132">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="eedcf-132">Namespace</span></span><br/>                | <span data-ttu-id="eedcf-133">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="eedcf-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="eedcf-134">MOF</span><span class="sxs-lookup"><span data-stu-id="eedcf-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="eedcf-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="eedcf-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="eedcf-136">DLL</span><span class="sxs-lookup"><span data-stu-id="eedcf-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eedcf-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eedcf-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eedcf-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="eedcf-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eedcf-139">**\_СИСТЕМКОМПОНЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="eedcf-139">**CIM\_SystemComponent**</span></span>](cim-systemcomponent.md)
</dt> <dt>

[<span data-ttu-id="eedcf-140">Классы операционной системы</span><span class="sxs-lookup"><span data-stu-id="eedcf-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
