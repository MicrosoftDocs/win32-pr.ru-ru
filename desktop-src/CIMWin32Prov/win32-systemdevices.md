---
description: '\_Класс WMI взаимосвязей Win32 системдевицес связывает компьютерную систему и логическое устройство, установленное в этой системе.'
ms.assetid: 84dfcb75-3b44-4b27-8eee-779be522eb1f
ms.tgt_platform: multiple
title: Класс Win32_SystemDevices
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDevices
- Win32_SystemDevices.GroupComponent
- Win32_SystemDevices.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b2b28c11e10318e3bca562baf93bc20df9b756cf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896341"
---
# <a name="win32_systemdevices-class"></a><span data-ttu-id="94ee5-103">\_Класс Win32 системдевицес</span><span class="sxs-lookup"><span data-stu-id="94ee5-103">Win32\_SystemDevices class</span></span>

<span data-ttu-id="94ee5-104">[Класс WMI](../wmisdk/retrieving-a-class.md) взаимосвязей **Win32 \_ системдевицес** связывает компьютерную систему и логическое устройство, установленное в этой системе.</span><span class="sxs-lookup"><span data-stu-id="94ee5-104">The **Win32\_SystemDevices** association [WMI class](../wmisdk/retrieving-a-class.md) relates a computer system and a logical device installed on that system.</span></span>

<span data-ttu-id="94ee5-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="94ee5-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="94ee5-106">Свойства и методы имеют алфавитный порядок, а не порядок MOF.</span><span class="sxs-lookup"><span data-stu-id="94ee5-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="94ee5-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="94ee5-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4F4-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemDevices : CIM_SystemDevice
{
  Win32_ComputerSystem REF GroupComponent;
  CIM_LogicalDevice    REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="94ee5-108">Члены</span><span class="sxs-lookup"><span data-stu-id="94ee5-108">Members</span></span>

<span data-ttu-id="94ee5-109">Класс **Win32 \_ системдевицес** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="94ee5-109">The **Win32\_SystemDevices** class has these types of members:</span></span>

-   [<span data-ttu-id="94ee5-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="94ee5-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="94ee5-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="94ee5-111">Properties</span></span>

<span data-ttu-id="94ee5-112">Класс **Win32 \_ системдевицес** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="94ee5-112">The **Win32\_SystemDevices** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="94ee5-113">**Ссылка**</span><span class="sxs-lookup"><span data-stu-id="94ee5-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94ee5-114">Тип данных: **Win32 \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="94ee5-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="94ee5-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="94ee5-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="94ee5-116">Квалификаторы: [**ключ**](../wmisdk/key-qualifier.md), [**Переопределение**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ ComputerSystem")</span><span class="sxs-lookup"><span data-stu-id="94ee5-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="94ee5-117">Ссылка на экземпляр, представляющий свойства компьютерной системы, в которой существует логическое устройство.</span><span class="sxs-lookup"><span data-stu-id="94ee5-117">Reference to the instance representing the properties of the computer system where the logical device exists.</span></span>

</dd> <dt>

<span data-ttu-id="94ee5-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="94ee5-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94ee5-119">Тип данных: **CIM \_** с типом "модель"</span><span class="sxs-lookup"><span data-stu-id="94ee5-119">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="94ee5-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="94ee5-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="94ee5-121">Квалификаторы: [**ключ**](../wmisdk/key-qualifier.md), [**Переопределение**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("CIM \| CIM \_ ")</span><span class="sxs-lookup"><span data-stu-id="94ee5-121">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM\|CIM\_LogicalDevice")</span></span>
</dt> </dl>

<span data-ttu-id="94ee5-122">Ссылка на экземпляр, представляющий свойства логического устройства, существующего в компьютерной системе.</span><span class="sxs-lookup"><span data-stu-id="94ee5-122">Reference to the instance representing the properties of a logical device that exists on the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="94ee5-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="94ee5-123">Remarks</span></span>

<span data-ttu-id="94ee5-124">Класс **Win32 \_ системдевицес** является производным от [**CIM \_ системдевице**](cim-systemdevice.md).</span><span class="sxs-lookup"><span data-stu-id="94ee5-124">The **Win32\_SystemDevices** class is derived from [**CIM\_SystemDevice**](cim-systemdevice.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="94ee5-125">Требования</span><span class="sxs-lookup"><span data-stu-id="94ee5-125">Requirements</span></span>



| <span data-ttu-id="94ee5-126">Требование</span><span class="sxs-lookup"><span data-stu-id="94ee5-126">Requirement</span></span> | <span data-ttu-id="94ee5-127">Значение</span><span class="sxs-lookup"><span data-stu-id="94ee5-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="94ee5-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="94ee5-128">Minimum supported client</span></span><br/> | <span data-ttu-id="94ee5-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="94ee5-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="94ee5-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="94ee5-130">Minimum supported server</span></span><br/> | <span data-ttu-id="94ee5-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="94ee5-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="94ee5-132">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="94ee5-132">Namespace</span></span><br/>                | <span data-ttu-id="94ee5-133">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="94ee5-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="94ee5-134">MOF</span><span class="sxs-lookup"><span data-stu-id="94ee5-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="94ee5-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="94ee5-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="94ee5-136">DLL</span><span class="sxs-lookup"><span data-stu-id="94ee5-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="94ee5-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="94ee5-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94ee5-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="94ee5-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94ee5-139">**\_СИСТЕМДЕВИЦЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="94ee5-139">**CIM\_SystemDevice**</span></span>](cim-systemdevice.md)
</dt> <dt>

[<span data-ttu-id="94ee5-140">Классы операционной системы</span><span class="sxs-lookup"><span data-stu-id="94ee5-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
