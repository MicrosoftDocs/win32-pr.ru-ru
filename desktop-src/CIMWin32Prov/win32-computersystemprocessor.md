---
description: '\_Класс WMI взаимосвязей Win32 компутерсистемпроцессор связывает компьютерную систему и процессор, работающий в этой системе.'
ms.assetid: e630ebea-19bf-43c7-a8a0-7acfda3a752b
ms.tgt_platform: multiple
title: Класс Win32_ComputerSystemProcessor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ComputerSystemProcessor
- Win32_ComputerSystemProcessor.PartComponent
- Win32_ComputerSystemProcessor.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2f836d8f5e9053029763c38d2c4f2116987b08fe
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141166"
---
# <a name="win32_computersystemprocessor-class"></a><span data-ttu-id="d1444-103">\_Класс Win32 компутерсистемпроцессор</span><span class="sxs-lookup"><span data-stu-id="d1444-103">Win32\_ComputerSystemProcessor class</span></span>

<span data-ttu-id="d1444-104">[Класс WMI](/windows/desktop/WmiSdk/retrieving-a-class) взаимосвязей **Win32 \_ компутерсистемпроцессор** связывает компьютерную систему и процессор, работающий в этой системе.</span><span class="sxs-lookup"><span data-stu-id="d1444-104">The **Win32\_ComputerSystemProcessor** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a computer system and a processor running on that system.</span></span>

<span data-ttu-id="d1444-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="d1444-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="d1444-106">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="d1444-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1444-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d1444-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{719A6839-C124-11d2-85E8-0000F8102E5F}"), AMENDMENT]
class Win32_ComputerSystemProcessor : Win32_SystemDevices
{
  Win32_Processor      REF PartComponent;
  Win32_ComputerSystem REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="d1444-108">Члены</span><span class="sxs-lookup"><span data-stu-id="d1444-108">Members</span></span>

<span data-ttu-id="d1444-109">Класс **Win32 \_ компутерсистемпроцессор** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="d1444-109">The **Win32\_ComputerSystemProcessor** class has these types of members:</span></span>

-   [<span data-ttu-id="d1444-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="d1444-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d1444-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="d1444-111">Properties</span></span>

<span data-ttu-id="d1444-112">Класс **Win32 \_ компутерсистемпроцессор** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="d1444-112">The **Win32\_ComputerSystemProcessor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d1444-113">**Ссылка**</span><span class="sxs-lookup"><span data-stu-id="d1444-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1444-114">Тип данных: **Win32 \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="d1444-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="d1444-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1444-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1444-116">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ ComputerSystem")</span><span class="sxs-lookup"><span data-stu-id="d1444-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="d1444-117">**Платформа Win32 \_ ComputerSystem** , описывающая свойства компьютерной системы, на которой работает процессор.</span><span class="sxs-lookup"><span data-stu-id="d1444-117">A **Win32\_ComputerSystem** that describes the properties of the computer system on which the processor is running.</span></span>

</dd> <dt>

<span data-ttu-id="d1444-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="d1444-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1444-119">Тип данных: **\_ процессор Win32**</span><span class="sxs-lookup"><span data-stu-id="d1444-119">Data type: **Win32\_Processor**</span></span>
</dt> <dt>

<span data-ttu-id="d1444-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1444-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1444-121">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| обработчик WMI Win32 \_ ")</span><span class="sxs-lookup"><span data-stu-id="d1444-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_Processor")</span></span>
</dt> </dl>

<span data-ttu-id="d1444-122">[**\_ Процессор Win32**](win32-processor.md) , описывающий свойства процессора, на котором работает компьютерная система.</span><span class="sxs-lookup"><span data-stu-id="d1444-122">A [**Win32\_Processor**](win32-processor.md) that describes the properties of a processor which is running the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d1444-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d1444-123">Remarks</span></span>

<span data-ttu-id="d1444-124">Класс **Win32 \_ компутерсистемпроцессор** является производным от [**Win32 \_ системдевицес**](win32-systemdevices.md).</span><span class="sxs-lookup"><span data-stu-id="d1444-124">The **Win32\_ComputerSystemProcessor** class is derived from [**Win32\_SystemDevices**](win32-systemdevices.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d1444-125">Требования</span><span class="sxs-lookup"><span data-stu-id="d1444-125">Requirements</span></span>



| <span data-ttu-id="d1444-126">Требование</span><span class="sxs-lookup"><span data-stu-id="d1444-126">Requirement</span></span> | <span data-ttu-id="d1444-127">Значение</span><span class="sxs-lookup"><span data-stu-id="d1444-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d1444-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d1444-128">Minimum supported client</span></span><br/> | <span data-ttu-id="d1444-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d1444-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d1444-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d1444-130">Minimum supported server</span></span><br/> | <span data-ttu-id="d1444-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d1444-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d1444-132">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="d1444-132">Namespace</span></span><br/>                | <span data-ttu-id="d1444-133">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="d1444-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d1444-134">MOF</span><span class="sxs-lookup"><span data-stu-id="d1444-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d1444-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d1444-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d1444-136">DLL</span><span class="sxs-lookup"><span data-stu-id="d1444-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d1444-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d1444-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1444-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d1444-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1444-139">**\_Системдевицес Win32**</span><span class="sxs-lookup"><span data-stu-id="d1444-139">**Win32\_SystemDevices**</span></span>](win32-systemdevices.md)
</dt> <dt>

<span data-ttu-id="d1444-140">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d1444-140">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

