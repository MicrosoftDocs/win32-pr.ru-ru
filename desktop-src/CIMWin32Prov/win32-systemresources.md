---
description: '\_Класс WMI взаимосвязей Win32 системресаурцес связывает системный ресурс и компьютерную систему, на которой он находится.'
ms.assetid: 90bff0b0-7c1d-44bf-b67e-aefeaa4b4a83
ms.tgt_platform: multiple
title: Класс Win32_SystemResources
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemResources
- Win32_SystemResources.GroupComponent
- Win32_SystemResources.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: fe96467e4bc609fa9426edd3c977b5596ea95fe7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990563"
---
# <a name="win32_systemresources-class"></a><span data-ttu-id="872bc-103">\_Класс Win32 системресаурцес</span><span class="sxs-lookup"><span data-stu-id="872bc-103">Win32\_SystemResources class</span></span>

<span data-ttu-id="872bc-104">[Класс WMI](../wmisdk/retrieving-a-class.md) взаимосвязей **Win32 \_ системресаурцес** связывает системный ресурс и компьютерную систему, на которой он находится.</span><span class="sxs-lookup"><span data-stu-id="872bc-104">The **Win32\_SystemResources** association [WMI class](../wmisdk/retrieving-a-class.md) relates a system resource and the computer system it resides on.</span></span>

<span data-ttu-id="872bc-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="872bc-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="872bc-106">Свойства и методы имеют алфавитный порядок, а не порядок MOF.</span><span class="sxs-lookup"><span data-stu-id="872bc-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="872bc-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="872bc-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4F8-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemResources : CIM_ComputerSystemResource
{
  Win32_ComputerSystem REF GroupComponent;
  CIM_SystemResource   REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="872bc-108">Члены</span><span class="sxs-lookup"><span data-stu-id="872bc-108">Members</span></span>

<span data-ttu-id="872bc-109">Класс **Win32 \_ системресаурцес** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="872bc-109">The **Win32\_SystemResources** class has these types of members:</span></span>

-   [<span data-ttu-id="872bc-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="872bc-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="872bc-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="872bc-111">Properties</span></span>

<span data-ttu-id="872bc-112">Класс **Win32 \_ системресаурцес** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="872bc-112">The **Win32\_SystemResources** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="872bc-113">**Ссылка**</span><span class="sxs-lookup"><span data-stu-id="872bc-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="872bc-114">Тип данных: **Win32 \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="872bc-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="872bc-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="872bc-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="872bc-116">Квалификаторы: [**ключ**](../wmisdk/key-qualifier.md), [**Переопределение**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ ComputerSystem")</span><span class="sxs-lookup"><span data-stu-id="872bc-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="872bc-117">Ссылка на экземпляр, представляющий компьютерную систему, в которой находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="872bc-117">Reference to the instance representing the computer system where the resource is located.</span></span>

</dd> <dt>

<span data-ttu-id="872bc-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="872bc-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="872bc-119">Тип данных: **CIM \_ системресаурце**</span><span class="sxs-lookup"><span data-stu-id="872bc-119">Data type: **CIM\_SystemResource**</span></span>
</dt> <dt>

<span data-ttu-id="872bc-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="872bc-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="872bc-121">Квалификаторы: [**ключ**](../wmisdk/key-qualifier.md), [**Переопределение**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("CIM \| CIM \_ системресаурце")</span><span class="sxs-lookup"><span data-stu-id="872bc-121">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM\|CIM\_SystemResource")</span></span>
</dt> </dl>

<span data-ttu-id="872bc-122">Ссылка на экземпляр, представляющий ресурс (например, службы ввода-вывода и ресурсы памяти), доступный в компьютерной системе.</span><span class="sxs-lookup"><span data-stu-id="872bc-122">Reference to the instance representing the resource (such as I/O services and memory resources) available on the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="872bc-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="872bc-123">Remarks</span></span>

<span data-ttu-id="872bc-124">Класс **Win32 \_ системресаурцес** является производным от [**CIM \_ компутерсистемресаурце**](cim-computersystemresource.md).</span><span class="sxs-lookup"><span data-stu-id="872bc-124">The **Win32\_SystemResources** class is derived from [**CIM\_ComputerSystemResource**](cim-computersystemresource.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="872bc-125">Требования</span><span class="sxs-lookup"><span data-stu-id="872bc-125">Requirements</span></span>



| <span data-ttu-id="872bc-126">Требование</span><span class="sxs-lookup"><span data-stu-id="872bc-126">Requirement</span></span> | <span data-ttu-id="872bc-127">Значение</span><span class="sxs-lookup"><span data-stu-id="872bc-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="872bc-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="872bc-128">Minimum supported client</span></span><br/> | <span data-ttu-id="872bc-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="872bc-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="872bc-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="872bc-130">Minimum supported server</span></span><br/> | <span data-ttu-id="872bc-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="872bc-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="872bc-132">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="872bc-132">Namespace</span></span><br/>                | <span data-ttu-id="872bc-133">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="872bc-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="872bc-134">MOF</span><span class="sxs-lookup"><span data-stu-id="872bc-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="872bc-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="872bc-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="872bc-136">DLL</span><span class="sxs-lookup"><span data-stu-id="872bc-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="872bc-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="872bc-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="872bc-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="872bc-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="872bc-139">**\_КОМПУТЕРСИСТЕМРЕСАУРЦЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="872bc-139">**CIM\_ComputerSystemResource**</span></span>](cim-computersystemresource.md)
</dt> <dt>

[<span data-ttu-id="872bc-140">Классы операционной системы</span><span class="sxs-lookup"><span data-stu-id="872bc-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
