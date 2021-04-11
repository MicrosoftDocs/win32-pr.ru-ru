---
description: '\_Класс WMI взаимосвязей Win32 системнетворкконнектионс связывает сетевое подключение и компьютерную систему, в которой он находится.'
ms.assetid: 7c47f653-74a9-4729-a72c-94930181f8c9
ms.tgt_platform: multiple
title: Класс Win32_SystemNetworkConnections
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemNetworkConnections
- Win32_SystemNetworkConnections.GroupComponent
- Win32_SystemNetworkConnections.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e90562dd4f98a00cf848fb83a9e3051b387241e4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142694"
---
# <a name="win32_systemnetworkconnections-class"></a><span data-ttu-id="413c7-103">\_Класс Win32 системнетворкконнектионс</span><span class="sxs-lookup"><span data-stu-id="413c7-103">Win32\_SystemNetworkConnections class</span></span>

<span data-ttu-id="413c7-104">[Класс WMI](../wmisdk/retrieving-a-class.md) взаимосвязей **Win32 \_ системнетворкконнектионс** связывает сетевое подключение и компьютерную систему, в которой он находится.</span><span class="sxs-lookup"><span data-stu-id="413c7-104">The **Win32\_SystemNetworkConnections** association [WMI class](../wmisdk/retrieving-a-class.md) relates a network connection and the computer system on which it resides.</span></span>

<span data-ttu-id="413c7-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="413c7-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="413c7-106">Свойства и методы имеют алфавитный порядок, а не порядок MOF.</span><span class="sxs-lookup"><span data-stu-id="413c7-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="413c7-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="413c7-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4F7-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemNetworkConnections : CIM_SystemComponent
{
  Win32_ComputerSystem    REF GroupComponent;
  Win32_NetworkConnection REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="413c7-108">Члены</span><span class="sxs-lookup"><span data-stu-id="413c7-108">Members</span></span>

<span data-ttu-id="413c7-109">Класс **Win32 \_ системнетворкконнектионс** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="413c7-109">The **Win32\_SystemNetworkConnections** class has these types of members:</span></span>

-   [<span data-ttu-id="413c7-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="413c7-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="413c7-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="413c7-111">Properties</span></span>

<span data-ttu-id="413c7-112">Класс **Win32 \_ системнетворкконнектионс** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="413c7-112">The **Win32\_SystemNetworkConnections** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="413c7-113">**Ссылка**</span><span class="sxs-lookup"><span data-stu-id="413c7-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="413c7-114">Тип данных: **Win32 \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="413c7-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="413c7-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="413c7-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="413c7-116">Квалификаторы: [**ключ**](../wmisdk/key-qualifier.md), [**Переопределение**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ ComputerSystem")</span><span class="sxs-lookup"><span data-stu-id="413c7-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="413c7-117">Ссылка на экземпляр, представляющий компьютерную систему, подключенную к сети.</span><span class="sxs-lookup"><span data-stu-id="413c7-117">Reference to the instance representing the computer system connected to the network.</span></span>

</dd> <dt>

<span data-ttu-id="413c7-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="413c7-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="413c7-119">Тип данных: **Win32 \_ NetworkConnection**</span><span class="sxs-lookup"><span data-stu-id="413c7-119">Data type: **Win32\_NetworkConnection**</span></span>
</dt> <dt>

<span data-ttu-id="413c7-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="413c7-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="413c7-121">Квалификаторы: [**ключ**](../wmisdk/key-qualifier.md), [**Переопределение**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ NetworkConnection")</span><span class="sxs-lookup"><span data-stu-id="413c7-121">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_NetworkConnection")</span></span>
</dt> </dl>

<span data-ttu-id="413c7-122">Ссылка на экземпляр, представляющий сетевое подключение к данной компьютерной системе.</span><span class="sxs-lookup"><span data-stu-id="413c7-122">Reference to the instance representing the network connection to this computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="413c7-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="413c7-123">Remarks</span></span>

<span data-ttu-id="413c7-124">Класс **Win32 \_ системнетворкконнектионс** является производным от [**CIM \_ системкомпонент**](cim-systemcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="413c7-124">The **Win32\_SystemNetworkConnections** class is derived from [**CIM\_SystemComponent**](cim-systemcomponent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="413c7-125">Требования</span><span class="sxs-lookup"><span data-stu-id="413c7-125">Requirements</span></span>



| <span data-ttu-id="413c7-126">Требование</span><span class="sxs-lookup"><span data-stu-id="413c7-126">Requirement</span></span> | <span data-ttu-id="413c7-127">Значение</span><span class="sxs-lookup"><span data-stu-id="413c7-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="413c7-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="413c7-128">Minimum supported client</span></span><br/> | <span data-ttu-id="413c7-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="413c7-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="413c7-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="413c7-130">Minimum supported server</span></span><br/> | <span data-ttu-id="413c7-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="413c7-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="413c7-132">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="413c7-132">Namespace</span></span><br/>                | <span data-ttu-id="413c7-133">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="413c7-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="413c7-134">MOF</span><span class="sxs-lookup"><span data-stu-id="413c7-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="413c7-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="413c7-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="413c7-136">DLL</span><span class="sxs-lookup"><span data-stu-id="413c7-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="413c7-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="413c7-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="413c7-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="413c7-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="413c7-139">**\_СИСТЕМКОМПОНЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="413c7-139">**CIM\_SystemComponent**</span></span>](cim-systemcomponent.md)
</dt> <dt>

[<span data-ttu-id="413c7-140">Классы операционной системы</span><span class="sxs-lookup"><span data-stu-id="413c7-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
