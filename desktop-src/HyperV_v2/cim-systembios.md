---
description: Связывает BIOS с компьютерной системой.
ms.assetid: a06af789-75c8-4d58-8a25-572dcf1091e2
title: Класс CIM_SystemBIOS
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SystemBIOS
- CIM_SystemBIOS.GroupComponent
- CIM_SystemBIOS.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: faa3130544fdb97bdf216fa266bc9e8cfe1815bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080603"
---
# <a name="cim_systembios-class"></a><span data-ttu-id="e6a3c-103">\_Класс CIM систембиос</span><span class="sxs-lookup"><span data-stu-id="e6a3c-103">CIM\_SystemBIOS class</span></span>

<span data-ttu-id="e6a3c-104">Связывает BIOS с компьютерной системой.</span><span class="sxs-lookup"><span data-stu-id="e6a3c-104">Associates a BIOS with a computer system.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6a3c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e6a3c-105">Syntax</span></span>

``` syntax
[Association, Aggregation, Abstract, Version("2.7.0"), UMLPackagePath("CIM::Application::BIOS"), AMENDMENT]
class CIM_SystemBIOS : CIM_SystemComponent
{
  CIM_ComputerSystem REF GroupComponent;
  CIM_BIOSElement    REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="e6a3c-106">Члены</span><span class="sxs-lookup"><span data-stu-id="e6a3c-106">Members</span></span>

<span data-ttu-id="e6a3c-107">Класс **CIM \_ систембиос** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="e6a3c-107">The **CIM\_SystemBIOS** class has these types of members:</span></span>

-   [<span data-ttu-id="e6a3c-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="e6a3c-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e6a3c-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="e6a3c-109">Properties</span></span>

<span data-ttu-id="e6a3c-110">Класс **CIM \_ систембиос** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="e6a3c-110">The **CIM\_SystemBIOS** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e6a3c-111">**Ссылка**</span><span class="sxs-lookup"><span data-stu-id="e6a3c-111">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6a3c-112">Тип данных: **CIM \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="e6a3c-112">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="e6a3c-113">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e6a3c-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e6a3c-114">Квалификаторы: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**reoverride**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="e6a3c-114">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="e6a3c-115">Компьютерная система, которая загружается из BIOS.</span><span class="sxs-lookup"><span data-stu-id="e6a3c-115">The computer system that boots from the BIOS.</span></span>

</dd> <dt>

<span data-ttu-id="e6a3c-116">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="e6a3c-116">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6a3c-117">Тип данных: **CIM \_ биоселемент**</span><span class="sxs-lookup"><span data-stu-id="e6a3c-117">Data type: **CIM\_BIOSElement**</span></span>
</dt> <dt>

<span data-ttu-id="e6a3c-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e6a3c-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e6a3c-119">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="e6a3c-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="e6a3c-120">BIOS.</span><span class="sxs-lookup"><span data-stu-id="e6a3c-120">The BIOS.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e6a3c-121">Требования</span><span class="sxs-lookup"><span data-stu-id="e6a3c-121">Requirements</span></span>



| <span data-ttu-id="e6a3c-122">Требование</span><span class="sxs-lookup"><span data-stu-id="e6a3c-122">Requirement</span></span> | <span data-ttu-id="e6a3c-123">Значение</span><span class="sxs-lookup"><span data-stu-id="e6a3c-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6a3c-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e6a3c-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e6a3c-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="e6a3c-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="e6a3c-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e6a3c-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e6a3c-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e6a3c-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="e6a3c-128">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e6a3c-128">Namespace</span></span><br/>                | <span data-ttu-id="e6a3c-129">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="e6a3c-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="e6a3c-130">MOF</span><span class="sxs-lookup"><span data-stu-id="e6a3c-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e6a3c-131"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e6a3c-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e6a3c-132">DLL</span><span class="sxs-lookup"><span data-stu-id="e6a3c-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e6a3c-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e6a3c-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e6a3c-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e6a3c-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6a3c-135">**\_СИСТЕМКОМПОНЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="e6a3c-135">**CIM\_SystemComponent**</span></span>](cim-systemcomponent.md)
</dt> </dl>

 

