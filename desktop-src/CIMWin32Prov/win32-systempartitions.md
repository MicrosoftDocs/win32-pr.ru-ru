---
description: '\_Класс WMI взаимосвязей Win32 системпартитионс связывает компьютерную систему и раздел диска в этой системе.'
ms.assetid: e8f02cd0-9446-4258-b476-5dc6c72c80d4
ms.tgt_platform: multiple
title: Класс Win32_SystemPartitions
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemPartitions
- Win32_SystemPartitions.GroupComponent
- Win32_SystemPartitions.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: deae8129772e5d854f05b5b953ec66a12bd5bcaf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895930"
---
# <a name="win32_systempartitions-class"></a><span data-ttu-id="7c1bd-103">\_Класс Win32 системпартитионс</span><span class="sxs-lookup"><span data-stu-id="7c1bd-103">Win32\_SystemPartitions class</span></span>

<span data-ttu-id="7c1bd-104">[Класс WMI](../wmisdk/retrieving-a-class.md) взаимосвязей **Win32 \_ системпартитионс** связывает компьютерную систему и раздел диска в этой системе.</span><span class="sxs-lookup"><span data-stu-id="7c1bd-104">The **Win32\_SystemPartitions** association [WMI class](../wmisdk/retrieving-a-class.md) relates a computer system and a disk partition on that system.</span></span>

<span data-ttu-id="7c1bd-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="7c1bd-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="7c1bd-106">Свойства и методы имеют алфавитный порядок, а не порядок MOF.</span><span class="sxs-lookup"><span data-stu-id="7c1bd-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c1bd-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7c1bd-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4F5-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemPartitions : Win32_SystemDevices
{
  Win32_ComputerSystem REF GroupComponent;
  Win32_DiskPartition  REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="7c1bd-108">Члены</span><span class="sxs-lookup"><span data-stu-id="7c1bd-108">Members</span></span>

<span data-ttu-id="7c1bd-109">Класс **Win32 \_ системпартитионс** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="7c1bd-109">The **Win32\_SystemPartitions** class has these types of members:</span></span>

-   [<span data-ttu-id="7c1bd-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="7c1bd-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7c1bd-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="7c1bd-111">Properties</span></span>

<span data-ttu-id="7c1bd-112">Класс **Win32 \_ системпартитионс** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="7c1bd-112">The **Win32\_SystemPartitions** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7c1bd-113">**Ссылка**</span><span class="sxs-lookup"><span data-stu-id="7c1bd-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c1bd-114">Тип данных: **Win32 \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="7c1bd-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="7c1bd-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7c1bd-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7c1bd-116">Квалификаторы: [**override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ ComputerSystem")</span><span class="sxs-lookup"><span data-stu-id="7c1bd-116">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="7c1bd-117">Ссылка на экземпляр, представляющий свойства компьютерной системы, в которой находится раздел диска.</span><span class="sxs-lookup"><span data-stu-id="7c1bd-117">Reference to the instance representing the properties of the computer system where the disk partition is located.</span></span>

</dd> <dt>

<span data-ttu-id="7c1bd-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="7c1bd-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c1bd-119">Тип данных: **Win32 \_ дискпартитион**</span><span class="sxs-lookup"><span data-stu-id="7c1bd-119">Data type: **Win32\_DiskPartition**</span></span>
</dt> <dt>

<span data-ttu-id="7c1bd-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7c1bd-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7c1bd-121">Квалификаторы: [**override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ дискпартитион")</span><span class="sxs-lookup"><span data-stu-id="7c1bd-121">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_DiskPartition")</span></span>
</dt> </dl>

<span data-ttu-id="7c1bd-122">Ссылка на экземпляр, представляющий свойства раздела диска, существующего в компьютерной системе.</span><span class="sxs-lookup"><span data-stu-id="7c1bd-122">Reference to the instance representing the properties of a disk partition that exists on the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7c1bd-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7c1bd-123">Remarks</span></span>

<span data-ttu-id="7c1bd-124">Класс **Win32 \_ системпартитионс** является производным от [**Win32 \_ системдевицес**](win32-systemdevices.md).</span><span class="sxs-lookup"><span data-stu-id="7c1bd-124">The **Win32\_SystemPartitions** class is derived from [**Win32\_SystemDevices**](win32-systemdevices.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7c1bd-125">Требования</span><span class="sxs-lookup"><span data-stu-id="7c1bd-125">Requirements</span></span>



| <span data-ttu-id="7c1bd-126">Требование</span><span class="sxs-lookup"><span data-stu-id="7c1bd-126">Requirement</span></span> | <span data-ttu-id="7c1bd-127">Значение</span><span class="sxs-lookup"><span data-stu-id="7c1bd-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7c1bd-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7c1bd-128">Minimum supported client</span></span><br/> | <span data-ttu-id="7c1bd-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7c1bd-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7c1bd-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7c1bd-130">Minimum supported server</span></span><br/> | <span data-ttu-id="7c1bd-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7c1bd-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7c1bd-132">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="7c1bd-132">Namespace</span></span><br/>                | <span data-ttu-id="7c1bd-133">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="7c1bd-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7c1bd-134">MOF</span><span class="sxs-lookup"><span data-stu-id="7c1bd-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7c1bd-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7c1bd-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7c1bd-136">DLL</span><span class="sxs-lookup"><span data-stu-id="7c1bd-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7c1bd-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7c1bd-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c1bd-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7c1bd-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c1bd-139">**\_Системдевицес Win32**</span><span class="sxs-lookup"><span data-stu-id="7c1bd-139">**Win32\_SystemDevices**</span></span>](win32-systemdevices.md)
</dt> <dt>

[<span data-ttu-id="7c1bd-140">Классы операционной системы</span><span class="sxs-lookup"><span data-stu-id="7c1bd-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
